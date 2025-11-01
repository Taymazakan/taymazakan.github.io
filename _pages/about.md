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
}

.slides {
  display: flex;
  transition: transform 0.6s ease;
}

.slide {
  flex: 0 0 33.33%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.slide img {
  width: 260px;
  height: 350px;
  border-radius: 10px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.15);
  transition: transform 0.3s ease;
}

.slide img:hover {
  transform: scale(1.05);
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
let currentIndex = 0;
const slidesPerView = 3;
const totalSlides = document.querySelectorAll('.slide').length;
const totalPages = Math.ceil(totalSlides / slidesPerView);

function showSlides(index) {
  const offset = index * (100 / totalPages);
  slidesContainer.style.transform = `translateX(-${offset}%)`;
  dots.forEach((dot, i) => dot.classList.toggle('active', i === index));
}

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
