---
title: "Test"
collection: personal
permalink: /personal/test
---

<head>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        /* General Reset */
        * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
        }
        /* Slideshow container */
        .slideshow-container {
        width: 80%;
        max-width: 800px;
        margin: 20px auto;
        position: relative;
        overflow: hidden;
        border-radius: 12px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        background: #fff;
        }
        /* Images */
        .slideshow-container img {
        width: 100%;
        display: block;
        border-radius: 12px;
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
        /* Navigation buttons */
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
        .prev:hover, .next:hover {
        background-color: rgba(255, 255, 255, 0.8);
        color: black;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }
        /* Slide visibility */
        .mySlides1, .mySlides2 {
        display: none;
        }
        /* Responsive */
        @media (max-width: 768px) {
        .prev, .next {
            padding: 10px 15px;
            font-size: 14px;
        }
        }
    </style>
</head>

<body>

<p align="justify">While I cannot claim which direction the causality goes, completing a video game 100% and publishing an academic paper share striking parallels. Both require resilience (gamers: challenging levels, researchers: overcoming rejections), patience (gamers: unlocking achievements, researchers: rewriting and revising), attention to detail (gamers: complex mechanics, researchers: precise writing), and the ability to learn from setbacks (gamers: adapting strategies after failure, researchers: incorporate feedback).</p>

<p align="justify">Below is a list of games I have completed to absolute perfection on Nintendo Switch. You will notice a pattern of game titles that scream nostalgia. My gaming name is DoctorIw, a name I chose when becoming a doctor was still a distant dream.</p>

<h2 align="center">Pokémon games</h2>
<div class="slideshow-container">
  <div class="mySlides1">
    <img src="/images/gaming/crash_1.jpg" alt="Slide 1">
  </div>

  <div class="mySlides1">
    <img src="/images/gaming/crash_2.jpg" alt="Slide 2">
    <div class="carousel-caption">Pokémon Scarlet Paldea Pokédex</div>
  </div>

  <div class="mySlides1">
    <img src="/images/gaming/crash_3.jpg" alt="Slide 3">
  </div>

  <span class="prev" onclick="plusSlides(-1, 0)">&#10094;</span>
  <span class="next" onclick="plusSlides(1, 0)">&#10095;</span>
</div>

<p>Slideshow 2:</p>
<div class="slideshow-container">
  <div class="mySlides2">
    <img src="/images/gaming/pokemon_arceus.jpg" alt="Slide 1">
  </div>

  <div class="mySlides2">
    <img src="/images/gaming/pokemon_lets_go_pikachu.jpg" alt="Slide 2">
  </div>

  <span class="prev" onclick="plusSlides(-1, 0)">&#10094;</span>
  <span class="next" onclick="plusSlides(1, 0)">&#10095;</span>
</div>

<script>
    let slideIndex = [1, 1]; // Add an entry for the more carousel
    let slideId = ["mySlides1", "mySlides2"]; // Can add more mySlides if needed
    showSlides(1, 0); // Initialize the first carousel
    showSlides(1, 1); // Initialize the second carousel
    // showSlides(1, 2); // Initialize the third carousel

    function plusSlides(n, no) {
    showSlides(slideIndex[no] += n, no);
    }

    function showSlides(n, no) {
    let i;
    let x = document.getElementsByClassName(slideId[no]);
    if (n > x.length) {slideIndex[no] = 1}    
    if (n < 1) {slideIndex[no] = x.length}
    for (i = 0; i < x.length; i++) {
        x[i].style.display = "none";  
    }
    x[slideIndex[no]-1].style.display = "block";  
    }
</script>
</body>
