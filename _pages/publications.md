---
title: "Publications"
layout: textlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

<div class="publications-page" markdown="1">

<h1 style="font-size: 32px; font-weight: 500; margin-top: 0; margin-bottom: 24px;">Publications</h1>

<p style="margin-top: 5px; margin-bottom: 28px;">
  <a href="https://scholar.google.com/citations?hl=en&user=8RNAdMYAAAAJ"
     target="_blank"
     rel="noopener noreferrer">Google Scholar Citations</a>
</p>

{% if site.data.publications and site.data.publications.size > 0 %}

{% assign total = site.data.publications | size %}
{% assign current_year = "" %}

{% for pub in site.data.publications %}

{% if pub.year != current_year %}
{% assign current_year = pub.year %}

<hr style="margin: 28px 0 24px 0;">

<h2 style="font-size: 32px; margin-top: 0; margin-bottom: 22px;">{{ current_year }}</h2>

{% endif %}

{% assign number = total | minus: forloop.index0 %}

<div class="publication-item" style="margin-bottom: 24px;">

<p style="margin: 0; line-height: 1.35;">
<strong>{{ number }}.
{% if pub.link %}
<a href="{{ pub.link }}"
   target="_blank"
   rel="noopener noreferrer">{{ pub.title }}</a>
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
<a href="{{ site.url }}{{ site.baseurl }}/{{ pub.pdf }}"
   target="_blank"
   rel="noopener noreferrer">PDF</a>
{% endif %}

{% if pub.extra_links %}
{% for extra in pub.extra_links %}
{% if pub.pdf or forloop.index0 > 0 %} | {% endif %}
<a href="{{ extra.url }}"
   target="_blank"
   rel="noopener noreferrer">{{ extra.label }}</a>
{% endfor %}
{% endif %}
</p>

{% if pub.images %}
<div class="publication-images" style="margin-top: 8px; margin-bottom: 4px; display: flex; gap: 12px; align-items: flex-start; flex-wrap: wrap;">
{% for img in pub.images %}
<img src="{{ site.url }}{{ site.baseurl }}/{{ img.path }}"
     alt="{{ img.alt | default: pub.image_alt | default: pub.title | strip_html | escape }}"
     style="height: {{ img.height | default: pub.image_height | default: '150px' }}; width: auto; max-width: {{ img.width | default: pub.image_width | default: '420px' }}; object-fit: contain; border-radius: 4px; margin-top: 0; margin-bottom: 0;">
{% endfor %}
</div>
{% elsif pub.image %}
<div class="publication-image" style="margin-top: 8px; margin-bottom: 4px;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ pub.image }}"
     alt="{{ pub.image_alt | default: pub.title | strip_html | escape }}"
     style="height: {{ pub.image_height | default: '150px' }}; width: auto; max-width: {{ pub.image_width | default: '420px' }}; object-fit: contain; border-radius: 4px; margin-top: 0; margin-bottom: 0;">
</div>
{% endif %}

</div>

{% endfor %}

{% else %}

<p><strong>No publication data found.</strong></p>
<p>Please check that the file exists at <code>_data/publications.yml</code>.</p>

{% endif %}

<hr style="margin: 34px 0 24px 0;">

<h2 style="font-size: 32px; margin-top: 0; margin-bottom: 22px;">US & International Patents</h2>

<div class="publication-item" style="margin-bottom: 24px;">
<p style="margin: 0; line-height: 1.35;">
<strong>2. Systems and Methods for Plasmonic Lasers</strong><br>
S. H. Yun, S. Cho.<br>
2024.
</p>
</div>

<div class="publication-item" style="margin-bottom: 24px;">
<p style="margin: 0; line-height: 1.35;">
<strong>1. Perovskite-Based Core-Shell Light-Emitting Structures and Materials, and Methods of Fabrication Thereof</strong><br>
S. H. Yun, S. Cho.<br>
2019.
</p>
</div>

</div>
