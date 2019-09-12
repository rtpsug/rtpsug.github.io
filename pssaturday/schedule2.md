---
layout: page2
group : pssaturday-nav
title: Schedule
tagline: Schedule for the Day
---
{% include JB/setup %}
<!-- Content Area Start -->
<div class="table-style2">
    <div class="sub-title">
        <span>Saturday Schedule  - 8AM -5 PM</span>
    </div>
    <div class="table-responsive mtb">
        <table class="table table-bordered table-1 table-striped">
            <thead>
                <tr>
                    <td></td>
                    <th>PowerShell 101</th>
                    <th>PowerShell Tools</th>
                    <th>DevOps & Security</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            8:00 - 8:45
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Registration / Breakfast
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            8:45 - 9:00
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Welcome Discussion / layout day
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            9:00 - 9:50
                        </p>
                        <p><i>Session Block 1</i></p>
                    </td>
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-101" %}{% if session.index == 1 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-Tools" %}{% if session.index == 1 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-DevOps" %}{% if session.index == 1 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            10:00 -10:50
                        </p>
                        <p><i>Session Block 2</i></p>
                    </td>
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-101" %}{% if session.index == 2 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-Tools" %}{% if session.index == 2 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-DevOps" %}{% if session.index == 2 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            11:00 -11:50
                        </p>
                        <p><i>Session Block 3</i></p>
                    </td>
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-101" %}{% if session.index == 3 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-Tools" %}{% if session.index == 3 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-DevOps" %}{% if session.index == 3 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            12:00 - 1:00
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Lunch
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            1:00 - 1:50
                        </p>
                        <p><i>Session Block 4</i></p>
                    </td>
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-101" %}{% if session.index == 4 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-Tools" %}{% if session.index == 4 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-DevOps" %}{% if session.index == 4 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            2:00 - 2:50
                        </p>
                        <p><i>Session Block 5</i></p>
                    </td>
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-101" %}{% if session.index == 5 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-Tools" %}{% if session.index == 5 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-DevOps" %}{% if session.index == 5 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            3:00 - 3:30
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Breakout / Birds of a Feather
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            3:30 - 4:15
                        </p>
                        <p><i>Session Block 6</i></p>
                    </td>
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-101" %}{% if session.index == 6 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-Tools" %}{% if session.index == 6 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                    {% for session in site.speakers %}
                    {% if session.talk == "PowerShell-DevOps" %}{% if session.index == 6 %}
                    <td>
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <p style="font-weight:700">
                                        {{ session.talk-title }}
                                    </p>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                            </div>
                        </div>
                    </td>
                    {% endif %}{% endif %}
                    {% endfor %}
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            4:30 - 5:00
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Panel Discussion
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            5:00 - 5:15
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Closing / Thank Yous / Raffles
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</div>


<div class="mb-60">&nbsp;</div>

<div class="table-style2">
    <div class="sub-title">
        <span>Sunday Schedule  - 8AM - 3PM</span>
    </div>
    <div class="table-responsive mtb">
        <table class="table table-bordered table-1 table-striped">
            <thead>
                <tr>
                    <td style="width: 25%"></td>
                    <th style="width: 75%">Security Deep Dive</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            8:30 - 9:00
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Breakfast
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            9:00 - 10:15
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Security Session
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            10:15 - 10:30
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Break
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            10:30 - 11:45
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Security Session
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            11:45 - 12:30
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Lunch
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            12:30 - 1:30
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Security Session
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            1:30 - 1:45
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Break
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            1:45 - 2:50
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Security Session
                    </td>
                </tr>
                <tr>
                    <td style="vertical-align: middle">
                        <p style="font-weight:700">
                            2:50 - 3:00
                        </p>
                    </td>
                    <td colspan="3" style="vertical-align: middle">
                        Closing / Thank Yous / Raffles
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</div>