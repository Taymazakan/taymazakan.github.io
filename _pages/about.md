---
permalink: /
title: "Taymaz Akan, PhD"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a postdoctoral fellow at Louisiana State University Health Sciences Center (LSUHSC), where I focus on deep learning, medical image analysis, and clinical AI applications. I earned my Ph.D. in Computer Engineering from Gazi University (Turkey), where I developed a fully automatic color image segmentation algorithm using multimodal optimization techniques. Prior to LSUHSC, I completed a postdoctoral research appointment at the University of Pardubice (Czech Republic), working on classification and localization systems. My research interests span video transformers for 3D medical imaging, topological data analysis, and metaheuristic optimization. I have published extensively, served as associate editor and reviewer for international journals, and held visiting academic positions across Europe.

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Featured Publications</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    #featured-publications {
      max-width: 900px;
      margin: 60px auto;
      text-align: center;
    }

    h2 {
      font-size: 1.6em;
      margin-bottom: 30px;
    }

    .carousel-container {
      position: relative;
      width: 100%;
      max-width: 750px;
      margin: 0 auto;
      padding: 0 50px;
    }

    .carousel-track {
      overflow: hidden;
      padding: 20px 0;
    }

    .carousel-slides {
      display: flex;
      transition: transform 0.5s ease;
    }

    .carousel-slide {
      min-width: 33.333%;
      padding: 0 10px;
      display: flex;
      justify-content: center;
    }

    .carousel-slide img {
      width: 210px;
      height: 280px;
      border-radius: 10px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.15);
      transition: transform 0.3s ease;
    }

    .carousel-slide img:hover {
      transform: scale(1.05);
    }

    .arrow {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 40px;
      height: 40px;
      background: rgba(255, 255, 255, 0.9);
      border: 1px solid #ddd;
      border-radius: 50%;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 10;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }

    .arrow:hover {
      background: white;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    }

    .arrow-left {
      left: 0;
    }

    .arrow-right {
      right: 0;
    }

    .dots {
      display: flex;
      justify-content: center;
      gap: 10px;
      margin-top: 20px;
    }

    .dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: #ccc;
      cursor: pointer;
      transition: background 0.3s;
    }

    .dot.active {
      background: #58a6ff;
    }
  </style>
</head>
<body>

<section id="featured-publications">
  <h2>Featured Publications</h2>
  
  <div class="carousel-container">
    <button class="arrow arrow-left" onclick="moveCarousel(-1)">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <polyline points="15 18 9 12 15 6"></polyline>
      </svg>
    </button>

    <div class="carousel-track">
      <div class="carousel-slides" id="slides">
        <div class="carousel-slide">
          <a href="https://www.sciencedirect.com/science/article/pii/S0306452225009108?ssrnid=5276922&dgcid=SSRN_redirect_SD" target="_blank">
            <img src="/images/papers/Alzhformer.png" alt="AlzhFormer">
          </a>
        </div>
        <div class="carousel-slide">
          <a href="https://www.nature.com/articles/s41598-024-59578-3" target="_blank">
            <img src="/images/papers/JointTransformer.png" alt="JointTransformer">
          </a>
        </div>
        <div class="carousel-slide">
          <a href="https://www.sciencedirect.com/science/article/pii/S0022510X25003557" target="_blank">
            <img src="/images/papers/NeuroDeepReview.png" alt="NeuroDeepReview">
          </a>
        </div>
        <div class="carousel-slide">
          <a href="https://link.springer.com/article/10.1007/s10278-024-01336-y" target="_blank">
            <img src="/images/papers/ViViEchoformer.png" alt="ViViEchoformer">
          </a>
        </div>
      </div>
    </div>

    <button class="arrow arrow-right" onclick="moveCarousel(1)">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <polyline points="9 18 15 12 9 6"></polyline>
      </svg>
    </button>
  </div>

  <div class="dots">
    <span class="dot active" onclick="goToSlide(0)"></span>
    <span class="dot" onclick="goToSlide(1)"></span>
  </div>
</section>

<script>
let currentPosition = 0;
const totalPages = 2;
const slides = document.getElementById('slides');
const dots = document.querySelectorAll('.dot');

function updateCarousel() {
  const offset = currentPosition * -33.333;
  slides.style.transform = `translateX(${offset}%)`;
  
  dots.forEach((dot, index) => {
    dot.classList.toggle('active', index === currentPosition);
  });
}

function moveCarousel(direction) {
  currentPosition += direction;
  if (currentPosition < 0) currentPosition = totalPages - 1;
  if (currentPosition >= totalPages) currentPosition = 0;
  updateCarousel();
}

function goToSlide(index) {
  currentPosition = index;
  updateCarousel();
}

// Auto-advance every 5 seconds
setInterval(() => {
  moveCarousel(1);
}, 5000);
</script>

</body>
</html>
