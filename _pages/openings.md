---
title: "Openings / Contact"
layout: textlay
excerpt: "Cho Lab: Openings and Contact"
sitemap: false
permalink: /openings/
---

<div class="openings-contact-page">

<div class="openings-top-layout">

<div class="openings-section">

{% for paragraph in site.data.openings.intro %}
<p>{{ paragraph }}</p>
{% endfor %}

<div class="opening-position-list">
{% for position in site.data.openings.positions %}
<div class="opening-position">
<h3>{{ position.title }}</h3>
<p>{{ position.text }}</p>
</div>
{% endfor %}
</div>

<div class="application-section">
<h3>{{ site.data.openings.application.heading }}</h3>

<p>{{ site.data.openings.application.text }}</p>

<ul>
{% for item in site.data.openings.application.materials %}
<li>{{ item }}</li>
{% endfor %}
</ul>

<p>{{ site.data.openings.application.closing }}</p>
</div>

</div>

<div class="openings-side-panel">
{% if site.data.openings.hero_image %}
<div class="openings-hero-square">
<img src="{{ site.url }}{{ site.baseurl }}/images/openings/{{ site.data.openings.hero_image.file }}"
     alt="{{ site.data.openings.hero_image.alt }}">
</div>
{% endif %}
</div>

</div>

<hr style="margin: 42px 0 34px 0; border: 0; border-top: 1px solid #e5e5e5;">

<div class="contact-row">

<div class="contact-text">

<h2>Contact</h2>

<p>
<strong>{{ site.data.openings.contact.name }}</strong><br>
{{ site.data.openings.contact.title }}<br>
{{ site.data.openings.contact.department }}<br>
{{ site.data.openings.contact.institution }}
</p>

<p>
Email: {{ site.data.openings.contact.email }}<br>
Office: {{ site.data.openings.contact.office }}<br>
{{ site.data.openings.contact.location }}
</p>

</div>

<div class="contact-map-box">
<iframe
  src="https://www.google.com/maps?q={{ site.data.openings.map.query | url_encode }}&output=embed"
  width="100%"
  height="100%"
  style="border:0;"
  allowfullscreen=""
  loading="lazy"
  referrerpolicy="no-referrer-when-downgrade">
</iframe>
</div>

</div>

</div>
