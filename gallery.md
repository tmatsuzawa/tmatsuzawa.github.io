---
layout: gallery
title: Gallery
permalink: gallery/
body_class: gallery-page
custom_css: css/gallery.css
---
<!-- Container for the image gallery -->
<div class="container">

  <!-- Images with number text -->
  <div class="mySlides">
    <div class="numbertext">1 / 8</div>
      <img src="/images/gallery/1_Confined_Turbulence.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">2 / 8</div>
      <img src="/images/gallery/2_Decay_and_Propagation_of_Turbulence.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">3 / 8</div>
      <img src="/images/gallery/3_Active_Matter.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">4 / 8</div>
      <img src="/images/gallery/4_Vortex_Ring_Collision.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">5 / 8</div>
      <img src="/images/gallery/5_Vortex_Ring_Collision_Symmetric.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">6 / 8</div>
      <img src="/images/gallery/6_Biomolecular_Condensates.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">7 / 8</div>
      <img src="/images/gallery/7_Active_Condensates.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">8 / 8</div>
      <video controls style="height: 600px;">
        <source src="/images/gallery/Movie1_Vortex_Ring_Collision.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
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
      <img class="demo cursor" src="/images/gallery/3_Active_Matter.png" style="height:100px" onclick="currentSlide(3)" alt="Collective dynamics of spinning swimmers">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/4_Vortex_Ring_Collision.png" style="height:100px" onclick="currentSlide(4)" alt="Vortex ring collision (3D particle tracking velocimetry)">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/5_Vortex_Ring_Collision_Symmetric.png" style="height:100px" onclick="currentSlide(5)" alt="Symmetric vortex ring collisions (Gross-Pitaevskii simulations)">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/6_Biomolecular_Condensates.png" style="height:100px" onclick="currentSlide(6)" alt="Dissolving biomolecular condensates">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/7_Active_Condensates.png" style="height:100px" onclick="currentSlide(7)" alt="Enzyme-loaded condensates">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/4_Vortex_Ring_Collision.png" style="height:100px" onclick="currentSlide(8)" alt="Vortex ring collision (video)">
    </div>
  </div>
</div>

<script src="js/gallery.js"></script>
