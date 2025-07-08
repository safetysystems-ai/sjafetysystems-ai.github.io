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
      {% for year in news2025 %}
        {% for item in year.items %}
          <li style="margin-bottom:7px;">
            {% if item.date %}
              <b>{{ item.date }}</b>
            {% endif %}
            {% if item.url %}
              <a href="{{ item.url }}" target="_blank" style="color:#2233ee;">
                {{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}
              </a>
            {% else %}
              {{ item.text | markdownify }}
            {% endif %}
          </li>
        {% endfor %}
      {% endfor %}
    </ul>

