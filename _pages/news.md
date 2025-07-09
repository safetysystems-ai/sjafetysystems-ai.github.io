---
layout: page
title: "News"
permalink: /news/
---

<style>
.news-flex-list {
  width: 100%;
  max-width: 1000px;
  margin: 0 auto 32px auto;
  padding: 0;
}
.news-flex-item {
  display: flex;
  border-bottom: 1.2px solid #ececec;
  padding: 28px 0 24px 0;
  align-items: flex-start;
}
.news-date-col {
  width: 90px;
  min-width: 75px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  font-family: 'Segoe UI', Arial, sans-serif;
  flex-shrink: 0;
}
.news-day {
  font-size: 2.3em;
  font-weight: 800;
  color: #2c2e30;
  letter-spacing: 0.01em;
  line-height: 1;
  margin-bottom: 2px;
}
.news-month-year {
  font-size: 1.09em;
  color: #7a7a7a;
  font-weight: 500;
  letter-spacing: 0.04em;
  text-align: center;
}
.news-content-col {
  flex: 1;
  padding-left: 22px;
  font-size: 1.04em;
  line-height: 1.72;
  color: #232323;
}
.news-details-link {
  color: #225;
  margin-left: 9px;
  font-weight: 500;
  font-size: 0.98em;
}
@media (max-width: 650px) {
  .news-flex-item { flex-direction: column; padding: 20px 0 14px 0;}
  .news-date-col { flex-direction: row; width: 100%; margin-bottom: 8px;}
  .news-day { font-size: 1.5em; margin-bottom:0; margin-right: 16px;}
  .news-month-year { font-size: 1em; }
  .news-content-col { padding-left:0; }
}
</style>

<!-- News Header Section -->
<div style="
  position: relative; 
  width: 100vw; 
  left: 50%; 
  right: 50%; 
  margin-left: -50vw; 
  margin-right: -50vw;
  height: 280px;
  overflow: hidden;">
  <img src="/assets/images/Academic_Sunset.jpg" alt="News Banner" 
    style="width: 100%; height: 100%; object-fit: cover; filter: brightness(0.7);" />
  <div style="
    position: absolute; 
    top: 52%; left: 6vw; 
    transform: translateY(-50%);
    color: #fff; 
    font-size: 2.6em; 
    font-weight: 800; 
    text-shadow: 0 3px 16px rgba(0,0,0,0.30);
    letter-spacing: 0.01em;">
    News
  </div>
</div>


<h2 style="font-size:1.5em; font-weight:700; margin-bottom:24px; text-align:center;">
  News and Updates
</h2>
<div class="news-flex-list">
  {%- assign all_news = "" -%}
  {%- for year in site.data.news -%}
    {%- for item in year.items -%}
      {%- assign all_news = all_news | append: "|" | append: item.date_full | append: "~~~" | append: item.text | append: "~~~" | append: item.url | append: "~~~" | append: item.link_text -%}
    {%- endfor -%}
  {%- endfor -%}
  {%- assign all_news = all_news | remove_first: "|" | split: "|" -%}
  {%- assign all_news = all_news | sort: "" | reverse -%}
  {%- for news_item in all_news -%}
    {%- assign parts = news_item | split: "~~~" -%}
    {%- assign date_full = parts[0] -%}
    {%- assign text = parts[1] -%}
    {%- assign url = parts[2] -%}
    {%- assign link_text = parts[3] -%}
    {%- assign year = date_full | slice: 0, 4 -%}
    {%- assign month_num = date_full | slice: 5, 2 -%}
    {%- assign day = date_full | slice: 8, 2 -%}
    {%- assign months = "Jan,Feb,Mar,Apr,May,Jun,Jul,Aug,Sep,Oct,Nov,Dec" | split: "," -%}
    {%- assign month_label = months[month_num | minus: 1] -%}
    <div class="news-flex-item">
      <div class="news-date-col">
        <div class="news-day">{{ day }}</div>
        <div class="news-month-year">{{ year }}.{{ month_num }}</div>
      </div>
      <div class="news-content-col">
        {{ text }}
        {% if url and url != "" %}
          <a class="news-details-link" href="{{ url }}" target="_blank">
            {{ link_text | default: '[Details]' }}
          </a>
        {% endif %}
      </div>
    </div>
  {%- endfor -%}
</div>
