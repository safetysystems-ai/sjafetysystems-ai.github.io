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
  background: #868e96;
  color: #fff;
  border: none;
  border-radius: 7px 7px 0 0;
  font-weight: 600;
  font-size: 1.05em;
  padding: 12px 28px;
  cursor: pointer;
  opacity: 0.85;
}
.pub-cat-btn.active, .pub-cat-btn:hover {
  background: #495057;
  opacity: 1;
}
.pub-list {
  max-width: 1100px;
  margin: 0 auto 60px auto;
  background: #fff;
  border-radius: 8px;
  padding: 30px 40px;
  font-size: 0.8em;
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
<ol id="pub-all" class="pub-list">
  <div style="font-size:1em; margin-bottom:20px;">
    <i>*Corresponding author, **Graduate student or postdoctoral scholar advisee</i>
  </div>
  {% assign all_journals = site.data.publications.journal %}
  {% assign all_confs = site.data.publications.conference %}
  {% for pub in all_journals %}
    <li>
      {{ pub.authors | replace: 'Kim, N.', '<b>Kim, N.</b>' }} ({{ pub.year }}).
      “{{ pub.title }}”
      {{ pub.journal }}
      {% if pub.link %}
        <a href="{{ pub.link }}" target="_blank" style="margin-left:6px; color:#2563eb;">[Link]</a>
      {% endif %}
    </li>
  {% endfor %}
  {% for pub in all_confs %}
    <li>
      {{ forloop.index | plus: all_journals.size }}. 
      {{ pub.authors | replace: 'Kim, N.', '<b>Kim, N.</b>' }} ({{ pub.year }}).
      “{{ pub.title }}”
      {{ pub.conference }}
      {% if pub.link %}
        <a href="{{ pub.link }}" target="_blank" style="margin-left:6px; color:#2563eb;">[Link]</a>
      {% endif %}
    </li>
  {% endfor %}
</ol>

  <!-- Journal Only -->
<ol id="pub-journal" class="pub-list" style="display:none;">
  <div style="font-size:1em; margin-bottom:20px;">
    <i>*Corresponding author, **Graduate student or postdoctoral scholar advisee</i>
  </div>
  {% for pub in site.data.publications.journal %}
    <li>
      {{ pub.authors | replace: 'Kim, N.', '<b>Kim, N.</b>' }} ({{ pub.year }}).
      “{{ pub.title }}”
      {{ pub.journal }}
      {% if pub.link %}
        <a href="{{ pub.link }}" target="_blank" style="margin-left:6px; color:#2563eb;">[Link]</a>
      {% endif %}
    </li>
  {% endfor %}
</ol>

<!-- Conference Only -->
<ol id="pub-conference" class="pub-list" style="display:none;">
  <div style="font-size:1em; margin-bottom:20px;">
    <i>*Corresponding author, **Graduate student or postdoctoral scholar advisee</i>
  </div>
  {% for pub in site.data.publications.conference %}
    <li>
      {{ pub.authors | replace: 'Kim, N.', '<b>Kim, N.</b>' }} ({{ pub.year }}).
      “{{ pub.title }}”
      {{ pub.conference }}
      {% if pub.link %}
        <a href="{{ pub.link }}" target="_blank" style="margin-left:6px; color:#2563eb;">[Link]</a>
      {% endif %}
    </li>
  {% endfor %}
</ol>

<script>
function showPubs(cat) {
  document.getElementById('pub-all').style.display = cat === 'all' ? '' : 'none';
  document.getElementById('pub-journal').style.display = cat === 'journal' ? '' : 'none';
  document.getElementById('pub-conference').style.display = cat === 'conference' ? '' : 'none';
  var btns = document.querySelectorAll('.pub-cat-btn');
  btns.forEach(function(b, i){
    b.classList.remove('active');
    if ((cat === 'all' && i===0) || (cat==='journal' && i===1) || (cat==='conference' && i===2)) b.classList.add('active');
  });
}
</script>
