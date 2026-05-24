---
title: "Publications"
layout: textlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

# Publications

[Google Scholar Citations](https://scholar.google.com/citations?hl=en&user=8RNAdMYAAAAJ)

{% assign total = site.data.publications | size %}
{% assign current_year = "" %}

{% for pub in site.data.publications %}

{% if pub.year != current_year %}
{% assign current_year = pub.year %}

---

## {{ current_year }}

{% endif %}

{% assign number = total | minus: forloop.index0 %}

<div class="publication-item" style="margin-bottom: 24px;">

<p>
<strong>{{ number }}. 
{% if pub.link %}
<a href="{{ pub.link }}" target="_blank">{{ pub.title }}</a>
{% else %}
{{ pub.title }}
{% endif %}
</strong><br>

{{ pub.authors }}<br>

<em>{{ pub.journal }}</em>

{% if pub.note %}
<br>{{ pub.note }}
{% endif %}

<br>

{% if pub.pdf %}
<a href="{{ site.url }}{{ site.baseurl }}/{{ pub.pdf }}" target="_blank">PDF</a>
{% endif %}

{% if pub.extra_links %}
{% for extra in pub.extra_links %}
{% if pub.pdf %} | {% endif %}
<a href="{{ extra.url }}" target="_blank">{{ extra.label }}</a>
{% endfor %}
{% endif %}
</p>

</div>

{% endfor %}

---

# US & International Patents

**2. Systems and Methods for Plasmonic Lasers** S. H. Yun, S. Cho.  
2024.

<br>

**1. Perovskite-Based Core-Shell Light-Emitting Structures and Materials, and Methods of Fabrication Thereof** S. H. Yun, S. Cho.  
2019.
