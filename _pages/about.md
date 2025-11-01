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
  <div class="pub-slider">
    <div class="slide">
      <a href="https://www.sciencedirect.com/science/article/pii/S0022510X25003557" target="_blank">
        <img src="/images/papers/ReviewDeepNEuro.png" alt="ReviewDeepNEuro">
      </a>
    </div>
    <div class="slide">
      <a href="https://link.springer.com/article/10.1007/s10278-024-01336-y" target="_blank">
        <img src="/images/papers/ViViEchoformer.png" alt="ViViEchoformer">
      </a>
    </div>
    <div class="slide">
      <a href="https://www.nature.com/articles/s41598-024-59578-3" target="_blank">
        <img src="/images/papers/JoinTransformer.png" alt="JoinTransformer">
      </a>
    </div>
    <div class="slide">
      <a href="https://www.sciencedirect.com/science/article/pii/S0306452225009108?ssrnid=5276922&dgcid=SSRN_redirect_SD" target="_blank">
        <img src="/images/papers/AlzFormer.png" alt="AlzFormer">
      </a>
    </div>
  </div>
</section>

<style>
.pub-slider {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  gap: 25px;
  padding: 20px;
  scrollbar-width: none;
  justify-content: center;
}
.pub-slider::-webkit-scrollbar {
  display: none;
}
.slide {
  flex: 0 0 auto;
  scroll-snap-align: center;
  width: 320px;
  height: 440px;
  border-radius: 12px;
  background: #fdfdfd;
  box-shadow: 0 4px 20px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}
.slide:hover {
  transform: scale(1.05);
}
.slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 12px;
}
h2 {
  font-size: 1.8em;
  font-weight: 600;
  margin-bottom: 15px;
}
</style>

<script>
const slider = document.querySelector('.pub-slider');
let isDown = false;
let startX;
let scrollLeft;

slider.addEventListener('mousedown', (e) => {
  isDown = true;
  startX = e.pageX - slider.offsetLeft;
  scrollLeft = slider.scrollLeft;
});
slider.addEventListener('mouseleave', () => isDown = false);
slider.addEventListener('mouseup', () => isDown = false);
slider.addEventListener('mousemove', (e) => {
  if(!isDown) return;
  e.preventDefault();
  const x = e.pageX - slider.offsetLeft;
  const walk = (x - startX) * 2;
  slider.scrollLeft = scrollLeft - walk;
});
</script>

