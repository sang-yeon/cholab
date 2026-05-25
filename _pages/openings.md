---
title: "Openings / Contact"
layout: textlay
excerpt: "Cho Lab: Openings and Contact"
sitemap: false
permalink: /openings/
---

<div class="openings-contact-page">

<h1 class="openings-title">
{{ site.data.openings.page_title }}
</h1>

{% if site.data.openings.hero_image %}
<div class="openings-hero">
<img src="{{ site.url }}{{ site.baseurl }}/images/openings/{{ site.data.openings.hero_image.file }}"
     alt="{{ site.data.openings.hero_image.alt }}">
</div>
{% endif %}

<div class="openings-contact-layout">

<div class="openings-section">

<h2>Openings</h2>

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

<div class="contact-section">

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

<div class="contact-map">
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

</div>
