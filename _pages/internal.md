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

{% if site.data.internal.main_folder %}
<div class="internal-main-card">
<h2>{{ site.data.internal.main_folder.title }}</h2>
<p>{{ site.data.internal.main_folder.description }}</p>

{% if site.data.internal.main_folder.url %}
<a href="{{ site.data.internal.main_folder.url }}" target="_blank" rel="noopener noreferrer">Open Internal Drive</a>
{% else %}
<span class="internal-inprep">In preparation</span>
{% endif %}

</div>
{% endif %}

<div class="internal-grid">

{% for item in site.data.internal.resources %}
<div class="internal-card">

<h3>{{ item.title }}</h3>

{% if item.description %}
<p>{{ item.description }}</p>
{% endif %}

{% if item.url %}
<a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">Open Resource</a>
{% else %}
<span class="internal-inprep">In preparation</span>
{% endif %}

</div>
{% endfor %}

</div>

</div>
