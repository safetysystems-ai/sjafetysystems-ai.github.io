---
layout: page
title: "News"
permalink: /news/
---

<h2 style="font-size:2.2em; font-weight:700; margin-bottom:24px;">News and Updates</h2>
<div class="news-list">
  {% assign news_years = site.data.news | sort: 'year' | reverse %}
  {% for year in news_years %}
    <h3 style="font-size:1.19em; font-weight:700; margin-bottom:9px; margin-top:32px;">{{ year.year }}</h3>
    <ul style="margin-bottom:22px; padding-left:30px;">
      {% for item in year.items %}
        <li style="margin-bottom:9px; font-size:1em; color:#252525; list-style-type: disc;">
          <span style="font-weight:600;">{{ item.date }}</span>
          <span style="margin-left:0.3em;">
            {% if item.url %}
              <a href="{{ item.url }}" target="_blank" style="color:#225;">
                {{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}
              </a>
            {% else %}
              {{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}
            {% endif %}
          </span>
        </li>
      {% endfor %}
    </ul>
  {% endfor %}
</div>

