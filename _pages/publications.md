---
title: "Publications"
layout: textlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

# Publications

[Google Scholar Citations](https://scholar.google.com/citations?hl=en&user=8RNAdMYAAAAJ)

{% if site.data.publications and site.data.publications.size > 0 %}

{% assign total = site.data.publications | size %}
{% assign current_year = "" %}

{% for pub in site.data.publications %}

{% if pub.year != current_year %}
{% assign current_year = pub.year %}

---

## {{ current_year }}

{% endif %}

{% assign number = total | minus: forloop.index0 %}

<div class="publication-item" style="margin-bottom: 36px;">

<p style="margin: 0;">
<strong>{{ number }}.
{% if pub.link %}
<a href="{{ pub.link }}" target="_blank">{{ pub.title }}</a>
{% else %}
{{ pub.title }}
{% endif %}
</strong><br>

{{ pub.authors }}<br>

{% if pub.journal_name %}
<strong><em>{{ pub.journal_name }}</em></strong>{% if pub.journal_info %} <em>{{ pub.journal_info }}</em>{% endif %}
{% else %}
<em>{{ pub.journal }}</em>
{% endif %}

{% if pub.note %}
<br>{{ pub.note }}
{% endif %}

{% if pub.pdf or pub.extra_links %}
<br>
{% endif %}

{% if pub.pdf %}
<a href="{{ site.url }}{{ site.baseurl }}/{{ pub.pdf }}" target="_blank">PDF</a>
{% endif %}

{% if pub.extra_links %}
{% for extra in pub.extra_links %}
{% if pub.pdf or forloop.index0 > 0 %} | {% endif %}
<a href="{{ extra.url }}" target="_blank">{{ extra.label }}</a>
{% endfor %}
{% endif %}
</p>

{% if pub.image %}
<div class="publication-image" style="margin-top: 12px;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ pub.image }}"
     alt="Publication image"
     style="height: {{ pub.image_height | default: '160px' }}; width: auto; max-width: {{ pub.image_width | default: '280px' }}; object-fit: contain; border-radius: 4px;">
</div>
{% endif %}

</div>

{% endfor %}

{% else %}

<p><strong>No publication data found.</strong></p>
<p>Please check that the file exists at <code>_data/publications.yml</code>.</p>

{% endif %}

---

# US & International Patents

**2. Systems and Methods for Plasmonic Lasers**  
S. H. Yun, S. Cho.  
2024.

<br>

**1. Perovskite-Based Core-Shell Light-Emitting Structures and Materials, and Methods of Fabrication Thereof**  
S. H. Yun, S. Cho.  
2019.
