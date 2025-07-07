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
