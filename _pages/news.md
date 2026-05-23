---
title: "News"
layout: textlay
excerpt: "News"
sitemap: false
permalink: /news/
---

# News

<div class="news-list">
{% for article in site.data.news %}
<div class="news-item" style="margin-bottom: 35px;">

<p><strong>{{ article.date }}</strong> &nbsp; {{ article.headline }}</p>

{% if article.images %}
<div class="news-images" style="margin-top: 12px; display: flex; gap: 14px; align-items: flex-start; flex-wrap: wrap; justify-content: flex-start;">
{% for img in article.images %}
<img src="{{ site.url }}{{ site.baseurl }}/{{ img.path }}" 
     alt="News image" 
     style="max-width: {{ img.width | default: '320px' }}; width: auto; height: auto; object-fit: contain; margin-bottom: 10px;">
{% endfor %}
</div>

{% elsif article.image %}
<div class="news-images" style="margin-top: 12px;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ article.image }}" 
     alt="News image" 
     style="max-width: {{ article.width | default: '500px' }}; width: auto; height: auto; margin-bottom: 10px;">
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
