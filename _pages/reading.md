---
layout: subpage
permalink: /reading/
title: reading
nav: true
nav_order: 4
nav_active: reading
page_title_short: Reading
page_eyebrow: "READING · 札记"
page_title_display: "Notes · 札记"
page_tagline: "Papers and ideas the group thinks are worth reading and writing about."
---

{% for note in site.data.notes %}
<div class="reading-card {% if note.featured %}reading-card--featured{% endif %}">
  <div class="reading-card-header">
    <div class="reading-card-date">{{ note.date | date: "%Y.%m.%d" }}</div>
    {% if note.featured %}<span class="reading-card-badge">FEATURED · 精读</span>{% endif %}
    <div class="reading-card-source">{{ note.paper }}</div>
    <div class="reading-card-meta">{{ note.paper_meta }}</div>
  </div>
  <div class="reading-card-body">
    <h3 class="reading-card-title zh"><a href="{{ note.url | relative_url }}">{{ note.title_zh }}</a></h3>
    {% if note.subtitle_zh != '' %}<div class="reading-card-subtitle zh">{{ note.subtitle_zh }}</div>{% endif %}
    {% if note.quote != '' %}
    <blockquote class="reading-card-quote">{{ note.quote }}</blockquote>
    {% endif %}
  </div>
  <div class="reading-card-footer">
    <span class="reading-card-author">— {{ note.author }}</span>
    {% if note.word_count > 0 %}
    <a href="{{ note.url }}" class="reading-card-link">Read full note ({{ note.word_count }} 字) →</a>
    {% endif %}
  </div>
</div>
{% endfor %}
