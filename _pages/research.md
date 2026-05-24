---
title: "Cho Lab - Research"
layout: textlay
excerpt: "Cho Lab -- Research"
sitemap: false
permalink: /research/
---

<div style="text-align: center; margin-top: 10px; margin-bottom: 30px;">
<h1 style="font-weight: 700;">{{ site.data.research.title }}</h1>
</div>

<div style="font-size: 1.25em; line-height: 1.6; margin-bottom: 30px;">
{{ site.data.research.intro | markdownify }}
</div>

{% if site.data.research.image %}
<div style="margin-top: 20px; text-align: center;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ site.data.research.image }}"
     alt="Cho Lab research vision"
     style="width: {{ site.data.research.image_width | default: '100%' }}; max-width: 1100px; height: auto; border-radius: 4px;">
</div>
{% endif %}
