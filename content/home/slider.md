---
widget: markdown
headless: true
weight: 1

design:
  columns: '1'
  spacing:
    padding: ['0', '0', '0', '0']
---

<div class="slider-container">
  <div class="slide active" style="background-image: url('https://images.unsplash.com/photo-1550751827-4bd374c3f58b?w=1920&q=80');">
    <div class="slide-content">
      <h1>정보보안 학습</h1>
      <p>체계적인 정보보안 지식 습득</p>
    </div>
  </div>
  
  <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?w=1920&q=80');">
    <div class="slide-content">
      <h1>웹 해킹 연구</h1>
      <p>다양한 웹 취약점 분석 및 연구</p>
    </div>
  </div>
  
  <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1558494949-ef010cbdcc31?w=1920&q=80');">
    <div class="slide-content">
      <h1>CTF/WARGAME</h1>
      <p>실전 문제 해결 능력 향상</p>
    </div>
  </div>
  
  <div class="slider-controls">
    <button class="prev" onclick="changeSlide(-1)">‹</button>
    <button class="next" onclick="changeSlide(1)">›</button>
  </div>
  
  <div class="slider-dots">
    <span class="dot active" onclick="currentSlide(1)"></span>
    <span class="dot" onclick="currentSlide(2)"></span>
    <span class="dot" onclick="currentSlide(3)"></span>
  </div>
</div>

<script>
let slideIndex = 1;
showSlide(slideIndex);

setInterval(() => {
  changeSlide(1);
}, 3000);

function changeSlide(n) {
  showSlide(slideIndex += n);
}

function currentSlide(n) {
  showSlide(slideIndex = n);
}

function showSlide(n) {
  let slides = document.querySelectorAll('.slide');
  let dots = document.querySelectorAll('.dot');
  
  if (n > slides.length) { slideIndex = 1 }
  if (n < 1) { slideIndex = slides.length }
  
  slides.forEach(slide => slide.classList.remove('active'));
  dots.forEach(dot => dot.classList.remove('active'));
  
  slides[slideIndex - 1].classList.add('active');
  dots[slideIndex - 1].classList.add('active');
}
</script>

<style>
.slider-container {
  position: relative;
  width: 100%;
  height: 500px;
  overflow: hidden;
  margin: 0;
  padding: 0;
}

.slide {
  position: absolute;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  display: none;
  align-items: center;
  justify-content: center;
}

.slide.active {
  display: flex;
  animation: fadeIn 1s;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.slide::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.4);
}

.slide-content {
  position: relative;
  z-index: 2;
  text-align: center;
  color: white;
  padding: 2rem;
}

.slide-content h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
  font-weight: bold;
}

.slide-content p {
  font-size: 1.3rem;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.7);
}

.slider-controls button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(255, 255, 255, 0.3);
  color: white;
  border: none;
  font-size: 3rem;
  padding: 0.5rem 1rem;
  cursor: pointer;
  z-index: 3;
  transition: all 0.3s;
}

.slider-controls button:hover {
  background: rgba(255, 255, 255, 0.5);
}

.slider-controls .prev { left: 20px; }
.slider-controls .next { right: 20px; }

.slider-dots {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 3;
}

.dot {
  display: inline-block;
  width: 12px;
  height: 12px;
  margin: 0 5px;
  background: rgba(255, 255, 255, 0.5);
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.3s;
}

.dot.active, .dot:hover {
  background: white;
  transform: scale(1.3);
}
</style>