---
title: "PI"
layout: textlay
excerpt: "Principal Investigator"
sitemap: false
permalink: /pi/
---

# Principal Investigator

<div style="display: flex; gap: 28px; align-items: flex-start; flex-wrap: wrap; margin-top: 20px;">

{% if site.data.pi.photo %}
<div style="flex: 0 0 auto;">
<img src="{{ site.url }}{{ site.baseurl }}/{{ site.data.pi.photo }}"
     alt="{{ site.data.pi.name }}"
     style="width: {{ site.data.pi.photo_width | default: '260px' }}; height: auto; border-radius: 6px;">
</div>
{% endif %}

<div style="flex: 1; min-width: 280px;">

## {{ site.data.pi.name }}

**{{ site.data.pi.title }}**  
{{ site.data.pi.department }}  
{{ site.data.pi.institution }}

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

## Biography

{{ site.data.pi.bio | markdownify }}

---

## Previous Employment and Education

{% for item in site.data.pi.previous_positions %}
**{{ item.year }}** &nbsp;&nbsp; {{ item.text }}  
{% endfor %}

{% if site.data.pi.thesis_committee %}
<br>

**Thesis Committee:**  
{% for person in site.data.pi.thesis_committee %}
- {{ person }}
{% endfor %}
{% endif %}

---

## Selected Awards and Honors

{% for award in site.data.pi.awards %}
**{{ award.year }}** &nbsp;&nbsp; {{ award.text }}  
{% endfor %}
