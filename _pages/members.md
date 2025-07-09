---
layout: page
title: People
permalink: /people/
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
  text-align: center;
  margin-left: 0;
  margin-bottom: 38px;
  font-size: 1.7em;
}

.member-list-container {
  display: flex;
  justify-content: flex-start;
  flex-wrap: wrap;
  gap: 32px;
  margin: 0 auto 40px auto;
  max-width: 1380px; /* 4 x 320 + gaps */
}
.member-card {
  width: 320px;
  min-height: 430px;
  background: #f6f6f6;
  border-radius: 24px;
  box-shadow: 0 4px 18px #e5e5e5;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  overflow: hidden;
  margin-bottom: 18px;
}
.member-card img {
  width: 100%;
  aspect-ratio: 1/1;
  object-fit: cover;
  border-radius: 24px 24px 0 0;
}
.member-card-info {
  padding: 18px 18px 12px 18px;
  width: 100%;
}
@media (max-width: 1300px) {
  .member-list-container { max-width: 1040px; }
}
@media (max-width: 1050px) {
  .member-list-container { max-width: 680px; }
}
@media (max-width: 750px) {
  .member-list-container { max-width: 340px; flex-direction: column; align-items: center; }
}
.member-card-name {
  font-size: 1em;
  font-weight: 600;
  margin-bottom: 2px;
}
.member-card-title {
  font-size: 0.92em;
  color: #333;
  font-weight: 500;
  margin-bottom: 5px;
}
.member-card-desc {
  font-size: 0.89em;
  color: #666;
  margin-bottom: 9px;
}

.members-header-image {
  position: relative;
  width: 100vw;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  height: 320px;
  background: url('/assets/images/12th_Man.jpg') center center / cover no-repeat;
  display: flex;
  align-items: center;
}
.members-header-overlay {
  position: absolute;
  inset: 0;
  background: rgba(30,30,30,0.30); /* overlay_filter: 0.2 */
  z-index: 1;
}
.members-header-text {
  position: relative;
  z-index: 2;
  color: #fff;
  font-size: 2.5em;
  font-weight: 700;
  margin-right: 7vw;
  margin-left: auto;      /* 왼쪽 여백 없이 */
  text-shadow: 0 2px 16px rgba(0,0,0,0.14);
  letter-spacing: 1px;
  display: flex;
  align-items: center;
  justify-content: flex-start;   /* 오른쪽 정렬 */
  width: 100%;
  height: 100%;
  text-align: left;
}

@media (max-width: 800px) {
  .members-header-image { height: 180px; }
  .members-header-text { font-size: 1.7em; margin-left: 18px;}
}

  
</style>

<div class="members-header-image">
  <div class="members-header-overlay"></div>
  <div class="members-header-text">
    <span>People</span>
  </div>
</div>

<!-- Director Section -->
<h2 class="section-title">Director</h2>
{% for m in site.data.members.faculty %}
<div class="member-flex">
  <img src="{{ m.image }}" alt="{{ m.name }}" class="member-photo">
  <div>
    <div style="font-size:1.1em; font-weight:600; margin-bottom:10px;">
      <span style="margin-left:10px;">{{ m.name }}</span>
      {% if m.website %}
        <a href="{{ m.website }}" target="_blank" title="Website" style="color:#888; display:inline-block; margin-right:4px;">
          <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:middle;"><circle cx="10" cy="10" r="8"/><line x1="2" y1="10" x2="18" y2="10"/><path d="M10 2a13 13 0 0 1 0 16M10 2a13 13 0 0 0 0 16"/></svg>
        </a>
      {% endif %}
      {% if m.linkedin %}
        <a href="{{ m.linkedin }}" target="_blank" title="LinkedIn" style="color:#888; display:inline-block;">
          <svg width="20" height="20" fill="currentColor" style="vertical-align:middle;" viewBox="0 0 448 512"><path d="M100.28 448H7.4V148.9h92.88zm-46.44-340C24.12 108 0 83.87 0 54.89A53.34 53.34 0 0 1 53.67 1.5c29.66 0 53.67 24.09 53.67 53.39 0 28.98-24.01 53.11-53.67 53.11zm394.84 340h-92.4V302.4c0-34.7-.7-79.29-48.32-79.29-48.38 0-55.78 37.78-55.78 76.87V448H160V148.9h88.56v40.81h1.28c12.36-23.38 42.56-48.32 87.56-48.32 93.68 0 110.92 61.73 110.92 142.3V448z"/></svg>
        </a>
      {% endif %}
      {% if m.scholar %}
        <a href="{{ m.scholar }}" target="_blank" title="Google Scholar" style="color:#888; display:inline-block;">
          <svg width="22" height="22" viewBox="0 0 256 256" fill="currentColor" style="vertical-align:middle;">
            <circle cx="128" cy="128" r="120" fill="currentColor"/>
            <path d="M103 174.2c0 22.9 20.1 36.5 41.3 36.5 17.3 0 31.4-7.2 31.4-25.5 0-19.7-14.8-21.2-28.2-22.7-8.1-.9-19-1.8-19-8.2 0-6.2 9.2-8.4 18-8.4 8.7 0 19.8 2.1 19.8 10.1h17.3c0-20.1-21.1-27.6-36.8-27.6-17.4 0-34.7 7.1-34.7 23.6 0 16.2 15.6 18.1 30.4 19.5 12.3 1.2 16.9 2.2 16.9 8.2 0 6.1-9.9 8.5-18.1 8.5-10.3 0-20.1-2.2-20.1-11.4H103z" fill="#fff"/>
            <path d="M205 62l-76.6-33.8c-1.3-.6-2.7-.6-3.9 0L51 62c-2.3 1-2.4 4.3-.1 5.4l26.5 12c2.2 1 4.7.1 5.7-2l9.4-21.5 31.4-13.9c1.3-.6 2.7-.6 3.9 0l31.4 13.9 9.4 21.5c1 2.1 3.5 3 5.7 2l26.5-12c2.3-1.1 2.2-4.4-.1-5.4z" fill="#fff"/>
            <rect x="181" y="75" width="13" height="34" rx="6.5" fill="#fff"/>
          </svg>
        </a>
      {% endif %}
    </div>
    {% if m.positions %}
      <div style="margin-bottom:10px; margin-left:0px;">
        <ul>
        {% for pos in m.positions %}
          <li>{{ pos }}</li>
        {% endfor %}
        </ul>
      </div>
    {% endif %}
    {% if m.education %}
      <div style="margin-bottom:10px;">
        <strong style="margin-left:10px;">Education</strong>
        <ul>
        {% for ed in m.education %}
          <li>{{ ed }}</li>
        {% endfor %}
        </ul>
      </div>
    {% endif %}
    {% if m.affiliations %}
      <div style="margin-bottom:10px;">
        <strong style="margin-left:10px;">Career</strong>
        <ul>
        {% for aff in m.affiliations %}
          <li>{{ aff }}</li>
        {% endfor %}
        </ul>
      </div>
    {% endif %}
    {% if m.awards %}
      <div style="margin-bottom:10px;margin-left:0px;">
        <strong style="margin-left:10px;">Honors & Awards</strong>
        <ul>
        {% for a in m.awards %}
          <li>{{ a }}</li>
        {% endfor %}
        </ul>
      </div>
    {% endif %}
  </div>
</div>
{% endfor %}

<!-- Current Members Section -->
<h2 class="section-title">Current Members</h2>
<div class="member-list-container">
  {% for c in site.data.members.current %}
    <div class="member-card">
      <img src="{{ c.image }}" alt="{{ c.name }}">
      <div class="member-card-info">
        <div class="member-card-name">{{ c.name }}</div>
        <div class="member-card-title">{{ c.title }}</div>
        {% if c.description %}
          <div class="member-card-desc">{{ c.description }}</div>
        {% endif %}
        {% if c.website %}
          <a href="{{ c.website }}" target="_blank" title="Website" style="color:#888; display:inline-block; margin-right:4px;">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:middle;"><circle cx="10" cy="10" r="8"/><line x1="2" y1="10" x2="18" y2="10"/><path d="M10 2a13 13 0 0 1 0 16M10 2a13 13 0 0 0 0 16"/></svg>
          </a>
        {% endif %}
        {% if c.linkedin %}
          <a href="{{ c.linkedin }}" target="_blank" title="LinkedIn" style="color:#888; display:inline-block;">
            <svg width="20" height="20" fill="currentColor" style="vertical-align:middle;" viewBox="0 0 448 512"><path d="M100.28 448H7.4V148.9h92.88zm-46.44-340C24.12 108 0 83.87 0 54.89A53.34 53.34 0 0 1 53.67 1.5c29.66 0 53.67 24.09 53.67 53.39 0 28.98-24.01 53.11-53.67 53.11zm394.84 340h-92.4V302.4c0-34.7-.7-79.29-48.32-79.29-48.38 0-55.78 37.78-55.78 76.87V448H160V148.9h88.56v40.81h1.28c12.36-23.38 42.56-48.32 87.56-48.32 93.68 0 110.92 61.73 110.92 142.3V448z"/></svg>
          </a>
        {% endif %}
        {% if c.scholar %}
          <a href="{{ c.scholar }}" target="_blank" title="Google Scholar" style="color:#888; display:inline-block; margin-right:8px;">
            <svg width="22" height="22" viewBox="0 0 256 256" fill="none" style="vertical-align:middle;">
              <circle cx="128" cy="128" r="120" fill="currentColor"/>
              <path d="M103 174.2c0 22.9 20.1 36.5 41.3 36.5 17.3 0 31.4-7.2 31.4-25.5 0-19.7-14.8-21.2-28.2-22.7-8.1-.9-19-1.8-19-8.2 0-6.2 9.2-8.4 18-8.4 8.7 0 19.8 2.1 19.8 10.1h17.3c0-20.1-21.1-27.6-36.8-27.6-17.4 0-34.7 7.1-34.7 23.6 0 16.2 15.6 18.1 30.4 19.5 12.3 1.2 16.9 2.2 16.9 8.2 0 6.1-9.9 8.5-18.1 8.5-10.3 0-20.1-2.2-20.1-11.4H103z" fill="#fff"/>
              <path d="M205 62l-76.6-33.8c-1.3-.6-2.7-.6-3.9 0L51 62c-2.3 1-2.4 4.3-.1 5.4l26.5 12c2.2 1 4.7.1 5.7-2l9.4-21.5 31.4-13.9c1.3-.6 2.7-.6 3.9 0l31.4 13.9 9.4 21.5c1 2.1 3.5 3 5.7 2l26.5-12c2.3-1.1 2.2-4.4-.1-5.4z" fill="#fff"/>
              <rect x="181" y="75" width="13" height="34" rx="6.5" fill="#fff"/>
            </svg>
          </a>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>

<!-- Former Members Section -->
<h2 class="section-title">Former Members</h2>
<div class="member-list-container">
  {% for f in site.data.members.former %}
    <div class="member-card">
      <img src="{{ f.image }}" alt="{{ f.name }}">
      <div class="member-card-info">
        <div class="member-card-name">{{ f.name }}</div>
        <div class="member-card-title">{{ f.title }}</div>
        {% if f.description %}
          <div class="member-card-desc">{{ f.description }}</div>
        {% endif %}
        {% if f.website %}
          <a href="{{ f.website }}" target="_blank" title="Website" style="color:#888; display:inline-block; margin-right:6px;">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:middle;">
              <circle cx="10" cy="10" r="8"/>
              <line x1="2" y1="10" x2="18" y2="10"/>
              <path d="M10 2a13 13 0 0 1 0 16M10 2a13 13 0 0 0 0 16"/>
            </svg>
          </a>
        {% endif %}
        {% if f.linkedin %}
          <a href="{{ f.linkedin }}" target="_blank" title="LinkedIn" style="color:#888; display:inline-block;">
            <svg width="20" height="20" fill="currentColor" style="vertical-align:middle;" viewBox="0 0 448 512">
              <path d="M100.28 448H7.4V148.9h92.88zm-46.44-340C24.12 108 0 83.87 0 54.89A53.34 53.34 0 0 1 53.67 1.5c29.66 0 53.67 24.09 53.67 53.39 0 28.98-24.01 53.11-53.67 53.11zm394.84 340h-92.4V302.4c0-34.7-.7-79.29-48.32-79.29-48.38 0-55.78 37.78-55.78 76.87V448H160V148.9h88.56v40.81h1.28c12.36-23.38 42.56-48.32 87.56-48.32 93.68 0 110.92 61.73 110.92 142.3V448z"/>
            </svg>
          </a>
        {% endif %}
        {% if f.scholar %}
          <a href="{{ f.scholar }}" target="_blank" title="Google Scholar" style="color:#888; display:inline-block; margin-right:8px;">
            <svg width="22" height="22" viewBox="0 0 256 256" fill="currentColor" style="vertical-align:middle;">
              <circle cx="128" cy="128" r="120" fill="currentColor"/>
              <path d="M103 174.2c0 22.9 20.1 36.5 41.3 36.5 17.3 0 31.4-7.2 31.4-25.5 0-19.7-14.8-21.2-28.2-22.7-8.1-.9-19-1.8-19-8.2 0-6.2 9.2-8.4 18-8.4 8.7 0 19.8 2.1 19.8 10.1h17.3c0-20.1-21.1-27.6-36.8-27.6-17.4 0-34.7 7.1-34.7 23.6 0 16.2 15.6 18.1 30.4 19.5 12.3 1.2 16.9 2.2 16.9 8.2 0 6.1-9.9 8.5-18.1 8.5-10.3 0-20.1-2.2-20.1-11.4H103z" fill="#fff"/>
              <path d="M205 62l-76.6-33.8c-1.3-.6-2.7-.6-3.9 0L51 62c-2.3 1-2.4 4.3-.1 5.4l26.5 12c2.2 1 4.7.1 5.7-2l9.4-21.5 31.4-13.9c1.3-.6 2.7-.6 3.9 0l31.4 13.9 9.4 21.5c1 2.1 3.5 3 5.7 2l26.5-12c2.3-1.1 2.2-4.4-.1-5.4z" fill="#fff"/>
              <rect x="181" y="75" width="13" height="34" rx="6.5" fill="#fff"/>
            </svg>
          </a>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>
