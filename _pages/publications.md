---
layout: page
title: "Publications"
permalink: /publications/
---

<style>
.pub-cat-btns {
  display: flex;
  gap: 12px;
  justify-content: center;
  margin-bottom: 32px;
}
.pub-cat-btn {
  background: #888a94;
  color: #fff;
  border: none;
  border-radius: 7px 7px 0 0;
  font-weight: 600;
  font-size: 0.8em;
  padding: 12px 28px;
  cursor: pointer;
  opacity: 0.88;
}
.pub-cat-btn.active, .pub-cat-btn:hover {
  background: #44454f;
  opacity: 1;
}
.pub-list {
  max-width: 1100px;
  margin: 0 auto 60px auto;
  background: #fff;
  border-radius: 8px;
  padding: 30px 40px;
  font-size: 1.11em;
}
.pub-list li { margin-bottom: 28px; }
@media (max-width: 850px) {
  .pub-list { padding: 20px 6vw; }
}
</style>

<div style="padding:44px 0 0 0;">
  <div class="pub-cat-btns">
    <button class="pub-cat-btn active" onclick="showPubs('all')">All Papers</button>
    <button class="pub-cat-btn" onclick="showPubs('journal')">Peer-reviewed Journal Publications</button>
    <button class="pub-cat-btn" onclick="showPubs('conference')">Peer-reviewed Conference Publications</button>
  </div>

  <!-- All Papers List -->
  <div style="font-size:0.8em; margin-bottom:20px;">
    <b>Graduate student or postdoctoral scholar advisee, <i>*Corresponding author</i></b>
  </div>
  <ol id="pub-all" class="pub-list">
    {% assign all_journals = site.data.publications.journal %}
    {% assign all_confs = site.data.publications.conference %}
    {% for pub in all_journals %}
      <li>
        {{ forloop.index }}. 
        {{ pub.authors | replace: 'Kim, N.', '<b>Kim, N.</b>' }} ({{ pub.year }}).
        <b>“{{ pub.title }}”</b>
        {{ pub.journal }}
        {% if pub.link %}
          <a href="{{ pub.link }}" target="_blank" style="margin-left:6px; color:#211dac;">[Link]</a>
        {% endif %}
      </li>
    {% endfor %}
    {% for pub in all_confs %}
      <li>
        {{ forloop.index | plus: all_journals.size }}. 
        {{ pub.authors | replace: 'Kim, N.', '<b>Kim, N.</b>' }} ({{ pub.year }}).
        <b>“{{ pub.title }}”</b>
        {{ pub.conference }}
        {% if pub.link %}
          <a href="{{ pub.link }}" target="_blank" style="margin-left:6px; color:#211dac;">[Link]</a>
        {% endif %}
      </li>
    {% endfor %}
  </ol>
  <!-- 이하 동일 (journal, conference) 부분도 ol/li 구조 위와 같이 div 바깥! -->
