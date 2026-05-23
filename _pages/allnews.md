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
<div class="news-images" style="margin-top: 12px;">
{% for img in article.images %}<img src="{{ site.url }}{{ site.baseurl }}/{{ img }}" alt="News image" style="max-width: 31%; width: 31%; margin-right: 1%; margin-bottom: 10px;">{% endfor %}
</div>
{% elsif article.image %}
<div class="news-images" style="margin-top: 12px;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ article.image }}" alt="News image" style="max-width: 500px; width: 100%; margin-bottom: 10px;">
</div>
{% endif %}
{% if article.pdfs %}
<div class="news-pdfs" style="margin-top: 8px;">
{% for pdf in article.pdfs %}<a href="{{ site.url }}{{ site.baseurl }}/{{ pdf }}" target="_blank">View PDF</a><br>{% endfor %}
</div>
{% endif %}
</div>
{% endfor %}
</div>
