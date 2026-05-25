---
title: "Research"
layout: textlay
excerpt: "Cho Lab: Research"
sitemap: false
permalink: /research/
---

<div class="research-page">

<h1 class="research-title">
{{ site.data.research.page_title }}
</h1>

<h2 class="research-intro-title">
{{ site.data.research.intro_title }}
</h2>

{% for paragraph in site.data.research.intro_text %}
<p class="research-intro-text">{{ paragraph }}</p>
{% endfor %}

{% for section in site.data.research.sections %}

<div class="research-section">

<div class="research-text">

<h2>{{ section.question }}</h2>

{% for paragraph in section.text %}
<p>{{ paragraph }}</p>
{% endfor %}

</div>

{% if section.image %}
<div class="research-image-wrap">
<img src="{{ site.url }}{{ site.baseurl }}/images/research/{{ section.image }}"
     alt="{{ section.image_alt }}"
     class="research-image">
</div>
{% endif %}

</div>

{% endfor %}

</div>
