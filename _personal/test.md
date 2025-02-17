---
title: "Being a video game completionist &rarr; a better academic?"
collection: personal
permalink: /personal/test
---

<p align="justify">While I cannot claim which direction the causality goes, completing a video game 100% and publishing an academic paper share striking parallels. Both require resilience (gamers: challenging levels, researchers: overcoming rejections), patience (gamers: unlocking achievements, researchers: rewriting and revising), attention to detail (gamers: complex mechanics, researchers: precise writing), and the ability to learn from setbacks (gamers: adapting strategies after failure, researchers: incorporate feedback).</p>

<p align="justify">Below is a list of games I have completed to absolute perfection on Nintendo Switch. You will notice a pattern of game titles that scream nostalgia. My gaming name is DoctorIw, a name I chose when becoming a doctor was still a distant dream.</p>

<div class="carousel-wrapper">
  <h2 align="center">Pokémon games</h2>
  <div class="carousel-container">
    <div class="carousel" id="carousel1">
      <div class="carousel-item">
        <img src="/images/gaming/pokemon_scarlet_paldea.jpg" alt="Carousel 1 Image 1">
        <p class="carousel-caption">Pokémon Scarlet Paldea Pokédex</p>
      </div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_scarlet_kitakami.jpg" alt="Pokémon Scarlet Kitakami Pokédex">
    <p class="carousel-caption">Pokémon Scarlet Kitakami Pokédex</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_scarlet_blueberry.jpg" alt="Pokémon Scarlet Blueberry Pokédex">
    <p class="carousel-caption">Pokémon Scarlet Blueberry Pokédex</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_arceus.jpg" alt="Pokémon Arceus Pokédex">
    <p class="carousel-caption">Pokémon Arceus Pokédex</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_shield_galar.jpg" alt="Pokémon Shield Galar Pokédex">
    <p class="carousel-caption">Pokémon Shield Galar Pokédex</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_shield_tundra.jpg" alt="Pokémon Shield Tundra Pokédex">
    <p class="carousel-caption">Pokémon Shield Tundra Pokédex</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_shield_armor.jpg" alt="Pokémon Shield Armor Pokédex">
    <p class="carousel-caption">Pokémon Shield Armor Pokédex</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_brilliant_diamond_sinnoh.jpg" alt="Pokémon Brilliant Diamond Sinnoh Pokédex">
    <p class="carousel-caption">Pokémon Brilliant Diamond Sinnoh Pokédex</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_brilliant_diamond_national.jpg" alt="Pokémon Brilliant Diamond National Pokédex">
    <p class="carousel-caption">Pokémon Brilliant Diamond National Pokédex</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/pokemon_lets_go_pikachu.jpg" alt="Pokémon Let's Go Pokédex">
    <p class="carousel-caption">Pokémon Let's Go Pikachu Pokédex</p>
</div>
    </div>
    <button class="prev" onclick="moveCarousel('carousel1', -1)">&#10094;</button>
    <button class="next" onclick="moveCarousel('carousel1', 1)">&#10095;</button>
  </div>
</div>

<div class="carousel-wrapper">
  <h2 align="center">Platform Games</h2>
  <div class="carousel-container">
    <div class="carousel" id="carousel2">
<div class="carousel-item">
    <img src="/images/gaming/crash_4.jpg" alt="Crash Bandicoot 4: It's About Time">
    <p class="carousel-caption">Crash Bandicoot 4: It's About Time</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/crash_3.jpg" alt="Crash Bandicoot 3: Warped">
    <p class="carousel-caption">Crash Bandicoot 3: Warped</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/crash_2.jpg" alt="Crash Bandicoot 2: Cortex Strikes Back">
    <p class="carousel-caption">Crash Bandicoot 2: Cortex Strikes Back</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/crash_1.jpg" alt="Crash Bandicoot">
    <p class="carousel-caption">Crash Bandicoot</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/spyro.jpg" alt="Spyro Reignited Trilogy">
    <p class="carousel-caption">Spyro Reignited Trilogy</p>
</div>
<div class="carousel-item">
    <img src="/images/gaming/super_mario_world.jpg" alt="Super Mario World">
    <p class="carousel-caption">Super Mario World</p>
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