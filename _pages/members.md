---
layout: page
title: Members
permalink: /members/
---

<style>
.member-flex {
  display: flex;
  align-items: flex-start;
  gap: 40px;
  margin-left: 60px;
  margin-bottom: 40px;
}
.member-photo {
  width: 200px;
  height: 200px;
  border-radius: 18px;
  object-fit: cover;
  box-shadow: 0 4px 24px #ccc;
}
@media (max-width: 700px) {
  .member-flex {
    flex-direction: column;
    margin-left: 0;
    gap: 20px;
    align-items: center;
  }
}
</style>

<div style="margin-left: 60px;">
## Director
</div>

<!-- Faculty loop -->
{% for m in site.data.members.faculty %}
<div class="member-flex">
  <img src="{{ m.image }}" alt="{{ m.name }}" class="member-photo">
  <div>
    <h2 style="margin-top:0;">{{ m.name }}</h2>
    <strong>{{ m.title }}</strong><br>
    {% for pos in m.positions %}
      {{ pos }}<br>
    {% endfor %}
    <p>
      {% for ed in m.education %}
        <em>{{ ed }}</em><br>
      {% endfor %}
    </p>
    <strong>Awards:</strong>
    <ul>
      {% for a in m.awards %}
        <li>{{ a }}</li>
      {% endfor %}
    </ul>
    {% if m.linkedin %}
      <a href="{{ m.linkedin }}" target="_blank">LinkedIn</a>
    {% endif %}
    {% if m.website %}
      | <a href="{{ m.website }}" target="_blank">Website</a>
    {% endif %}
  </div>
</div>
{% endfor %}

---

<div style="margin-left: 60px;">
## Legacy of Graduated PhDs and Postdocs
</div>

<div style="display:flex; flex-wrap: wrap;">
{% for p in site.data.members.phds_postdocs %}
  <div style="width:270px; background:#181b1f; margin:10px; padding:16px; border-radius:18px; display:inline-block; vertical-align:top; text-align:center; color: #fafafa;">
    <img src="{{ p.image }}" style="width:85px; height:85px; border-radius:15%;">
    <div style="margin-top:10px; font-weight: bold;">{{ p.name }}</div>
    <div style="font-size:0.97em;">{{ p.title }}</div>
    <div style="margin-top:5px; font-size:0.93em;">{{ p.description }}</div>
    {% if p.website %}
      <div style="margin-top:8px;"><a href="{{ p.website }}" target="_blank" style="color:#42a5f5;">Website</a></div>
    {% endif %}
  </div>
{% endfor %}
</div>

---

<div style="margin-left: 60px;">
## Current Members
</div>

<div style="display:flex; flex-wrap: wrap;">
{% for c in site.data.members.current %}
  <div style="width:200px; background:#181b1f; margin:10px; padding:12px; border-radius:14px; text-align:center; color: #fafafa;">
    <img src="{{ c.image }}" style="width:65px; height:65px; border-radius: 15%;">
    <div style="margin-top:8px; font-weight: bold;">{{ c.name }}</div>
    <div style="font-size:0.95em;">{{ c.title }}</div>
    <div style="font-size:0.92em; color:#cfcfcf;">{{ c.description }}</div>
  </div>
{% endfor %}
</div>
