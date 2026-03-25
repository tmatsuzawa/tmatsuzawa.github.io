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
    <div class="numbertext">1 / 16</div>
      <img src="/images/gallery/1_Confined_Turbulence.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">2 / 16</div>
      <img src="/images/gallery/2_Decay_and_Propagation_of_Turbulence.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">3 / 16</div>
      <img src="/images/gallery/3_Active_Matter.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">4 / 16</div>
      <video controls style="height: 600px;">
        <source src="/images/gallery/Movie1_Vortex_Ring_Collision.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
  </div>

  <div class="mySlides">
    <div class="numbertext">5 / 16</div>
      <video controls style="height: 600px;">
        <source src="/images/gallery/Movie4_Vortex_Ring_Collision_Symmetric.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
  </div>

  <div class="mySlides">
    <div class="numbertext">6 / 16</div>
      <img src="/images/gallery/6_Biomolecular_Condensates.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">7 / 16</div>
      <img src="/images/gallery/7_Active_Condensates.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">8 / 16</div>
      <img src="/images/gallery/8_Turbulent_Blob.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">9 / 16</div>
      <img src="/images/gallery/9_Turbulent_Blob_Enstrophy.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">10 / 16</div>
      <img src="/images/gallery/10_Turbulence1.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">11 / 16</div>
      <img src="/images/gallery/11_Turbulence2.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">12 / 16</div>
      <img src="/images/gallery/12_Turbulence3.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">13 / 16</div>
      <img src="/images/gallery/13_Turbulence4.png" style="height: 600px;">
  </div>

  <div class="mySlides">
    <div class="numbertext">14 / 16</div>
      <video controls style="height: 600px;">
        <source src="/images/gallery/Movie2_3D_PTV.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
  </div>

  <div class="mySlides">
    <div class="numbertext">15 / 16</div>
      <video controls style="height: 600px;">
        <source src="/images/gallery/Movie3_3D_Energy.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
  </div>

  <div class="mySlides">
    <div class="numbertext">16 / 16</div>
      <video controls style="height: 600px;">
        <source src="/images/gallery/Movie5_flowtrace_highRe_blob.mp4" type="video/mp4">
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
      <img class="demo cursor" src="/images/gallery/4_Vortex_Ring_Collision.png" style="height:100px" onclick="currentSlide(4)" alt="Vortex ring collision (3D particle tracking velocimetry, video)">
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
      <img class="demo cursor" src="/images/gallery/8_Turbulent_Blob.png" style="height:100px" onclick="currentSlide(8)" alt="Turbulent blob">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/9_Turbulent_Blob_Enstrophy.png" style="height:100px" onclick="currentSlide(9)" alt="Enstrophy of a turbulent blob">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/10_Turbulence1.png" style="height:100px" onclick="currentSlide(10)" alt="Pathlines in turbulent flows 1">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/11_Turbulence2.png" style="height:100px" onclick="currentSlide(11)" alt="Pathlines in turbulent flows 2">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/12_Turbulence3.png" style="height:100px" onclick="currentSlide(12)" alt="Pathlines in turbulent flows 3">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/13_Turbulence4.png" style="height:100px" onclick="currentSlide(13)" alt="Pathlines in turbulent flows 4">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/14_Movie2_Thumbnail.png" style="height:100px" onclick="currentSlide(14)" alt="Pathline visualization of a turbulent blob(video)">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/15_Movie3_Thumbnail.png" style="height:100px" onclick="currentSlide(15)" alt="Energy decomposition of a turbulent blob (video)">
    </div>
    <div class="column">
      <img class="demo cursor" src="/images/gallery/16_Movie5_Thumbnail.png" style="height:100px" onclick="currentSlide(16)" alt="One-shot movie of decat of turbulence (video)">
    </div>
  </div>
</div>

<script src="js/gallery.js"></script>
