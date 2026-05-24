---
title: "Cho Lab - Team"
layout: gridlay
excerpt: "Cho Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

**We are looking for motivated PhD students, postdocs, master’s students, and undergraduate researchers to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/openings/) **!**

<br>

{% assign number_printed = 0 %}
{% for member in site.data.team %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix" style="margin-bottom: 34px;">

  <img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.photo }}"
       class="img-responsive"
       width="25%"
       style="float: left; margin: 0 18px 16px 0; border-radius: 8px; box-shadow: none;" />

  <h4 style="margin-top: 0; margin-bottom: 4px;">{{ member.name }}</h4>

  <i>{{ member.info }}</i>

  {% if member.email %}
  <br>
  <span style="font-size: 14px;">Email: {{ member.email }}</span>
  {% endif %}

  <ul style="overflow: hidden; margin-top: 8px; padding-left: 20px; line-height: 1.35;">

    {% if member.number_educ >= 1 and member.education1 %}
    <li>{{ member.education1 | markdownify | remove: '<p>' | remove: '</p>' }}</li>
    {% endif %}

    {% if member.number_educ >= 2 and member.education2 %}
    <li>{{ member.education2 | markdownify | remove: '<p>' | remove: '</p>' }}</li>
    {% endif %}

    {% if member.number_educ >= 3 and member.education3 %}
    <li>{{ member.education3 | markdownify | remove: '<p>' | remove: '</p>' }}</li>
    {% endif %}

    {% if member.number_educ >= 4 and member.education4 %}
    <li>{{ member.education4 | markdownify | remove: '<p>' | remove: '</p>' }}</li>
    {% endif %}

    {% if member.number_educ >= 5 and member.education5 %}
    <li>{{ member.education5 | markdownify | remove: '<p>' | remove: '</p>' }}</li>
    {% endif %}

    {% if member.number_educ >= 6 and member.education6 %}
    <li>{{ member.education6 | markdownify | remove: '<p>' | remove: '</p>' }}</li>
    {% endif %}

    {% if member.number_educ >= 7 and member.education7 %}
    <li>{{ member.education7 | markdownify | remove: '<p>' | remove: '</p>' }}</li>
    {% endif %}

  </ul>

</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
