---
layout: page
title: "News"
permalink: /news/
---

<h2 style="font-size:1.5em; font-weight:700; margin-bottom:24px; text-align:center;">
  News and Updates
</h2>
<div class="news-list">
  <ul style="margin-bottom:22px; padding-left:30px;">
    {%- assign all_news = "" -%}
    {%- for year in site.data.news -%}
      {%- for item in year.items -%}
        {%- assign all_news = all_news | append: "|" | append: item.order | append: "~~~" | append: item.date | append: "~~~" | append: item.text | append: "~~~" | append: item.url | append: "~~~" | append: item.link_text -%}
      {%- endfor -%}
    {%- endfor -%}
    {%- assign all_news = all_news | remove_first: "|" | split: "|" -%}
    {%- assign all_news = all_news | sort: "" | reverse -%}

    {%- for news_item in all_news -%}
      {%- assign parts = news_item | split: "~~~" -%}
      <li style="margin-bottom:9px; font-size:1em; color:#252525; list-style-type: disc;">
        <span style="font-weight:600;">{{ parts[1] }}</span>
        <span style="margin-left:0.3em;">
          {% if parts[3] and parts[3] != "" %}
            <a href="{{ parts[3] }}" target="_blank" style="color:#225;">
              {{ parts[2] }}
            </a>
          {% else %}
            {{ parts[2] }}
          {% endif %}
        </span>
      </li>
    {%- endfor -%}
  </ul>
</div>
