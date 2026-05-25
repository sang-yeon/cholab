---
title: "PI"
layout: textlay
excerpt: "Principal Investigator"
sitemap: false
permalink: /pi/
---

<h1 style="font-size: 28px; font-weight: 500; margin-bottom: 28px;">Principal Investigator</h1>

<div style="display: flex; gap: 28px; align-items: flex-start; flex-wrap: wrap; margin-top: 20px; margin-bottom: 44px;">

{% if site.data.pi.photo %}
<div style="flex: 0 0 auto;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ site.data.pi.photo }}"
     alt="{{ site.data.pi.name }}"
     style="width: {{ site.data.pi.photo_width | default: '260px' }}; height: auto; border-radius: 6px; display: block; margin: 0 !important; padding: 0 !important;">
</div>
{% endif %}

<div style="flex: 1; min-width: 280px; padding-top: 0;">

<h2 style="font-size: 28px; font-weight: 500; margin-top: 0; margin-bottom: 16px; line-height: 1.2;">
{{ site.data.pi.name }}
</h2>

**{{ site.data.pi.title }}**  
{{ site.data.pi.department }}  
{{ site.data.pi.institution }}

<br>

Email: {{ site.data.pi.email }}  
Office: {{ site.data.pi.office }}

{% if site.data.pi.links %}
<p>
{% for item in site.data.pi.links %}
<a href="{% if item.url contains 'http' %}{{ item.url }}{% else %}{{ site.url }}{{ site.baseurl }}{{ item.url }}{% endif %}" target="_blank">{{ item.label }}</a>{% unless forloop.last %} | {% endunless %}
{% endfor %}
</p>
{% endif %}

</div>
</div>

---

<h2 style="font-size: 28px; font-weight: 500; margin-top: 28px; margin-bottom: 18px;">Previous Employment and Education</h2>

<div style="line-height: 1.22;">

{% for item in site.data.pi.previous_positions %}
<div style="display: flex; align-items: flex-start; gap: 16px; margin-bottom: 9px;">
  <div style="flex: 0 0 115px; font-weight: 700;">{{ item.year }}</div>
  <div style="flex: 1;">
    <div>{{ item.text }}</div>
    {% if item.note %}
    <div style="margin-top: 1px; font-size: 0.96em;">{{ item.note }}</div>
    {% endif %}
  </div>
</div>
{% endfor %}

</div>

{% if site.data.pi.thesis_committee %}
<br>

**Thesis Committee:**  
{% for person in site.data.pi.thesis_committee %}
- {{ person }}
{% endfor %}
{% endif %}

---

<h2 style="font-size: 28px; font-weight: 500; margin-top: 28px; margin-bottom: 18px;">Selected Awards and Honors</h2>

<div style="line-height: 1.22;">

{% for award in site.data.pi.awards %}
<div style="display: flex; align-items: flex-start; gap: 16px; margin-bottom: 9px;">
  <div style="flex: 0 0 48px; font-weight: 700;">{{ award.year }}</div>
  <div style="flex: 1;">{{ award.text }}</div>
</div>
{% endfor %}

</div>

{% if site.data.pi.marathon %}
---

<h2 style="font-size: 28px; font-weight: 500; margin-top: 28px; margin-bottom: 18px;">Marathon</h2>

<div style="display: flex; gap: 28px; align-items: flex-start; flex-wrap: wrap; line-height: 1.35;">

{% if site.data.pi.marathon.photo %}
<div style="flex: 0 0 auto;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ site.data.pi.marathon.photo }}"
     alt="Professor Cho marathon photo"
     style="width: {{ site.data.pi.marathon.photo_width | default: '260px' }}; max-width: 100%; height: auto; border-radius: 6px; display: block; margin: 0 !important; padding: 0 !important;">
</div>
{% endif %}

<div style="flex: 1; min-width: 280px;">

{% if site.data.pi.marathon.quote %}
<p style="margin-top: 0; margin-bottom: 14px; font-style: italic;">
“{{ site.data.pi.marathon.quote }}” — {{ site.data.pi.marathon.quote_author }}, <em>{{ site.data.pi.marathon.quote_book }}</em>
</p>
{% endif %}

{% for paragraph in site.data.pi.marathon.text %}
<p style="margin-top: 0; margin-bottom: 10px;">
{{ paragraph }}
</p>
{% endfor %}

</div>
</div>
{% endif %}
