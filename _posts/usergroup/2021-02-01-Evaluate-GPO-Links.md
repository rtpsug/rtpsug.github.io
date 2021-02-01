---
layout: post
category : usergroup
tagline: Evaluating GPO Links
tags : [UserGroup, News]
img : 
img-mobile : 
img2 : 
img3 : 
author : Jeremy Brown
title : Title - Evaluating GPO Links
title3 : 
css: 
js: 
bgcolor: ff5a71
keywords: UserGroup, News
canonical: https://fullit.github.io
---
{% include JB/setup %}

## Jeremy Brown

### Intro

This past week I needed to find duplicate links across nested OUs within the org.
The suspicion was there were a lot of GPOs linked repeatedly that could have been linked once at a higher level.
I thought I might make a quick post to talk about how I got the information.
Along the way, we can learn a little about Active Directory and GPOs.

### What is a GPO

GPOs, otherwise known as Group Policy Objects, apply desired state to domain joined devices and users.
Each Group policy consists of a Group Policy Object and Group Policy Template.
Every Group Policy you make can apply to a user, computer, or both.
When you make a GPO, the template contains a '.POL' file that imposes the desired state.
The .POL file is deployed from SYSVOL.
To go along with the template, there is an object that exists within the Active Directory database.
The object maintains consistency with everywhere an admin links a Group Policy.
That means if I have one Group Policy linked to 3 different OUs in the domain, I have one template and three references to that Group Policy Object.

### PowerShell and Group Policy

If you have the ActiveDirectory RSAT installed, you will have a few PowerShell modules installed on that device.
Not only do you get the ActiveDirectory module, you also get a GroupPolicy module.
We can look at what commands are available in the GroupPolicy module with:

```Get-Command -Module GroupPolicy```

Here we can see a lot of opportunity to interact with Group Policy; however, most of the options work on the template.
What we're interested in is the object.
These cmdlets allow the ability to create a new GPLink, which would affect a Group Policy object in AD.
But how can we count where a single GPO is linked everywhere in the domain?

### The Script

[Here is the script.](https://github.com/BananaJama/PowerShell/blob/main/Get-GpoByOu.ps1)
In this script we'll take in a DistinguishedName of an Organizational Unit and look for all GPOs linked from that location and further down the tree.
We'll start by getting a list of OUs to search across by issuing:

```$OuTree = Get-ADOrganizationalUnit -Filter * -SearchBase $SearchBaseDn -SearchScope Subtree```

Next, we need to evaluate the Group Policy GUID stored in AD against a friendly name.
To do this, we need to get all the GPOs in the domain.  We'll grab those with this command.

```$AllGPOs = Get-GPO -All```

If we look at a single OU, we can see there is a `LinkedGroupPolicyObjects` attribute.
This is what we're after.
This property will hold a list of all the GPO GUIDs linked at that OU.
Once we have those GUIDs, we can do a lookup against our list of all the GPOs and return a friendly name.
To accomplish this, I created a couple of private functions to help with the work.
The first private function looks like this:

```powershell
function GetGpoGuids {
    param (
        $LinkedGpos
    )

    $RegexPattern = '[A-Z0-9]{8}-[A-Z0-9]{4}-[A-Z0-9]{4}-[A-Z0-9]{4}-[A-Z0-9]{12}'
    
    foreach ($ou in $LinkedGpos) {
        ($ou | Select-String $RegexPattern).Matches.Value
    }
}
```

In this function, we can take the list of Group Policy links and retrieve just the GUID for that GPO.
Since the `LinkedGroupPolicyObjects` attribute is going to contain a list of items that look something like this:

```cn={316E23FF-9546-46BB-AB06-729FF2058E36},cn=policies,cn=system,DC=your,DC=domain,DC=com```

This code will use the regex to strip away everything but the GUID inside the curly braces and return only that as a value.

```316E23FF-9546-46BB-AB06-729FF2058E36```

Furthermore, since an OU may have more than one Group Policy linked to it, the attribute may have more more than 1 Group Policy link referenced.
We can just pass all the values in the list, whether that's 0 or 100, through a `foreach` loop and output all the GUIDs.

The next private function looks like this:

```powershell
function GetGpoFromGuid {
    param (
        $GpoGuid
        ,
        $GpoSearchBank
    )
    $GpoSearchBank.Where({$_.Id -eq $GpoGuid})
}
```

This function will take care of the lookup.
Here we will take in two parameters.
The first is the GUID of a single GPO link on an OU.
The second is the list of Group Policy objects we retrieved earlier.
From there, we can take the comprehensive list of all the GPOs and filter it down to a single GPO by looking for a matching GUID.
We'll use that output, the entire GPO, in the main script.

Now that we have looked at the private functions, let's look at the main script.

```powershell
foreach ($ou in $OuTree) {
    $LinkedGpos = $ou.LinkedGroupPolicyObjects
    $GpoGuids = GetGpoGuids -LinkedGpos $LinkedGpos
    $Gpos = $GpoGuids | ForEach-Object {GetGpoFromGuid -GpoGuid $_ -GpoSearchBank $AllGPOs}

    foreach ($gpo in $Gpos) {
        $Result = [PSCustomObject]@{
            OuName = $ou.Name
            OuDN = $ou.DistinguishedName
            GpoName = $gpo.DisplayName
        }
        $Result
    }
}
```

The working code is quite short.
We'll take each OU, evaluate it to retrieve the list of GUIDs for all linked GPOs, and return a custom object.
The custom object will contain the DN of the OU, the friendly name of the OU, and the friendly name of the GPO.
From here, we can store this in a variable and work on exploring afterward.
Once I completed the script, I quickly executed the following code from my terminal:

```powershell
$GpoInfo = .\Get-GpoByOu.ps1 -SearchBaseDn 'OU=foo,DC=domain,DC=com'
$GpoInfo | Export-CSV -Path 'GpoByOu.csv'
```

Following that, I could start counting duplication by using `Group-Object`

```powershell
$GpoInfo | Group-Object GpoName | Sort-Object Count -Descending
```

This would give us a count of how many links each GPO has per the OUs in the tree.
