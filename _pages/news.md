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
.news-month {
  font-size: 2.3em;
  font-weight: 800;
  color: #2c2e30;
  letter-spacing: 0.01em;
  line-height: 1;
  margin-bottom: 6px;
}
.news-year {
  font-size: 1.09em;
  color: #7a7a7a;
  font-weight: 500;
  letter-spacing: 0.04em;
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
  .news-month { font-size: 1.5em; margin-bottom:0; margin-right: 16px;}
  .news-year { font-size: 1em; }
  .news-content-col { padding-left:0; }
}
</style>

<h2 style="font-size:1.5em; font-weight:700; margin-bottom:24px; text-align:center;">
  News and Updates
</h2>
<div class="news-flex-list">
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
    {%- assign order = parts[0] -%}
    {%- assign year = order | split: "-" | first -%}
    {%- assign month_num = order | split: "-" | last -%}
    {%- assign months = "Jan,Feb,Mar,Apr,May,Jun,Jul,Aug,Sep,Oct,Nov,Dec" | split: "," -%}
    {%- assign month_label = months[month_num | minus: 1] -%}
    <div class="news-flex-item">
      <div class="news-date-col">
        <div class="news-month">{{ month_label }}</div>
        <div class="news-year">{{ year }}</div>
      </div>
      <div class="news-content-col">
        {{ parts[2] }}
        {% if parts[3] and parts[3] != "" %}
          <a class="news-details-link" href="{{ parts[3] }}" target="_blank">
            {{ parts[4] | default: '[Details]' }}
          </a>
        {% endif %}
      </div>
    </div>
  {%- endfor -%}
</div>
