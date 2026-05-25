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

<div style="line-height: 1.25;">

{% for item in site.data.pi.previous_positions %}
<p style="margin-top: 0; margin-bottom: 11px;">
<strong>{{ item.year }}</strong> &nbsp;&nbsp; {{ item.text }}
{% if item.note %}
<br>
<span style="display: inline-block; margin-left: 64px; margin-top: 2px; font-size: 0.96em;">{{ item.note }}</span>
{% endif %}
</p>
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

<div style="line-height: 1.25;">

{% for award in site.data.pi.awards %}
<p style="margin-top: 0; margin-bottom: 11px;">
<strong>{{ award.year }}</strong> &nbsp;&nbsp; {{ award.text }}
</p>
{% endfor %}

</div>
