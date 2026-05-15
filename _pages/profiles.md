---
layout: subpage
permalink: /people/
title: people
nav: true
nav_order: 5
nav_active: people
page_title_short: People
page_eyebrow: "PEOPLE · 成员"
page_title_display: "实验室成员 · The people"
page_tagline: "PI, students, and researchers in the group."
---

{% assign pi = site.data.people | where: "role", "pi" | first %}

<div class="people-section-label">PRINCIPAL INVESTIGATOR · 课题组长</div>

<div class="pi-row">
  <div class="pi-photo">{% if pi.photo != "" %}<img src="{{ pi.photo | relative_url }}" alt="{{ pi.name }}">{% else %}[PI photo]{% endif %}</div>
  <div class="pi-info">
    <div class="pi-name">{{ pi.name }}</div>
    <div class="pi-name-zh zh">{{ pi.name_zh }}</div>
    <div class="pi-title">{{ pi.title_en }}</div>
    <div class="pi-title-zh zh">{{ pi.title_zh }}</div>
    <div class="pi-sep"></div>
    <p class="pi-bio">{{ pi.bio }}</p>
    <div class="pi-links">
      <a href="mailto:{{ pi.email }}" class="pi-email">{{ pi.email }}</a>
      <a href="{{ pi.scholar }}">Google Scholar →</a>
      <a href="{{ pi.dblp }}">DBLP →</a>
      <a href="{{ pi.github }}">GitHub →</a>
    </div>
  </div>
</div>

{% assign phds = site.data.people | where: "role", "phd" %}
<div class="people-section">
  <div class="people-section-label">PHD STUDENTS · 博士研究生</div>
  <div class="phd-grid">
    {% for member in phds %}
    <div class="member-card">
      <div class="member-photo phd-photo">{% if member.photo != "" %}<img src="{{ member.photo | relative_url }}" alt="{{ member.name }}">{% endif %}</div>
      <div>
        <div class="member-name">{{ member.name }}</div>
        <div class="member-name-zh zh">{{ member.name_zh }}</div>
        <div class="member-role">PHD · {{ member.year }}</div>
        <div class="member-interest">{{ member.interest }}</div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>

{% assign masters = site.data.people | where: "role", "master" %}
<div class="people-section">
  <div class="people-section-label">MASTER STUDENTS · 硕士研究生</div>
  <div class="master-grid">
    {% for member in masters %}
    <div class="member-card">
      <div class="member-photo master-photo">{% if member.photo != "" %}<img src="{{ member.photo | relative_url }}" alt="{{ member.name }}">{% endif %}</div>
      <div>
        <div class="member-name">{{ member.name }}</div>
        <div class="member-name-zh zh">{{ member.name_zh }}</div>
        <div class="member-role">MASTER · {{ member.year }}</div>
        <div class="member-interest">{{ member.interest }}</div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>

{% assign alumni = site.data.people | where: "role", "alumni" %}
<div class="people-section">
  <div class="people-section-label">ALUMNI · 已毕业</div>
  <div class="alumni-list">
    {% for member in alumni %}
    <div class="alumni-row">
      <span class="alumni-name">{{ member.name }}</span>
      <span class="alumni-name-zh zh">{{ member.name_zh }}</span>
      <span class="alumni-degree">{{ member.degree }}</span>
      <span class="alumni-now">{{ member.now }}</span>
    </div>
    {% endfor %}
  </div>
</div>
