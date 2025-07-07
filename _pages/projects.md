---
layout: page
title: Projects
permalink: /projects/
---

<h2>Project in progress</h2>
<div style="display:flex; flex-wrap:wrap; gap:32px;">
  {% for project in site.projects %}
    <div style="width:320px; background:#fff; border-radius:12px; box-shadow:0 4px 12px #e0e0e0; margin-bottom:24px;">
      <img src="{{ project.image }}" alt="{{ project.title }}" style="width:100%; height:160px; object-fit:cover; border-radius:12px 12px 0 0;">
      <div style="padding:18px;">
        <div style="font-weight:700; font-size:1.08em; margin-bottom:8px;">
          {{ project.title | truncate: 42 }}
        </div>
        <div style="font-size:0.98em; color:#777; margin-bottom:18px;">
          {{ project.summary | truncate: 100 }}
        </div>
        <div style="font-size:0.93em; color:#333; margin-bottom:10px;">
          <i class="far fa-calendar-alt"></i>
          {{ project.start }} ~ {{ project.end }}
        </div>
        <div style="text-align:right;">
          <a href="{{ project.url }}" style="font-weight:600; color:#111;">Read More</a>
        </div>
      </div>
    </div>
  {% endfor %}
</div>
