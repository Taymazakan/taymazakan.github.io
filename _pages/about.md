---
permalink: /
title: "Taymaz Akan, PhD"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a postdoctoral fellow at Louisiana State University Health Sciences Center (LSUHSC), where I focus on deep learning, medical image analysis, and clinical AI applications. I earned my Ph.D. in Computer Engineering from Gazi University (Turkey), where I developed a fully automatic color image segmentation algorithm using multimodal optimization techniques. Prior to LSUHSC, I completed a postdoctoral research appointment at the University of Pardubice (Czech Republic), working on classification and localization systems. My research interests span video transformers for 3D medical imaging, topological data analysis, and metaheuristic optimization. I have published extensively, served as associate editor and reviewer for international journals, and held visiting academic positions across Europe.



<section id="featured-publications" style="text-align:center; margin: 50px 0;">
  <h2>Featured Publications</h2>

  <div class="pub-carousel">
    <div class="slides">
      <div class="slide active">
        <a href="https://www.sciencedirect.com/science/article/pii/S0022510X25003557" target="_blank">
          <img src="/images/papers/NeuroDeepReview.png" alt="ReviewDeepNEuro">
        </a>
      </div>
      <div class="slide">
        <a href="https://link.springer.com/article/10.1007/s10278-024-01336-y" target="_blank">
          <img src="/images/papers/ViViEchoformer.png" alt="ViViEchoformer">
        </a>
      </div>
      <div class="slide">
        <a href="https://www.nature.com/articles/s41598-024-59578-3" target="_blank">
          <img src="/images/papers/JointTransformer.png" alt="JoinTransformer">
        </a>
      </div>
      <div class="slide">
        <a href="https://www.sciencedirect.com/science/article/pii/S0306452225009108?ssrnid=5276922&dgcid=SSRN_redirect_SD" target="_blank">
          <img src="/images/papers/Alzhformer.png" alt="AlzFormer">
        </a>
      </div>
    </div>

    <div class="dots">
      <span class="dot active"></span>
      <span class="dot"></span>
      <span class="dot"></span>
      <span class="dot"></span>
    </div>
  </div>
</section>

<style>
#featured-publications {
  max-width: 900px;
  margin: 0 auto;
}

.pub-carousel {
  position: relative;
  overflow: hidden;
}

.slides {
  display: flex;
  transition: transform 0.6s ease;
}

.slide {
  min-width: 100%;
  display: none;
  justify-content: center;
  align-items: center;
}

.slide.active {
  display: flex;
}

.slide img {
  width: 140px;
  height: 190px;
  border-radius: 10px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.15);
  transition: transform 0.3s ease;
}

.slide img:hover {
  transform: scale(1.05);
}

.dots {
  text-align: center;
  margin-top: 12px;
}

.dot {
  height: 10px;
  width: 10px;
  margin: 0 4px;
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
const slides = document.querySelectorAll('.slide');
const dots = document.querySelectorAll('.dot');
let currentIndex = 0;

function showSlide(index) {
  slides.forEach((slide, i) => {
    slide.classList.toggle('active', i === index);
    dots[i].classList.toggle('active', i === index);
  });
}

dots.forEach((dot, i) => {
  dot.addEventListener('click', () => {
    currentIndex = i;
    showSlide(currentIndex);
  });
});

setInterval(() => {
  currentIndex = (currentIndex + 1) % slides.length;
  showSlide(currentIndex);
}, 4000);
</script>


