---
permalink: /
title: "Taymaz Akan, PhD"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a postdoctoral fellow at Louisiana State University Health Sciences Center (LSUHSC), where I focus on deep learning, medical image analysis, and clinical AI applications. I earned my Ph.D. in Computer Engineering from Gazi University (Turkey), where I developed a fully automatic color image segmentation algorithm using multimodal optimization techniques. Prior to LSUHSC, I completed a postdoctoral research appointment at the University of Pardubice (Czech Republic), working on classification and localization systems. My research interests span video transformers for 3D medical imaging, topological data analysis, and metaheuristic optimization. I have published extensively, served as associate editor and reviewer for international journals, and held visiting academic positions across Europe.


<section id="featured-publications" style="text-align:center; margin: 60px 0;">
  <h2>Featured Publications</h2>
  <div class="pub-carousel">
    <button class="arrow arrow-left" aria-label="Previous">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="15 18 9 12 15 6"></polyline>
      </svg>
    </button>
    
    <div class="slides">
      <div class="slide">
        <a href="https://www.sciencedirect.com/science/article/pii/S0306452225009108?ssrnid=5276922&dgcid=SSRN_redirect_SD" target="_blank">
          <img src="/images/papers/Alzhformer.png" alt="AlzhFormer">
        </a>
      </div>
      <div class="slide">
        <a href="https://www.nature.com/articles/s41598-024-59578-3" target="_blank">
          <img src="/images/papers/JointTransformer.png" alt="JointTransformer">
        </a>
      </div>
      <div class="slide">
        <a href="https://www.sciencedirect.com/science/article/pii/S0022510X25003557" target="_blank">
          <img src="/images/papers/NeuroDeepReview.png" alt="NeuroDeepReview">
        </a>
      </div>
      <div class="slide">
        <a href="https://link.springer.com/article/10.1007/s10278-024-01336-y" target="_blank">
          <img src="/images/papers/ViViEchoformer.png" alt="ViViEchoformer">
        </a>
      </div>
    </div>
    
    <button class="arrow arrow-right" aria-label="Next">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="9 18 15 12 9 6"></polyline>
      </svg>
    </button>
    
    <div class="dots">
      <span class="dot active"></span>
      <span class="dot"></span>
    </div>
  </div>
</section>

<style>
#featured-publications {
  max-width: 1000px;
  margin: 0 auto;
}

.pub-carousel {
  position: relative;
  overflow: hidden;
  padding: 0 60px;
}

.slides {
  display: flex;
  transition: transform 0.6s ease;
  gap: 20px;
}

.slide {
  flex: 0 0 calc(33.33% - 14px);
  display: flex;
  justify-content: center;
  align-items: center;
}

.slide img {
  width: 210px;
  height: 285px;
  border-radius: 10px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.15);
  transition: transform 0.3s ease;
}

.slide img:hover {
  transform: scale(1.05);
}

.arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(255, 255, 255, 0.9);
  border: 1px solid #ddd;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  z-index: 10;
  transition: all 0.3s ease;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.arrow:hover {
  background-color: #fff;
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.arrow svg {
  color: #333;
}

.arrow-left {
  left: 0;
}

.arrow-right {
  right: 0;
}

.dots {
  text-align: center;
  margin-top: 15px;
}

.dot {
  height: 10px;
  width: 10px;
  margin: 0 5px;
  background-color: #ccc;
  border-radius: 50%;
  display: inline-block;
  cursor: pointer;
  transition: background-color 0.3s;
}

.dot.active {
  background-color: #58a6ff;
}

h2 {
  font-size: 1.6em;
  margin-bottom: 20px;
}
</style>

<script>
const slidesContainer = document.querySelector('.slides');
const dots = document.querySelectorAll('.dot');
const arrowLeft = document.querySelector('.arrow-left');
const arrowRight = document.querySelector('.arrow-right');

let currentIndex = 0;
const slidesPerView = 3;
const totalSlides = document.querySelectorAll('.slide').length;
const totalPages = Math.ceil(totalSlides / slidesPerView);

function showSlides(index) {
  const offset = index * (100 / totalPages);
  slidesContainer.style.transform = `translateX(-${offset}%)`;
  dots.forEach((dot, i) => dot.classList.toggle('active', i === index));
}

function nextSlide() {
  currentIndex = (currentIndex + 1) % totalPages;
  showSlides(currentIndex);
}

function prevSlide() {
  currentIndex = (currentIndex - 1 + totalPages) % totalPages;
  showSlides(currentIndex);
}

// Arrow click handlers
arrowLeft.addEventListener('click', prevSlide);
arrowRight.addEventListener('click', prevSlide);

// Dot click handlers
dots.forEach((dot, i) => {
  dot.addEventListener('click', () => {
    currentIndex = i;
    showSlides(currentIndex);
  });
});

// Auto slide every 5 seconds
setInterval(() => {
  currentIndex = (currentIndex + 1) % totalPages;
  showSlides(currentIndex);
}, 5000);
</script>
