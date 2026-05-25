---
title: "Internal"
layout: textlay
excerpt: "Cho Lab Internal Resources"
sitemap: false
permalink: /internal/
---

<div class="internal-page">

<h1>{{ site.data.internal.page_title }}</h1>

{% for paragraph in site.data.internal.intro %}
<p>{{ paragraph }}</p>
{% endfor %}

<div class="internal-main-card">
<h2>{{ site.data.internal.main_folder.title }}</h2>
<p>{{ site.data.internal.main_folder.description }}</p>
<a href="{{ site.data.internal.main_folder.url }}" target="_blank" rel="noopener noreferrer">Open Internal Drive</a>
</div>

<div class="internal-grid">

{% for item in site.data.internal.resources %}
<div class="internal-card">
<h3>{{ item.title }}</h3>
<p>{{ item.description }}</p>
<a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">Open Resource</a>
</div>
{% endfor %}

</div>

</div>
