---
title: "Cho Lab - Home"
layout: homelay
excerpt: "Creative Nanobiophotonics Laboratory"
sitemap: false
permalink: /
---

# Welcome to the Creative Nanobiophotonics Laboratory

We are trailblazers on a mission to drive medicine and photonics forward in the service of humanity.

Our current focus is on nanolasers, which hold transformative potential across diverse fields—from high-performance photonic devices to advanced medical discoveries—through their coherence, speed-of-light operation, and multiplexing capability.

<div class="home-carousel-wrapper" markdown="0">

<div id="carouselExample"
     class="carousel slide"
     data-ride="carousel"
     data-interval="3000"
     data-pause="hover">

  <div class="carousel-inner">

    <div class="item active">
      <img src="{{ site.url }}{{ site.baseurl }}/images/main/rice1.jpeg" alt="Rice image 1">
    </div>

    <div class="item">
      <img src="{{ site.url }}{{ site.baseurl }}/images/main/rice2.jpeg" alt="Rice image 2">
    </div>

    <div class="item">
      <img src="{{ site.url }}{{ site.baseurl }}/images/main/rice3.jpeg" alt="Rice image 3">
    </div>

    <div class="item">
      <img src="{{ site.url }}{{ site.baseurl }}/images/main/rice4.jpeg" alt="Rice image 4">
    </div>

  </div>
</div>

<p class="photo-credit">
  Photo credit: Sangyeon Cho
</p>

</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
  var carousel = document.querySelector("#carouselExample");
  if (!carousel) return;

  var items = carousel.querySelectorAll(".item");
  if (items.length === 0) return;

  for (var i = 0; i < items.length; i++) {
    items[i].classList.remove("active");
  }

  var randomIndex = Math.floor(Math.random() * items.length);
  items[randomIndex].classList.add("active");

  if (typeof jQuery !== "undefined" && typeof jQuery.fn.carousel !== "undefined") {
    jQuery("#carouselExample").carousel({
      interval: 3000,
      pause: "hover"
    });
  }
});
</script>
