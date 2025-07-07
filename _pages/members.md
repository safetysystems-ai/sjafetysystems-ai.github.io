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
  width: 300px;
  height: 400px;
  border-radius: 15px;
  object-fit: cover;
  box-shadow: 0 4px 20px #ccc;
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

---

<h2 class="section-title">Current Members</h2>
<div style="margin-left:60px;">
  <div style="display: flex; flex-wrap: wrap; gap: 32px;">
    {% for c in site.data.members.current %}
      <div style="width:320px; min-height: 430px; background:#f6f6f6; border-radius:24px; margin-bottom:18px; box-shadow:0 4px 18px #e5e5e5; display:flex; flex-direction:column; align-items:flex-start; overflow:hidden;">
        <img src="{{ c.image }}" alt="{{ c.name }}" style="width:100%; aspect-ratio:1/1; object-fit:cover; border-radius:24px 24px 0 0;">
        <div style="padding:18px 18px 12px 18px; width:100%;">
          <div style="font-weight:600; font-size:1.1em; margin-bottom:2px;">{{ c.name }}</div>
          <div style="font-size:1em; color:#333; font-weight:500; margin-bottom:6px;">{{ c.title }}</div>
          {% if c.description %}
            <div style="font-size:0.97em; color:#666; margin-bottom:10px;">{{ c.description }}</div>
          {% endif %}
          {% if c.website %}
            <a href="{{ c.website }}" target="_blank" title="Website" style="color:#222; display:inline-block; margin-right:8px;">
              <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:middle;"><circle cx="10" cy="10" r="8"/><line x1="2" y1="10" x2="18" y2="10"/><path d="M10 2a13 13 0 0 1 0 16M10 2a13 13 0 0 0 0 16"/></svg>
            </a>
          {% endif %}
          {% if c.linkedin %}
            <a href="{{ c.linkedin }}" target="_blank" title="LinkedIn" style="color:#0077b5; display:inline-block;">
              <svg width="20" height="20" fill="currentColor" style="vertical-align:middle;" viewBox="0 0 448 512"><path d="M100.28 448H7.4V148.9h92.88zm-46.44-340C24.12 108 0 83.87 0 54.89A53.34 53.34 0 0 1 53.67 1.5c29.66 0 53.67 24.09 53.67 53.39 0 28.98-24.01 53.11-53.67 53.11zm394.84 340h-92.4V302.4c0-34.7-.7-79.29-48.32-79.29-48.38 0-55.78 37.78-55.78 76.87V448H160V148.9h88.56v40.81h1.28c12.36-23.38 42.56-48.32 87.56-48.32 93.68 0 110.92 61.73 110.92 142.3V448z"/></svg>
            </a>
          {% endif %}
          {% if c.scholar %}
            <a href="{{ c.scholar }}" target="_blank" title="Google Scholar" style="color:#4285F4; display:inline-block; margin-right:8px;">
              <!-- Google Scholar SVG -->
              <svg width="20" height="20" fill="currentColor" viewBox="0 0 48 48" style="vertical-align:middle;">
                <g><ellipse cx="24" cy="41" rx="20" ry="4" fill="#4285F4"/><path d="M9.4 34c3-4.8 8.3-8 14.6-8s11.6 3.2 14.6 8" fill="#A0C3FF"/><path d="M24 34C15 34 7.9 28.5 6.2 20.5c-.3-1.5 1-2.7 2.5-2.7h30.6c1.5 0 2.8 1.2 2.5 2.7C40.1 28.5 33 34 24 34z" fill="#4285F4"/><circle cx="24" cy="14" r="11" fill="#4285F4"/><path d="M24 19a5 5 0 110-10 5 5 0 010 10z" fill="#FFF"/></g>
              </svg>
            </a>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  </div>
</div>
