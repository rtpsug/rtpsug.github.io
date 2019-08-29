---
layout: pssat
title : Our Speakers
group : pssaturday-nav
img : pssatTracks.png
img-mobile : pssatTracks.png
author : rtpsug
creator : rtpsug
---
<!-- Content Area Start -->
<div id="content">
  <div class="container">
    <!-- row start -->
    <div class="row">
      <div class="col-md-12">
          <div class="page-header-title">
              <h2 class="heading-title text-center">Our Speakers</h2>
            </div>
          <div class="row">
            <!--START speaker LOOP-->
            {% for speaker in site.speakers %}
            <div class="col-sm-6 col-md-4">
              <!-- speaker Item Starts -->
              <div class="speaker-item">
                <figure class="team-profile">
                  <img src="{{ BASE_PATH }}/assets/images/pssat-speaker/{{ speaker.img }}" alt="">
                  <figcaption class="our-team">
                    <div class="details col-md-12">
                      <p class="content-white">{{ speaker.talk-title }}</p>
                      <hr class="small-divider border-white">
                      <ul class="social-icons text-center">
                        {% if speaker.twitter %}<li><a href="https://twitter.com/{{ speaker.twitter }}"
                            target="_blank" title="@{{ speaker.twitter }}"><i class="fa fa-twitter"
                              aria-hidden="true"></i></a></li>{% endif %}
                        {% if speaker.linkedin %}<li><a
                            href="https://www.linkedin.com/in/{{ speaker.linkedin }}/" target="_blank"
                            title="{{ speaker.linkedin }}"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
                        </li>{% endif %}
                        {% if speaker.website %}<li><a href="{{ speaker.website }}" target="_blank"
                            title="{{ speaker.website }}"><i class="fa fa-cloud" aria-hidden="true"></i></a></li>
                        {% endif %}
                      </ul>
                    </div>
                  </figcaption>
                </figure>
                <div class="info">
                  <h2>
                    {{ speaker.name }}
                  </h2>
                </div>
              </div>
              <!-- Team Item Ends -->
            </div>
            {% endfor %}
            <!--END speaker LOOP-->
          </div>
          <!-- End speaker  01 -->
        </div>
      </div>
    </div>
  </div>
  <!-- Content Area End -->