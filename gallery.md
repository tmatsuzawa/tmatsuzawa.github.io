---
layout: gallery
title: Gallery
permalink: gallery/
body_class: gallery-page
custom_css: css/gallery.css
---
<!-- Container for the image gallery -->
<div class="container">

  <!-- Full-width images with number text -->
  <div class="mySlides">
    <div class="numbertext">1 / 7</div>
      <img src="/images/gallery/1_Confined_Turbulence.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">2 / 7</div>
      <img src="/images/gallery/2_Decay_and_Propagation_of_Turbulence.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">3 / 7</div>
      <img src="/images/gallery/3_Active_Matter.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">4 / 7</div>
      <img src="/images/gallery/4_Vortex_Ring_Collision.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">5 / 7</div>
      <img src="/images/gallery/5_Vortex_Ring_Collision_Symmetric.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">6 / 7</div>
      <img src="/images/gallery/6_Biomolecular_Condensates.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">7 / 7</div>
      <img src="/images/gallery/7_Active_Condensates.png" style="height: 600px;">
  </div>

  <!-- Next and previous buttons -->
  <a class="prev" onclick="plusSlides(-1)">&#6094;</a>
  <a class="next" onclick="plusSlides(1)">&#6095;</a>

  <!-- Image text -->
  <div class="caption-container">
    <p id="caption"></p>
  </div>

  <!-- Thumbnail images -->
  <div class="row">
    <div class="column">
      <img class="demo cursor" src="/images/gallery/1_Confined_Turbulence.png" style="height:100px" onclick="currentSlide(1)" alt="Confined turbulence">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/2_Decay_and_Propagation_of_Turbulence.png" style="height:100px" onclick="currentSlide(2)" alt="Nonlinear diffusion and decay of turbulence">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/3_Active_Matter.png" style="height:100px" onclick="currentSlide(3)" alt="Vortex ring collision">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/4_Vortex_Ring_Collision.png" style="height:100px" onclick="currentSlide(4)" alt="Geometry of vortex ring collisions">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/5_Vortex_Ring_Collision_Symmetric.png" style="height:100px" onclick="currentSlide(5)" alt="Collective dynamics of spinners">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/6_Biomolecular_Condensates.png" style="height:100px" onclick="currentSlide(6)" alt="Dissolving biomolecular condensates">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/7_Active_Condensates.png" style="height:100px" onclick="currentSlide(7)" alt="Enzyme-loaded condensates">
    </div>
  </div>
</div>

<script src="js/gallery.js"></script>
