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
h2.section-title {
  margin-left: 60px;
  margin-bottom: 38px; /* 아래 간격 충분히 */
}
</style>

<h2 class="section-title">Director</h2>
{% for m in site.data.members.faculty %}
<div class="member-flex">
  <img src="{{ m.image }}" alt="{{ m.name }}" class="member-photo">
  <div>
    <!-- 이름과 나머지 텍스트를 같은 블록에! -->
    <div style="font-size:2em; font-weight:700; margin-bottom:10px;">
      {{ m.name }}
    </div>
    {% for pos in m.positions %}
      {{ pos }}<br>
    {% endfor %}
    <p style="margin-top:12px;">
      {% for ed in m.education %}
        <em>{{ ed }}</em></li>
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

<h2 class="section-title">Current Members</h2>
<div style="margin-left:60px;">
  <div style="display:flex; flex-wrap:wrap;">
    {% for c in site.data.members.current %}
      <div style="width:200px; background:#181b1f; margin:10px; padding:12px; border-radius:14px; text-align:center; color:#fafafa;">
        <img src="{{ c.image }}" style="width:65px; height:65px; border-radius:18px;">
        <div style="margin-top:8px; font-weight: bold;">{{ c.name }}</div>
        <div style="font-size:0.95em;">{{ c.title }}</div>
        <div style="font-size:0.92em; color:#cfcfcf;">{{ c.description }}</div>
      </div>
    {% endfor %}
  </div>
</div>
