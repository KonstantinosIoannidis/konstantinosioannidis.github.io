---
title: "Test"
collection: personal
permalink: /personal/test
---

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Carousels</title>
  <style>
    /* Hide all slides initially */
    .mySlides1, .mySlides2 {
      display: none;
    }
    /* Slideshow container styles */
    .slideshow-container {
      position: relative;
      width: 80%;
      max-width: 800px;
      margin: 0 auto;
      overflow: hidden;
      border-radius: 10px;
    }
    /* Images inside slides */
    .slideshow-container img {
      width: 100%;
      display: block;
    }
    /* Navigation buttons */
    .prev, .next {
      cursor: pointer;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      padding: 10px;
      color: white;
      font-size: 18px;
      background-color: rgba(0, 0, 0, 0.5);
      border-radius: 50%;
      z-index: 1;
    }
    /* Position the buttons */
    .prev {
      left: 10px;
    }
    .next {
      right: 10px;
    }
    /* Responsive: Adjust button size on smaller screens */
    @media (max-width: 768px) {
      .prev, .next {
        padding: 8px;
        font-size: 14px;
      }
    }
  </style>
</head>

<body>
  <h2 align="center">Pokémon games</h2>
  <div class="slideshow-container">
    <div class="mySlides1">
      <img src="/images/gaming/crash_1.jpg" alt="Slide 1">
    </div>
    <div class="mySlides1">
      <img src="/images/gaming/crash_2.jpg" alt="Slide 2">
    </div>
    <div class="mySlides1">
      <img src="/images/gaming/crash_3.jpg" alt="Slide 3">
    </div>
    <span class="prev" onclick="plusSlides(-1, 0)">&#10094;</span>
    <span class="next" onclick="plusSlides(1, 0)">&#10095;</span>
  </div>

  <h2 align="center">Platform games</h2>
  <div class="slideshow-container">
    <div class="mySlides2">
      <img src="/images/gaming/pokemon_arceus.jpg" alt="Slide 1">
    </div>
    <div class="mySlides2">
      <img src="/images/gaming/pokemon_lets_go_pikachu.jpg" alt="Slide 2">
    </div>
    <span class="prev" onclick="plusSlides(-1, 1)">&#10094;</span>
    <span class="next" onclick="plusSlides(1, 1)">&#10095;</span>
  </div>

  <script>
    let slideIndex = [1, 1];
    let slideId = ["mySlides1", "mySlides2"];

    // Initialize carousels
    showSlides(1, 0);
    showSlides(1, 1);

    function plusSlides(n, no) {
      showSlides((slideIndex[no] += n), no);
    }

    function showSlides(n, no) {
      let i;
      let x = document.getElementsByClassName(slideId[no]);
      if (n > x.length) {
        slideIndex[no] = 1;
      }
      if (n < 1) {
        slideIndex[no] = x.length;
      }
      for (i = 0; i < x.length; i++) {
        x[i].style.display = "none";
      }
      x[slideIndex[no] - 1].style.display = "block";
    }

    // Debugging
    console.log("Initializing carousels...");
    console.log(`Carousel 1 has ${document.getElementsByClassName("mySlides1").length} slides.`);
    console.log(`Carousel 2 has ${document.getElementsByClassName("mySlides2").length} slides.`);
</script>
</body>
