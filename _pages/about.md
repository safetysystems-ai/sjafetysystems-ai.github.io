---
layout: page
title: "About"
permalink: /about/
---

<style>
.about-header-image {
  position: relative;
  width: 100vw;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  height: 280px;
  background: url('/assets/images/Kyle_Field_02.jpg') center center / cover no-repeat;
  display: flex;
  align-items: center;
}
.about-header-overlay {
  position: absolute;
  inset: 0;
  background: rgba(30,30,30,0.20); /* overlay_filter: 0.2 */
  z-index: 1;
}
.about-header-text {
  position: relative;
  z-index: 2;
  color: #fff;
  font-size: 2.5em;
  font-weight: 700;
  margin-left: 7vw;
  margin-right: auto;
  text-shadow: 0 2px 16px rgba(0,0,0,0.14);
  letter-spacing: 1px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
  height: 100%;
  text-align: left;
}
@media (max-width: 800px) {
  .about-header-image { height: 160px; }
  .about-header-text { font-size: 1.5em; margin-left: 14px;}
}
</style>

<!-- About Header Section -->
<div class="about-header-image">
  <div class="about-header-overlay"></div>
  <div class="about-header-text">
    <span>About</span>
  </div>
</div>

<!-- About 본문 -->
<div style="max-width:950px; margin:36px auto 0 auto; display:flex; flex-direction:column; align-items:center;">
  <img src="/assets/images/Logo_full_Blue.png"
       alt="Safety Systems AI Lab Logo"
       style="width:900px; max-width:98vw; height:auto; margin-bottom:30px;" />
  <div style="font-size:1.15em; color:#3d4853; font-weight:500; text-align:center; max-width:800px; margin-bottom:15px;">
    Augmenting the Human Cognitive and Physical Capabilities for Safety
  </div>
  <div style="font-size:1.07em; color:#61697a; text-align:center; max-width:900px; margin-bottom:40px;">
    The Safety Systems.AI Lab is dedicated to advancing safety in both workplaces and everyday life by augmenting human cognitive and physical capabilities to prevent accidents and injuries. Our research integrates AI, VR/AR, and advanced sensing technologies to transform how people learn about, manage, and respond to safety risks. By combining insights from cognitive science, engineering, and emerging technologies, we develop intelligent systems that enhance awareness, decision-making, and the ability to respond effectively to safety challenges across diverse environments.
  </div>
</div>
