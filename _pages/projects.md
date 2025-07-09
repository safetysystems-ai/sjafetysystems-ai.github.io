---
layout: page
title: Projects
permalink: /projects/
---

<style>
.project-card,
.project-card *,
.project-card a {
  text-decoration: none;
}
.project-section-bg {
  background: #f5f6f7;
  min-height: unset;
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  padding: 30px 0 10px 0;
}
.project-section-bg-completed {
  background: #faf9f8;
  min-height: unset;
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  padding: 30px 0 10px 0;
}
.project-inner-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 32px;
}
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 24px;
  justify-items: start; /* 카드 가운데 정렬 */
  justify-content: start; /* 전체 컨테이너 왼쪽 정렬 */
}

.project-card {
  width: 320px;
  background: #fff;
  border-radius: 16px;
  box-shadow: 0 4px 18px #e0e0e0;
  transition: box-shadow .17s, transform .11s;
  display: block;
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
  font-size: 0.80em;
  margin-bottom: 4px;
  letter-spacing: 0.01em;
}
@media (max-width: 850px) {
  .project-inner-container { max-width: 95vw; }
  .project-card { width: 96vw; max-width: 380px;}
}

.section-title {
  text-align: center;
  color: inherit;
  font-weight: 600;
  font-size: 1.5em;
  margin-bottom: 8px;
  margin-top: 0;
  letter-spacing: 0.01em;
}
.projects-header-image {
  position: relative;
  width: 100vw;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  height: 320px;  /* 필요시 조정 */
  background: url('/assets/images/Aggie_Park.jpg') center center / cover no-repeat;
  display: flex;
  align-items: center;
}
.projects-header-overlay {
  position: absolute;
  inset: 0;
  background: rgba(30,30,30,0.20); /* overlay_filter: 0.2 와 유사 */
  z-index: 1;
}
.projects-header-text {
  position: relative;
  z-index: 2;
  color: #fff;
  font-size: 2.5em;
  font-weight: 700;
  margin-left: 5vw;   /* 왼쪽 정렬, 값 조절 가능 */
  text-shadow: 0 2px 16px rgba(0,0,0,0.14);
  letter-spacing: 1px;
}
@media (max-width: 800px) {
  .projects-header-image { height: 180px; }
  .projects-header-text { font-size: 1.8em; margin-left: 18px;}
}

</style>

<div class="projects-header-image">
  <div class="projects-header-overlay"></div>
  <div class="projects-header-text">
    <span>Research Projects</span>
  </div>
</div>


<!-- Project in Progress Section -->
<div class="project-section-bg">
  <div class="project-inner-container">
    <h2 class="section-title">Projects in Progress</h2>
    <div style="margin-bottom:38px; margin-left:3px;"></div>
    <div class="project-grid">
      {% assign ongoing_projects = site.projects | where: "status", "ongoing" %}
      {% for project in ongoing_projects %}
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
  </div>
</div>

<!-- Completed Projects Section -->
<div class="project-section-bg-completed">
  <div class="project-inner-container">
    <h2 class="section-title">Completed Projects</h2>
    <div style="margin-bottom:38px; margin-left:3px;"></div>
    <div class="project-grid">
      {% assign completed_projects = site.projects | where: "status", "completed" %}
      {% for project in completed_projects %}
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
  </div>
</div>

