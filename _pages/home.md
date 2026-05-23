---
title: "Cho Lab - Home"
layout: homelay
excerpt: "Creative Nanobiophotonics Laboratory at Rice University"
sitemap: false
permalink: /
---

# Welcome to the Cho Lab

**Creative Nanobiophotonics Laboratory**  
Department of Bioengineering, Rice University

We develop optical nanolaser technologies for single-cell tracking, biological sensing, and dynamic phenotyping.

Our research brings together nanophotonics, bioengineering, optical microscopy, and semiconductor materials to create new tools for understanding complex biological systems. We are particularly interested in using nanolaser particles as optical barcodes and sensors for tracking cellular states, dynamics, and functions.

<!-- Items -->
<div class="carousel-inner" markdown="0">
    <div class="item active">
        <img src="{{ site.url }}{{ site.baseurl }}/images/slider7001400/nanolaser1.jpg" alt="Nanolaser image 1" />
    </div>
    <div class="item">
        <img src="{{ site.url }}{{ site.baseurl }}/images/slider7001400/microscopy1.jpg" alt="Microscopy image" />
    </div>
    <div class="item">
        <img src="{{ site.url }}{{ site.baseurl }}/images/slider7001400/lab1.jpg" alt="Lab image" />
    </div>
</div>

<br>

We are building a research group at Rice University Bioengineering focused on creative nanobiophotonics and translational optical technologies. Our goal is to develop new photonic tools that can read, track, and ultimately help control biological systems at the single-cell scale.

We are looking for passionate postdoctoral fellows, graduate students, undergraduate students, and visiting researchers to join the team. Please see [Openings / Contact]({{ site.url }}{{ site.baseurl }}/openings/) for more information.

<br>

## News

{% for article in site.data.news limit:5 %}
**{{ article.date }}** &nbsp;&nbsp; {{ article.headline }}  
{% endfor %}
