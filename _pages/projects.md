---
layout: page
title: Projects
permalink: /projects/
---

# Research Projects

<div style="display: flex; flex-wrap: wrap; gap: 32px;">
{% for p in site.data.projects %}
  <a href="{{ p.link }}" style="text-decoration:none; color:inherit;">
    <div style="width:320px; background:#f8f8f8; border-radius:18px; box-shadow:0 4px 12px #eee; overflow:hidden;">
      <img src="{{ p.image }}" style="width:100%; height:170px; object-fit:cover;">
      <div style="padding:16px;">
        <strong>{{ p.title }}</strong>
        <div style="color:#555; margin-top:6px;">{{ p.summary }}</div>
      </div>
    </div>
  </a>
{% endfor %}
</div>
