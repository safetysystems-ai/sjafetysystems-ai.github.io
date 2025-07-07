---
layout: splash
title: "AI-Powered 
Safety Systems 
Research"
header:
  overlay_image: /assets/images/Asset_22.png   # 사용하고 싶은 이미지 경로
  overlay_filter: 0.2           # 어두운 효과(0~1), 원하면 조정
  actions:
    - label: "Learn More"
      url: "/about/"
excerpt: "Safety Systems AI (SSAI) Lab"
---

<h2 style="text-align:center; margin-top:50px; font-size:2.1em;">Research Projects</h2>
<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 32px; margin-top:32px;">
{% for p in site.data.projects %}
  <a href="{{ p.link }}" style="text-decoration:none;">
    <div>
      <img src="{{ p.image }}">
      <h3>{{ p.title }}</h3>
      <div>{{ p.summary }}</div>
    </div>
  </a>
{% endfor %}
</div>
