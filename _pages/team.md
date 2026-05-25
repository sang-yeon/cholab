---
title: "Cho Lab - Team"
layout: gridlay
excerpt: "Cho Lab: Team members"
sitemap: false
permalink: /team/
---

<div class="team-intro">
<p>
The Cho Lab is a collaborative team dedicated to developing creative tools that advance science and benefit society. We value openness, respect, curiosity, and the joy of discovery. Our priority is to help every lab member grow, succeed, and thrive as a scientist, engineer, and person.
</p>
</div>

<h1 class="team-heading">Group Members</h1>

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row team-row">
{% endif %}

<div class="col-sm-6 clearfix team-member-card">
<div class="team-member-inner">

<div class="team-photo-wrap">
{% if member.hover_photo %}
<img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.photo }}"
     data-hover="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.hover_photo }}"
     data-original="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.photo }}"
     data-locked="false"
     class="img-responsive team-photo-img"
     alt="{{ member.name }}"
     style="object-position: {{ member.photo_position | default: 'center center' }} !important;" />

<button type="button" class="team-photo-toggle">Alt</button>

{% else %}
<img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.photo }}"
     class="img-responsive team-photo-img"
     alt="{{ member.name }}"
     style="object-position: {{ member.photo_position | default: 'center center' }} !important;" />
{% endif %}
</div>

<div class="team-member-text">

<h4>{{ member.name }}</h4>

<div class="team-member-role">
<i>{{ member.info }}</i>
</div>

{% if member.email %}
<div class="team-member-email">
Email: {{ member.email }}
</div>
{% endif %}

<ul>
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

</div>
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

<script>
document.addEventListener("DOMContentLoaded", function () {
  var photos = document.querySelectorAll(".team-photo-img[data-hover]");

  photos.forEach(function (photo) {
    photo.addEventListener("mouseenter", function () {
      if (photo.getAttribute("data-locked") !== "true") {
        photo.src = photo.getAttribute("data-hover");
      }
    });

    photo.addEventListener("mouseleave", function () {
      if (photo.getAttribute("data-locked") !== "true") {
        photo.src = photo.getAttribute("data-original");
      }
    });
  });

  var buttons = document.querySelectorAll(".team-photo-toggle");

  buttons.forEach(function (button) {
    button.addEventListener("click", function () {
      var wrap = button.closest(".team-photo-wrap");
      var photo = wrap.querySelector(".team-photo-img[data-hover]");

      if (!photo) return;

      var isLocked = photo.getAttribute("data-locked") === "true";

      if (isLocked) {
        photo.src = photo.getAttribute("data-original");
        photo.setAttribute("data-locked", "false");
        button.textContent = "Alt";
      } else {
        photo.src = photo.getAttribute("data-hover");
        photo.setAttribute("data-locked", "true");
        button.textContent = "Original";
      }
    });
  });
});
</script>
