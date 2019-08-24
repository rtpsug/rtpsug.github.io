---
name : Justin Gehman
img : justin_gehman.jpg
twitter : jmgehman
website : 
linkedin : 
bio : 
talk-title: PowerShell Streams and Using the Right Write-* Cmdlet
abstract:
    All native PowerShell cmdlets have what is called ‘Common Parameters’, which provides useful features like controlling error, informational, and verbose output. Understanding how this works is important when it comes time to write our own code that looks and acts like native PowerShell.
talk: PowerShell-101
index: 4
---

I spent years writing PowerShell scripts like I did my batch scripts - using ‘Write-Host’ to provide debugging output that I’d eventually comment out or informational output for the user. PowerShell has a much better way of handling these different types of output - and understanding how it works will allow you to take you PowerShell code to the next level. Learn how to make your functions accept ‘-Verbose’ just like native PowerShell cmdlet, and why the ‘Write-Information’ cmdlet was introduced in 5.0 and what it brings to the table.