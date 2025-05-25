---
layout: default
title: Feline Friends
permalink: /cats/
description: "Meet my furry companions"
---

<div class="cat-gallery">
  <div class="cat-card">
    <img src="/assets/images/my_cat.jpg" alt="My cat Janush">
    <h3>Yanush</h3>
    <p>The adventurous explorer</p>
  </div>
  
  <!-- Add more cats as needed -->
</div>

<style>
  .cat-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
    margin: 2rem 0;
  }
  .cat-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 8px;
  }
</style>
