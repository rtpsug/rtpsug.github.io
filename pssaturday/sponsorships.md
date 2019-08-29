---
layout: pssat
title: Become A Sponsor
group: pssaturday-sponsor-drop-nav
img : pssaturday.png
img-mobile : pssaturday.png
author : rtpsug
creator : rtpsug
---
{% include JB/setup %}
<!-- Content Area Start -->
<div id="content">
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="page-header-title">
          <h2 class="heading-title text-center">Sponsorships</h2>
        </div>
      </div>
    </div>
    <div class="row">
        <div class="col-md-12">
            <p class="text-success" style="text-align: center"><a href="https://drive.google.com/file/d/1z4fu7oUUK_5yFX_dWZwp0gIJx-y9Q-nq/view?usp=sharing" target="_blank"><strong>Download Sponsorship Packages</strong></a></p>
          </div>
    </div>
    <div class="row">
      {% for sponsorship in site.sponsorships %}
      <!-- Pricing Start 01 -->
      <div class="col-md-4 col-sm-6 col-xs-12">
        <div class="pricing-table-block">
          <div class="plan-name">
            <h3>
              {{ sponsorship.name }}
            </h3>
            <h6>
                {{ sponsorship.caption }}
            </h6>
          </div>
          <div class="plan-price">
              <div class="price-value">$ {{ sponsorship.cost }}</div>
          </div>
          <div class="plan-list">
              <ul>
                  {% if sponsorship.detail1 %}
                  <li><i class="fa fa-check"></i>{{ sponsorship.detail1 }}</li>
                  {% endif %}
                  {% if sponsorship.detail2 %}
                  <li><i class="fa fa-check"></i>{{ sponsorship.detail2 }}</li>
                  {% endif %}
                  {% if sponsorship.detail3 %}
                  <li><i class="fa fa-check"></i>{{ sponsorship.detail3 }}</li>
                  {% endif %}
                  {% if sponsorship.detail4 %}
                  <li><i class="fa fa-check"></i>{{ sponsorship.detail4 }}</li>
                  {% endif %}
                  {% if sponsorship.detail5 %}
                  <li><i class="fa fa-check"></i>{{ sponsorship.detail5 }}</li>
                  {% endif %}
                  {% if sponsorship.detail6 %}
                  <li><i class="fa fa-check"></i>{{ sponsorship.detail6 }}</li>
                  {% endif %}
                </ul>
          </div>
        </div>
      </div>
      <!-- Pracing End 01 -->
      {% endfor %}
    </div>
  </div>
</div>

<div class="mb-60"></div>



<!-- Content Area End -->