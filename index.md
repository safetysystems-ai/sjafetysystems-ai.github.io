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

<style>
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
  justify-content: flex-start;
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
  background: #f7f7f7; /* Optional: subtle bg for transparent logos */
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
</style>

<!-- Projects Section (Main Page) -->
<div class="project-section-bg">
  <div class="project-inner-container">    

    <!-- 로고 삽입부 START -->
    <div style="display:flex; justify-content:center; align-items:center; margin-bottom:28px;">
      <img src="/assets/images/Logo_full_Blue.png"
           alt="Safety Systems AI Lab Logo"
           style="width:900px; max-width:98vw; height:auto;" />
    </div>
    <!-- 로고 삽입부 END -->

    <h2 style="font-size:1.5em; font-weight:600; margin-bottom:18px; margin-left:3px;">
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


<!-- Contact Us Section -->
<div id="contact" class="contact-section-bg">
  <div style="max-width:600px; margin:0 auto; text-align:center;">
    <h2 style="font-size:1.5em; font-weight:600; margin-bottom:14px;">Contact Us</h2>
    <div style="font-size:1.07em; color:#333; margin-bottom:28px;">
      Have questions? Interested in collaboration?<br>
      Reach out to us below!
    </div>
    <div style="margin-bottom:18px;">
      <strong>Email:</strong>
      <a href="mailto:ssai@tamu.edu" style="color:#2a2a8c; font-weight:500;">ssai@tamu.edu</a>
    </div>
    <div style="margin-bottom:18px;">
      <strong>Address:</strong>
      <span>454 Throckmorton St. College Station, TX 77843</span>
    </div>
    <div style="margin: 30px 0;">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d4083.3265252776173!2d-96.34143144218953!3d30.61550314807618!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x86468399d9df49cb%3A0x9841ee504f247ca6!2sNagle%20Hall%2C%20454%20Throckmorton%20St%2C%20College%20Station%2C%20TX%2077843!5e0!3m2!1sen!2sus!4v1751918635059!5m2!1sen!2sus"
        width="100%"
        height="300"
        style="border:0; border-radius: 14px;"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade">
      </iframe>
    </div>
  </div>
</div>
