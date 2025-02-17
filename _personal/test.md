---
title: "Being a video game completionist &rarr; a better academic?"
collection: personal
permalink: /personal/test
---

<div class="carousel-wrapper">
  <h2>Carousel 1</h2>
  <div class="carousel-container">
    <div class="carousel" id="carousel1">
      <div class="carousel-item">
        <img src="/images/gaming/pokemon_scarlet_paldea.jpg" alt="Carousel 1 Image 1">
        <p class="carousel-caption">Caption for Image 1 in Carousel 1</p>
      </div>
      <div class="carousel-item">
        <img src="/images/gaming/pokemon_scarlet_kitakami.jpg" alt="Carousel 1 Image 2">
        <p class="carousel-caption">Caption for Image 2 in Carousel 1</p>
      </div>
      <div class="carousel-item">
        <img src="/images/gaming/pokemon_scarlet_blueberry.jpg" alt="Carousel 1 Image 3">
        <p class="carousel-caption">Caption for Image 3 in Carousel 1</p>
      </div>
    </div>
    <button class="prev" onclick="moveCarousel('carousel1', -1)">&#10094;</button>
    <button class="next" onclick="moveCarousel('carousel1', 1)">&#10095;</button>
  </div>
</div>

<div class="carousel-wrapper">
  <h2>Carousel 2</h2>
  <div class="carousel-container">
    <div class="carousel" id="carousel2">
      <div class="carousel-item">
        <img src="/images/gaming/crash_4.jpg" alt="Carousel 2 Image 1">
        <p class="carousel-caption">Caption for Image 1 in Carousel 2</p>
      </div>
      <div class="carousel-item">
        <img src="/images/gaming/crash_3.jpg" alt="Carousel 2 Image 2">
        <p class="carousel-caption">Caption for Image 2 in Carousel 2</p>
      </div>
      <div class="carousel-item">
        <img src="/images/gaming/crash_2.jpg" alt="Carousel 2 Image 3">
        <p class="carousel-caption">Caption for Image 3 in Carousel 2</p>
      </div>
    </div>
    <button class="prev" onclick="moveCarousel('carousel2', -1)">&#10094;</button>
    <button class="next" onclick="moveCarousel('carousel2', 1)">&#10095;</button>
  </div>
</div>

<style>
  .carousel-wrapper {
    position: relative;
    width: 80%;
    margin: 0 auto 2rem;
  }
  .carousel-container {
    position: relative;
    overflow: hidden;
    width: 100%;
  }
  .carousel {
    display: flex;
    transition: transform 0.5s ease;
  }
  .carousel-item {
    min-width: 100%;
    box-sizing: border-box;
    position: relative;
  }
  .carousel-item img {
    width: 100%;
    height: auto;
  }
  .carousel-caption {
    position: absolute;
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    background-color: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    font-size: 14px;
  }
  .prev, .next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0,0,0,0.5);
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    z-index: 10;
  }
  .prev { left: 10px; }
  .next { right: 10px; }
</style>

<script>
  function moveCarousel(carouselId, direction) {
    const carousel = document.getElementById(carouselId);
    const items = carousel.querySelectorAll('.carousel-item');
    const totalItems = items.length;
    let currentIndex = parseInt(carousel.dataset.currentIndex) || 0;

    currentIndex = (currentIndex + direction + totalItems) % totalItems;
    carousel.style.transform = `translateX(-${currentIndex * 100}%)`;
    carousel.dataset.currentIndex = currentIndex;
  }
</script>