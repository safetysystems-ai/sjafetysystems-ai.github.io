---
layout: page
title: Members
permalink: /members/
---

<!-- 메인 Faculty (PI) -->
## Members

{% for m in site.data.members.faculty %}
<div style="max-width: 900px; margin: 0 auto; padding-left: 60px;">
  <img src="{{ m.image }}" style="width:140px; height:140px; border-radius: 100px; margin-right: 28px; object-fit:cover; border: 2px solid #eee;">
  <div>
    <h2 style="margin-bottom: 0.5em;">{{ m.name }}</h2>
    <div><strong>{{ m.title }}</strong></div>
    <div>
      {% for pos in m.positions %}
        <div>{{ pos }}</div>
      {% endfor %}
    </div>
    <div style="margin-top:8px;"><em>{{ m.education }}</em></div>
    <div style="margin-top:8px;"><strong>Awards:</strong>
      <ul>
        {% for a in m.awards %}
          <li>{{ a }}</li>
        {% endfor %}
      </ul>
    </div>
    <div>
      {% if m.linkedin %}
        <a href="{{ m.linkedin }}">LinkedIn</a>
      {% endif %}
      {% if m.website %}
        | <a href="{{ m.website }}">Website</a>
      {% endif %}
    </div>
  </div>
</div>
{% endfor %}

---


## Current Members

<div style="max-width: 900px; margin: 0 auto; padding-left: 60px;">
{% for c in site.data.members.current %}
  <div style="width:220px; background:#f6f7fa; margin:10px; padding:10px; border-radius:12px; text-align:center;">
    <img src="{{ c.image }}" style="width:65px; height:65px; border-radius: 50%;">
    <div style="margin-top:8px; font-weight: bold;">{{ c.name }}</div>
    <div style="font-size:0.95em;">{{ c.title }}</div>
    <div style="font-size:0.9em; color:#444;">{{ c.description }}</div>
  </div>
{% endfor %}
</div>
