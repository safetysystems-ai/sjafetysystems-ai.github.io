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
  {% for p in site.data.projects limit:3 %}
    <a href="{{ p.link }}" style="text-decoration:none; color:inherit;">
      <div style="width:330px; background:#f8f8f8; border-radius:20px; box-shadow:0 4px 16px #e0e0e0; overflow:hidden; transition:transform 0.15s; margin-bottom:24px;">
        <img src="{{ p.image }}" alt="{{ p.title }}" style="width:100%; height:170px; object-fit:cover;">
        <div style="padding:18px;">
          <div style="font-weight:600; font-size:1.16em; margin-bottom:8px;">{{ p.title }}</div>
          <div style="color:#777; font-size:0.98em;">{{ p.summary }}</div>
        </div>
      </div>
    </a>
  {% endfor %}
</div>
