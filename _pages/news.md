---
layout: page
title: "News"
permalink: /news/
---

<h2 style="font-size:2em; font-weight:700; margin-bottom:18px;">News and Updates</h2>
<div class="news-list">
  {% assign news_years = site.data.news | sort: 'year' | reverse %}
  {% for year in news_years %}
    <h3 style="margin-top:24px;">{{ year.year }}</h3>
    <ul>
      {% for item in year.items %}
        <li>
          {% if item.date %}
            <span style="font-weight:600;">{{ item.date }}</span>
          {% endif %}
          {{ item.text | markdownify }}
        </li>
      {% endfor %}
    </ul>
  {% endfor %}
</div>
