---
layout: default
title: Feline Friends
permalink: /cats/
description: "Meet my furry companions - past and present"
---

<div class="cat-gallery">
  <!-- Yanush - The adventurous explorer -->
  <div class="cat-card">
    <img src="/cats/yanush1.jpg" alt="Yanush the cat">
    <img src="/cats/yanush2.jpg" alt="Yanush playing" class="second-image">
    <h3>Yanush</h3>
    <p>The adventurous explorer</p>
    <div class="status-alive">❤️ Currently brightening our days</div>
  </div>
  
  <!-- Murka - In loving memory -->
  <div class="cat-card memorial">
    <div class="memorial-ribbon">Forever in our hearts</div>
    <img src="/cats/murka.jpg" alt="Murka in her favorite spot" class="second-image">
    <h3>Murka <span class="angel">😇</span></h3>
    <p>Wild and independent spirit</p>
    <div class="status-memorial">🌈 2010 - 2022</div>
  </div>
</div>

<style>
  .cat-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 30px;
    margin: 2rem 0;
  }
  
  .cat-card {
    position: relative;
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
  }
  
  .cat-card:hover {
    transform: translateY(-5px);
  }
  
  .cat-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-bottom: 3px solid #f8f9fa;
  }
  
  .cat-card img.second-image {
    height: 180px;
    border-top: 1px dashed #eee;
  }
  
  .cat-card h3 {
    padding: 15px 15px 5px;
    font-size: 1.5rem;
    color: #333;
  }
  
  .cat-card p {
    padding: 0 15px;
    color: #666;
    font-style: italic;
  }
  
  .status-alive, .status-memorial {
    padding: 10px 15px;
    margin: 10px 15px 15px;
    border-radius: 20px;
    text-align: center;
    font-weight: 500;
  }
  
  .status-alive {
    background-color: #e8f5e9;
    color: #2e7d32;
  }
  
  .status-memorial {
    background-color: #f3e5f5;
    color: #7b1fa2;
  }
  
  .memorial {
    border: 2px solid #e1bee7;
  }
  
  .memorial-ribbon {
    position: absolute;
    top: 10px;
    right: -35px;
    transform: rotate(45deg);
    background: #7b1fa2;
    color: white;
    padding: 5px 40px;
    font-size: 0.8rem;
    z-index: 10;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
  }
  
  .angel {
    font-size: 1.2rem;
  }
  
  @media (max-width: 768px) {
    .cat-gallery {
      grid-template-columns: 1fr;
    }
  }
</style>
