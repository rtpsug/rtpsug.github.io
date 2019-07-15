---
layout: pssat
title: Event Schedule
tagline: Schedule of Events
group: pssaturday-nav
author : RTPSUG
---
{% include JB/setup %}
<!-- Content Area Start -->
<div id="content">
    <div class="container">
        <div class="row">
            <div class="col-md-12">
                <div class="page-header-title">
                    <h2 class="heading-title text-center">{{ page.title }}</h2>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-md-4 col-sm-6 col-xs-12">
                <div class="features-wrap">

                    <div class="featured-box">
                        <div class="featured-icon">
                            <i class="fa fa-cubes"></i>
                        </div>
                        <div class="featured-content">
                            <h4>Saturday<br>PowerShell 101</h4>
                            <p><i>Intro and Fundamentals</i></p>
                            <br>
                        </div>
                        {% for session in site.speakers %}
                        {% if session.talk == "PowerShell-101" %}
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <a class="panel-title collapsed" data-toggle="collapse"
                                        href="#panel_{{session.talk}}{{session.index}}">
                                        {{ session.talk-title }}
                                    </a>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                                <div id="panel_{{session.talk}}{{session.index}}" class="panel-collapse collapse">
                                    <div class="panel-body text-gray" style="background: white">
                                        {{ session.abstract }}
                                        <br><br>
                                        <div class="speaker-item">
                                            <figure class="team-profile">
                                                <img src="{{ BASE_PATH }}/assets/images/pssat-speaker/{{ session.img }}"
                                                    alt="">
                                            </figure>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <br>
                        {% endif %}
                        {% endfor %}
                    </div>
                </div>
            </div>
            <div class="col-md-4 col-sm-6 col-xs-12">
                <div class="features-wrap">
                    <div class="featured-box">
                        <div class="featured-icon">
                            <i class="fa fa-wrench"></i>
                        </div>
                        <div class="featured-content">
                            <h4>Saturday<br>PowerShell Tools</h4>
                            <p><i>Advanced Scripting and Tools</i></p>
                            <br>
                        </div>
                        {% for session in site.speakers %}
                        {% if session.talk == "PowerShell-Tools" %}
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <a class="panel-title collapsed" data-toggle="collapse"
                                        href="#panel_{{session.talk}}{{session.index}}">
                                        {{ session.talk-title }}
                                    </a>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                                <div id="panel_{{session.talk}}{{session.index}}" class="panel-collapse collapse">
                                    <div class="panel-body text-gray" style="background: white">
                                        {{ session.abstract }}
                                        <br><br>
                                        <div class="speaker-item">
                                            <figure class="team-profile">
                                                <img src="{{ BASE_PATH }}/assets/images/pssat-speaker/{{ session.img }}"
                                                    alt="">
                                            </figure>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <br>
                        {% endif %}
                        {% endfor %}
                    </div>
                </div>
            </div>
            <div class="col-md-4 col-sm-6 col-xs-12">
                <div class="features-wrap">
                    <div class="featured-box">
                        <div class="featured-icon">
                            <i class="fa fa-cogs"></i>
                        </div>
                        <div class="featured-content">
                            <h4>Saturday<br>DevOps & Security</h4>
                            <p><i>DevOps, CI\CD and Security</i></p>
                            <br>
                        </div>
                        {% for session in site.speakers %}
                        {% if session.talk == "PowerShell-DevOps" %}
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <a class="panel-title collapsed" data-toggle="collapse"
                                        href="#panel_{{session.talk}}{{session.index}}">
                                        {{ session.talk-title }}
                                    </a>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                                <div id="panel_{{session.talk}}{{session.index}}" class="panel-collapse collapse">
                                    <div class="panel-body text-gray" style="background: white">
                                        {{ session.abstract }}
                                        <br><br>
                                        <div class="speaker-item">
                                            <figure class="team-profile">
                                                <img src="{{ BASE_PATH }}/assets/images/pssat-speaker/{{ session.img }}"
                                                    alt="">
                                            </figure>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <br>
                        {% endif %}
                        {% endfor %}
                    </div>
                </div>

            </div>
        </div>
        <div class="row">
            <div class="col-md-4 col-md-offset-4 col-sm-6 col-sm-offset-6 col-xs-12">
                <div class="features-wrap">
                    <div class="featured-box">
                        <div class="featured-icon">
                            <i class="fa fa-ticket"></i>
                        </div>
                        <div class="featured-content">
                            <h4>Sunday<br>Security Special</h4>
                            <p><i>Security Practices</i></p>
                            <br>
                        </div>
                        {% for session in site.speakers %}
                        {% if session.talk == "PowerShell-Sunday" %}
                        <div class="panel-group tabbed">
                            <div class="panel">
                                <div class="panel-heading tabbed" style="background: white">
                                    <a class="panel-title collapsed" data-toggle="collapse"
                                        href="#panel_{{session.talk}}{{session.index}}">
                                        {{ session.talk-title }}
                                    </a>
                                    <p style="text-align: right"><i>{{session.name}}</i></p>
                                </div>
                                <div id="panel_{{session.talk}}{{session.index}}" class="panel-collapse collapse">
                                    <div class="panel-body text-gray" style="background: white">
                                        {{ session.abstract }}
                                        <br><br>
                                        <div class="speaker-item">
                                            <figure class="team-profile">
                                                <img src="{{ BASE_PATH }}/assets/images/pssat-speaker/{{ session.img }}"
                                                    alt="">
                                            </figure>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <br>
                        {% endif %}
                        {% endfor %}
                    </div>
                </div>

            </div>
        </div>
    </div>
</div>
<!-- Content Area end -->
