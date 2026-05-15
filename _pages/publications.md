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
page_tagline: "Selected papers across HCI, AI, and human-AI collaboration venues."
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

{% assign years = site.data.publications | map: "year" | uniq | sort | reverse %}
{% for year in years %}
<div class="pub-year">{{ year }}</div>
<hr class="pub-year-divider">

{% assign pubs_in_year = site.data.publications | where: "year", year %}
{% for pub in pubs_in_year %}
<div class="pub-row" data-direction="{{ pub.direction }}">
  <span class="pub-badge {% if pub.tier == 'top' %}top{% else %}secondary{% endif %}">{{ pub.venue }}</span>
  <div>
    <div class="pub-title">{{ pub.title }}</div>
    <div class="pub-authors">{{ pub.authors }}</div>
  </div>
  <div class="pub-links">
    {% for link in pub.links %}
    <a href="{{ link[1] }}">{{ link[0] | upcase }}</a>
    {% endfor %}
  </div>
</div>
{% endfor %}
{% endfor %}

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
