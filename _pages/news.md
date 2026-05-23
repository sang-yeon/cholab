---
title: "News"
layout: textlay
excerpt: "News"
sitemap: false
permalink: /news/
---

<h1>News</h1>

<div class="news-list">
{% for article in site.data.news %}
<div class="news-item" style="margin-bottom: 35px;">

<p><strong>{{ article.date }}</strong> &nbsp; {{ article.headline }}</p>

{% if article.images %}
<div class="news-images" style="margin-top: 12px; display: flex; flex-wrap: wrap; gap: 10px; align-items: flex-start;">
{% for img in article.images %}
<img src="{{ site.url }}{{ site.baseurl }}/{{ img.path }}" alt="News image" style="height: 220px; width: auto; object-fit: contain;">
{% endfor %}
</div>
{% elsif article.image %}
<div class="news-images" style="margin-top: 12px;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ article.image }}" alt="News image" style="max-width: {{ article.width | default: '500px' }}; width: auto; height: auto;">
</div>
{% endif %}

{% if article.pdfs %}
<div class="news-pdfs" style="margin-top: 8px;">
{% for pdf in article.pdfs %}
<a href="{{ site.url }}{{ site.baseurl }}/{{ pdf }}" target="_blank">View PDF</a><br>
{% endfor %}
</div>
{% endif %}

</div>
{% endfor %}
</div>
