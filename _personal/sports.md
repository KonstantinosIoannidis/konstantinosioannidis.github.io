---
title: "Sports"
collection: personal
permalink: /personal/sports
---

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gaming Achievements Carousel</title>
  <style>
    /* Container for the carousel */
    .carousel-container {
      width: 80%;
      max-width: 800px;
      margin: 0 auto;
      position: relative;
      overflow: hidden;
      border-radius: 10px;
      margin-bottom: 20px;
    }
    /* The slides (images) inside the carousel */
    .carousel-slides {
      display: flex;
      transition: transform 0.5s ease;
    }
    /* Each individual slide */
    .carousel-slide {
      min-width: 100%;
      height: auto;
      position: relative;
    }
    /* Style for captions */
    .carousel-caption {
      text-align: center;
      padding: 10px;
      background-color: rgba(0, 0, 0, 0.6);
      color: white;
      font-size: 16px;
      position: absolute;
      bottom: 0;
      width: 100%;
      box-sizing: border-box;
    }
    /* Navigation buttons (next/previous) */
    .prev, .next {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background-color: rgba(0, 0, 0, 0.5);
      color: white;
      font-size: 18px;
      padding: 10px;
      cursor: pointer;
      z-index: 1;
    }
    .prev {
      left: 10px;
    }
    .next {
      right: 10px;
    }
  </style>
</head>
<body>

<p align="justify">I enjoy running, chess, and football. I mostly run 5k, but I have occasionally attempted 10k. I want to run a half marathon once. You can check my <a href="https://www.parkrun.org.uk/parkrunner/9474117/" target="_blank">Parkrun profile</a>. A longer list of formal running events I have participated in is below.</p>

<ul>
  <li>Netherlands</li>
  <ul>
    <li>
        41<sup>st</sup> Olympisch Stadionloop voor Unicef (5000m, 2018),
        59<sup>th</sup> Middenmeerloop (5000m, 2018),
        83<sup>rd</sup> Sloterplasloop (5000m, 2018),
        Gaasperplasrun (5000m, 2018),
        Uilenstede VU Polderloop (5000m, 2018),
        13<sup>th</sup> Nescioloop (8000m, 2018),
        Gaasperplascross (5000m, 2018),
        Gaasperplasrun (5000m, 2017),
        Hardloopavond4daagse (5000m, 2017),
        12<sup>th</sup> Nescioloop (8000m, 2017),
        40<sup>th</sup> Olympisch Stadionloop voor Unicef (5000m, 2016),
        81<sup>st</sup> Sloterplasloop (5000m, 2016),
        2<sup>nd</sup> De Ijburg Run (5000m, 2016),
        Hardloopavond4daagse (5000m, 2016),
        11<sup>th</sup> Nescioloop (8000m, 2016)</li>
  </ul>
  <li>Greece</li>
  <ul>
    <li>
        Samodolihos (8500m, 2015),
        10<sup>th</sup> International Marathon Alexander The Great (5000m, 2015),
        2<sup>nd</sup> Lykourgos Logothetis Trophy (5000m, 2015),
        3<sup>rd</sup> Samos running (5000m, 2014),
        6th International Marathon Alexander The Great (5000m, 2011)
    </li>
  </ul>
</ul>

<!-- <div class="carousel-container" id="carousel1">
    <div class="carousel-slides">
        <div class="carousel-slide">
            <img src="/images/sports/running_2017.jpg" alt="running_2017" style="width:100%; height:auto;">
            <div class="carousel-caption">Photo Finish Loss (Amsterdam, Netherlands, 9 April, 2017)</div>
        </div>
        <div class="carousel-slide">
            <img src="/images/sports/running_2015.jpg" alt="running_2015" style="width:100%; height:auto;">
            <div class="carousel-caption">Photo Finish Victory (Samos, Greece, 15 March, 2015)</div>
        </div>
    </div>
    <span class="prev" onclick="moveSlide(-1, 'carousel1')">&#10094;</span>
    <span class="next" onclick="moveSlide(1, 'carousel1')">&#10095;</span>
</div> -->

<script>
  // Function to handle slides for any given carousel
  function moveSlide(n, carouselId) {
      const carousel = document.getElementById(carouselId);
      const slides = carousel.querySelectorAll(".carousel-slide");
      let slideIndex = parseInt(carousel.getAttribute("data-slide-index") || 0); // Get the current index

      // Update the index
      slideIndex += n;

      // Ensure the slide index stays within bounds
      if (slideIndex >= slides.length) {
          slideIndex = 0;  // Loop back to first slide
      } else if (slideIndex < 0) {
          slideIndex = slides.length - 1;  // Loop back to last slide
      }

      // Update the carousel's current slide index
      carousel.setAttribute("data-slide-index", slideIndex);

      // Show the corresponding slide
      showSlide(carouselId, slideIndex);
  }

  // Function to display the slide based on the index
  function showSlide(carouselId, slideIndex) {
      const carousel = document.getElementById(carouselId);
      const slides = carousel.querySelectorAll(".carousel-slide");

      // Hide all slides
      slides.forEach(slide => {
          slide.style.display = "none";
      });

      // Show the current slide
      slides[slideIndex].style.display = "block";
  }

  // Initialize the carousels
  document.querySelectorAll(".carousel-container").forEach((carousel, index) => {
      carousel.setAttribute("data-slide-index", 0);  // Set initial slide index to 0
      showSlide(carousel.id, 0);  // Show first slide
  });
</script>

</body>
