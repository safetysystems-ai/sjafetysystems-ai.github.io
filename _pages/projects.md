---
layout: page
title: Projects
permalink: /projects/
---

<style>
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(325px, 1fr));
  gap: 32px;
  margin-top: 32px;
}
.project-card {
  background: #f6f7fa;
  border-radius: 18px;
  box-shadow: 0 4px 20px #e2e5ea;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: transform 0.18s, box-shadow 0.18s;
}
.project-card:hover {
  transform: translateY(-4px) scale(1.03);
  box-shadow: 0 8px 28px #d4d8e1;
}
.project-img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-radius: 18px 18px 0 0;
  background: #cdd1d6;
}
.project-body {
  padding: 22px 22px 18px 22px;
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
}
.project-title {
  font-size: 1.1em;
  font-weight: 700;
  margin-bottom: 10px;
  color: #1c222c;
  letter-spacing: 0.01em;
}
.project-summary {
  font-size: 0.99em;
  color: #586174;
  margin-bottom: 18px;
  min-height: 45px;
}
.project-period {
  font-size: 0.93em;
  color: #7b8897;
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 6px;
}
.project-readmore {
  margin-top: auto;
  font-size: 0.96em;
  color: #2a67fa;
  font-weight: 600;
  text-decoration: none;
  letter-spacing: 0.03em;
  transition: color 0.15s;
}
.project-readmore:hover {
  color: #194ed3;
  text-decoration: underline;
}
</style>

<h2 style="margin-top:24px;">Project in progress</h2>
<div class="project-grid">
  {% for project in site.projects %}
    <div class="project-card">
      <img class="project-img" src="{{ project.image }}" alt="{{ project.title }}">
      <div class="project-body">
        <div class="project-title">{{ project.title | truncate: 48 }}</div>
        <div class="project-summary">{{ project.summary | truncate: 90 }}</div>
        <div class="project-period">📅 {{ project.start }} ~ {{ project.end }}</div>
        <a class="project-readmore" href="{{ project.url }}">Read More &rarr;</a>
      </div>
    </div>
  {% endfor %}
</div>
