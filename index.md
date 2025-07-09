---
layout: splash
title: "AI-Powered 
Safety Systems 
Research"
header:
  overlay_image: /assets/images/Asset_22.png
  overlay_filter: 0.2
  actions:
    - label: "Learn More"
      url: "/about/"
excerpt: "Safety Systems.AI (SSAI) Lab"
---

<style>
/* 기존 스타일 그대로 사용, 추가 스타일은 필요시 조정 */

.project-card,
.project-card *,
.project-card a {
  text-decoration: none;
}

.project-section-bg {
  background: #f5f6f7;
  min-height: 100vh;
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  padding: 60px 0 80px 0;
  text-decoration: none
}

.project-inner-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 32px;
}

.project-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 32px;
  justify-content: center;
}

.project-card {
  width: 320px;
  background: #fff;
  border-radius: 16px;
  box-shadow: 0 4px 18px #e0e0e0;
  transition: box-shadow .17s, transform .11s;
  display: block;
  text-decoration: none;
  color: inherit;
  margin-bottom: 24px;
  overflow: hidden;
  position: relative;
}
.project-card:hover {
  box-shadow: 0 12px 32px #dbdbdb;
  transform: translateY(-4px) scale(1.025);
}
.project-card-img {
  width: 100%;
  height: 120px;
  object-fit: cover;
  border-radius: 16px 16px 0 0;
  background: #f7f7f7;
}
.project-card-content {
  padding: 18px 18px 8px 18px;
}
.project-title {
  font-weight: 700;
  font-size: 1.08em;
  margin-bottom: 8px;
  color: #171c36;
  line-height: 1.25;
  text-decoration: none
}
.project-summary {
  font-size: 0.97em;
  color: #656e7a;
  margin-bottom: 18px;
  min-height: 52px;
}
.project-date {
  font-size: 0.95em;
  color: #444;
  margin-bottom: 14px;
  display: flex;
  align-items: center;
  gap: 5px;
}
.project-readmore {
  text-align: right;
  font-weight: 600;
  color: #333;
  font-size: 0.90em;
  margin-bottom: 2px;
  letter-spacing: 0.01em;
}
@media (max-width: 850px) {
  .project-inner-container { max-width: 95vw; }
  .project-card { width: 96vw; max-width: 380px;}
}
html {
  scroll-behavior: smooth;
}
.contact-section-bg {
  background: #f8f8fa;
  min-height: 60vh;
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  padding: 60px 0 80px 0;
}
/* About 섹션 구분선용 (필요시 추가) */
.about-section-bg {
  background: #fff;
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  padding: 56px 0 34px 0;
}
</style>

<!-- About Section (Main Page, 풀로고+미션/소개) -->

<div style="max-width:950px; margin:0 auto; display:flex; flex-direction:column; align-items:center;">
  <img src="/assets/images/Logo_full_Blue.png"
        alt="Safety Systems AI Lab Logo"
        style="width:900px; max-width:98vw; height:auto; margin-bottom:22px; margin-top:22px;" />
  <div style="font-size:1.14em; color:#3d4853; font-weight:600; text-align:center; max-width:800px; margin-bottom:10px;">
    Augmenting the Human Cognitive and Physical Capabilities for Safety
  </div>
  <div style="font-size:1.07em; color:#61697a; text-align:center; max-width:900px;margin-bottom:40px;">
    The Safety Systems.AI Lab is dedicated to advancing safety in both workplaces and everyday life by augmenting human cognitive and physical capabilities to prevent accidents and injuries. Our research integrates AI, VR/AR, and advanced sensing technologies to transform how people learn about, manage, and respond to safety risks. By combining insights from cognitive science, engineering, and emerging technologies, we develop intelligent systems that enhance awareness, decision-making, and the ability to respond effectively to safety challenges across diverse environments.
  </div>
</div>


<!-- Research Projects Section (Main Page) -->
<div class="project-section-bg">
  <div class="project-inner-container" style="display:flex; flex-direction:column; align-items:center;">
    <h2 style="font-size:1.5em; font-weight:600; margin-bottom:18px; text-align:center; width:100%;">
      Research Projects
    </h2>
    <div style="margin-bottom:38px; margin-left:3px;"></div>
    <div class="project-grid">
      {% for project in site.projects limit:6 %}
        <a href="{{ project.url }}" class="project-card">
          <img src="{{ project.image }}" alt="{{ project.title }}" class="project-card-img">
          <div class="project-card-content">
            <div class="project-title">{{ project.title | truncate: 44 }}</div>
            <div style="width:36px; margin-bottom:14px;"></div>
            <div class="project-summary">{{ project.summary | truncate: 96 }}</div>
            <div class="project-date">
              <svg width="17" height="17" fill="#999" viewBox="0 0 20 20" style="margin-right:4px;vertical-align:middle;">
                <path d="M6 2v2H4.5A2.5 2.5 0 0 0 2 6.5v9A2.5 2.5 0 0 0 4.5 18h11A2.5 2.5 0 0 0 18 15.5v-9A2.5 2.5 0 0 0 15.5 4H14V2h-1.5v2h-5V2zM4.5 5h11A1.5 1.5 0 0 1 17 6.5V7H3v-.5A1.5 1.5 0 0 1 4.5 5zm11 12h-11A1.5 1.5 0 0 1 3 15.5V8h14v7.5A1.5 1.5 0 0 1 15.5 17z"/>
              </svg>
              {{ project.start }} ~ {{ project.end }}
            </div>
            <div class="project-readmore">Read More</div>
          </div>
        </a>
      {% endfor %}
    </div>
    <div style="text-align:center; margin-top:30px;">
      <a href="/projects/" style="color:#222; font-weight:600; font-size:1.05em; text-decoration:underline;">View all projects</a>
    </div>
  </div>
</div>

<!-- Recent News Section (Main Page) -->
<div class="recent-news-section" style="background:#fff; padding:15px 0 32px 0; margin:0;">
  <div style="max-width:1000px; margin:0 auto;">
    <h2 style="font-size:1.5em; font-weight:600; margin-bottom:18px; text-align:center;">
      Recent News
    </h2>
    <ul style="font-size:0.9em; color:#262626; margin-bottom:18px; padding-left:18px;">
      {%- assign all_news = "" | split: "" -%}
      {%- for year in site.data.news -%}
        {%- for item in year.items -%}
          {%- assign _item = item | merge: {"year": year.year} -%}
          {%- assign all_news = all_news | push: _item -%}
        {%- endfor -%}
      {%- endfor -%}
      {%- assign all_news = all_news | sort: "order" | reverse -%}
      {%- for item in all_news limit:4 -%}
        <li style="margin-bottom:7px; line-height:1.65;">
          {% if item.date %}
            <b>{{ item.date }}</b>&nbsp;
          {% endif %}
          {{ item.text }}
          {% if item.url %}
            <a href="{{ item.url }}" target="_blank" style="color:#225; margin-left:7px;">{{ item.link_text | default: "[Link]" }}</a>
          {% endif %}
        </li>
      {%- endfor -%}
    </ul>
    <div style="text-align:center; margin-bottom:4px;">
      <a href="/news/" style="font-size:1.05em; color:#222; text-decoration:underline; font-weight:600;">View all news</a>
    </div>
  </div>
</div>

<!-- Contact Us Section (with Lab Logo & Join Us Button 바로 아래에) -->
<div id="contact" class="contact-section-bg" style="padding-bottom: 0;">
  <div style="
      max-width:700px; margin:0 auto; text-align:center;
      display:flex; flex-direction:column; align-items:center; justify-content:center;">
    <h2 style="font-size:1.5em; font-weight:600; margin-bottom:14px;">Contact Us</h2>
    <div style="font-size:1.07em; color:#333; margin-bottom:28px;">
      Have questions? Interested in collaboration?<br>
      Reach out to us below!
    </div>
    <div style="margin-bottom:14px;">
      <strong>Email:</strong>
      <a href="mailto:ssai@tamu.edu" style="color:#2a2a8c; font-weight:500;">ssai@tamu.edu</a>
    </div>
    <div style="margin-bottom:14px;">
      <strong>Address:</strong>
      <span>454 Throckmorton St. College Station, TX 77843</span>
    </div>
<!-- 지도 + 로고 + 버튼 묶음 시작 -->
<div style="display:flex; flex-direction:column; align-items:center; gap:14px; margin: 18px 0 12px 0; width:100%;">
  <!-- 지도 -->
  <iframe
    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d4083.3265252776173!2d-96.34143144218953!3d30.61550314807618!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x86468399d9df49cb%3A0x9841ee504f247ca6!2sNagle%20Hall%2C%20454%20Throckmorton%20St%2C%20College%20Station%2C%20TX%2077843!5e0!3m2!1sen!2sus!4v1751918635059!5m2!1sen!2sus"
    width="320"
    height="320"
    style="border:0; border-radius: 14px;"
    allowfullscreen=""
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade">
  </iframe>

  <!-- 연구실 로고 (아래 margin이 아니라 위에 margin 추가) -->
  <img src="/assets/images/Logo_Blue.png"
       alt="SSAI Lab Logo"
       style="width: 240px; height:auto; margin-top: 32px; margin-bottom: 5px;" />

  <!-- Join Us Button -->
  <a href="https://forms.gle/x9q3HTGj2SFoi5H9A" target="_blank" style="text-decoration: none;">
    <div style="
      display: flex;
      align-items: center;
      padding: 0 34px 0 14px;
      background: #3d4853;
      color: #fff;
      border-radius: 26px;
      height: 54px;
      min-width: 160px;
      font-size: 1.18em;
      font-weight: 600;
      box-shadow: 0 2px 12px rgba(30,30,60,0.12);
      transition: background 0.17s, box-shadow 0.17s;
      cursor: pointer;
      gap: 18px;
      margin-bottom: 8px;"
      onmouseover="this.style.background='#30407a'; this.style.boxShadow='0 6px 28px #b3c2f5';"
      onmouseout="this.style.background='#3d4853'; this.style.boxShadow='0 2px 12px rgba(30,30,60,0.12)';"
    >
      <div style="
        width: 38px; height: 38px; border-radius: 14px; background: #fff;
        display: flex; align-items: center; justify-content: center; margin-right: 12px;">
        <svg width="22" height="22" stroke='#19213b' fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="11" cy="11" r="9"/>
          <polyline points="9,7 13,11 9,15"/>
        </svg>
      </div>
      <span>Join us</span>
    </div>
  </a>
  </div> <!-- 지도+로고+버튼 묶음 끝 -->
</div>   <!-- Contact Us 내부 flex 컨테이너 끝 -->
</div>   <!-- Contact Us Section 전체 끝 -->
