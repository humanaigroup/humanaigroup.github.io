---
layout: subpage
permalink: /publications/
title: publications
nav: true
nav_order: 3
nav_active: publications
page_title_short: Publications
page_eyebrow: "PUBLICATIONS · 论文"
page_title_display: "Publications · 发表论文"
page_tagline: "35 papers across HCI, AI, and human-AI collaboration venues."
---

<div class="pub-filter">
  <div class="pub-filter-label">FILTER BY DIRECTION · 按方向筛选</div>
  <div class="pub-pills">
    <button class="pub-pill active" data-filter="all">All</button>
    <button class="pub-pill" data-filter="co-perception">Co-Perception</button>
    <button class="pub-pill" data-filter="user-simulation">User Simulation</button>
    <button class="pub-pill" data-filter="embodied-coaching">Embodied Coaching</button>
    <button class="pub-pill" data-filter="earlier">Earlier</button>
  </div>
</div>

<div class="pub-year">2025</div>
<hr class="pub-year-divider">

<div class="pub-row" data-direction="user-simulation">
  <span class="pub-badge top">IJHCS</span>
  <div>
    <div class="pub-title">Pika: Designing a social-support agent to improve drivers' experience in gig work</div>
    <div class="pub-authors">Wei Xiang, Xiang Chen, Ting Guo, Mingming Zhou, Shuai Chen</div>
  </div>
  <div class="pub-links">
    <a href="#">PDF</a>
    <a href="#">DOI</a>
    <a href="#">Bib</a>
  </div>
</div>

<div class="pub-row" data-direction="co-perception">
  <span class="pub-badge top">T-ITS</span>
  <div>
    <div class="pub-title">Visionary Co-Driver: Enhancing driver perception of potential risks</div>
    <div class="pub-authors">Wei Xiang, Zhenxing Lei, Haoyan Che, Fangzhou Ye et al.</div>
  </div>
  <div class="pub-links">
    <a href="#">PDF</a>
    <a href="#">DOI</a>
    <a href="#">Bib</a>
  </div>
</div>

<div class="pub-row" data-direction="embodied-coaching">
  <span class="pub-badge top">IJCAI</span>
  <div>
    <div class="pub-title">Hand by Hand: LLM driving EMS assistant for operational skill learning</div>
    <div class="pub-authors">Wei Xiang, Zhenxing Lei, Haoyan Che, Fangzhou Ye et al.</div>
  </div>
  <div class="pub-links">
    <a href="#">PDF</a>
    <a href="#">Code</a>
    <a href="#">Bib</a>
  </div>
</div>

<div class="pub-row" data-direction="earlier">
  <span class="pub-badge secondary">SMC</span>
  <div>
    <div class="pub-title">CareEmo: Supporting caregivers with personalized communication approaches</div>
    <div class="pub-authors">Meng Li, Wei Xiang, Yi He, Menghan Jiang, Xiangshi Wu</div>
  </div>
  <div class="pub-links">
    <a href="#">PDF</a>
    <a href="#">DOI</a>
    <a href="#">Bib</a>
  </div>
</div>

<div class="pub-row" data-direction="user-simulation">
  <span class="pub-badge top">CHI</span>
  <div>
    <div class="pub-title">Voice by the Non-sighted: Practices and challenges of audiobook voice actors</div>
    <div class="pub-authors">Shuai Chen, Jiayi Zhang, Shixian Lou, Xiaoyu Wang, Wei Xiang, Lian Sun</div>
  </div>
  <div class="pub-links">
    <a href="#">PDF</a>
    <a href="#">DOI</a>
    <a href="#">Bib</a>
  </div>
</div>

<div class="pub-year">2024</div>
<hr class="pub-year-divider">

<div class="pub-row" data-direction="user-simulation">
  <span class="pub-badge top">CHI</span>
  <div>
    <div class="pub-title">SimUser: Generating usability feedback by simulating various users</div>
    <div class="pub-authors">Wei Xiang, Hanxian Zhu, Shixian Lou, Xiang Chen et al.</div>
  </div>
  <div class="pub-links">
    <a href="#">PDF</a>
    <a href="#">Abs</a>
    <a href="#">DOI</a>
    <a href="#">Bib</a>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  var pills = document.querySelectorAll('.pub-pill');
  var rows = document.querySelectorAll('.pub-row');
  var years = document.querySelectorAll('.pub-year');
  var yearDividers = document.querySelectorAll('.pub-year-divider');

  pills.forEach(function(pill) {
    pill.addEventListener('click', function() {
      pills.forEach(function(p) { p.classList.remove('active'); });
      pill.classList.add('active');
      var filter = pill.getAttribute('data-filter');

      rows.forEach(function(row) {
        if (filter === 'all' || row.getAttribute('data-direction') === filter) {
          row.style.display = '';
        } else {
          row.style.display = 'none';
        }
      });

      years.forEach(function(year, i) {
        var divider = yearDividers[i];
        var nextEl = divider.nextElementSibling;
        var hasVisible = false;
        while (nextEl && !nextEl.classList.contains('pub-year')) {
          if (nextEl.classList.contains('pub-row') && nextEl.style.display !== 'none') {
            hasVisible = true;
            break;
          }
          nextEl = nextEl.nextElementSibling;
        }
        year.style.display = hasVisible ? '' : 'none';
        divider.style.display = hasVisible ? '' : 'none';
      });
    });
  });
});
</script>
