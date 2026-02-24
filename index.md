---
layout: default
---

<div id="about" class="section"></div>

## About Me

I am **{{ site.profile.role }}** at **{{ site.profile.org }}**.  
My research interests include **(your keywords here)**.  
You can reach me at **{{ site.profile.email }}**.

<div id="news" class="section"></div>

## News

<ul class="news">
{% for item in site.news %}
  <li><span class="date">{{ item.date }}:</span> {{ item.text }}</li>
{% endfor %}
</ul>

<div id="selected-publications" class="section"></div>

## Selected Competitions

{% for p in site.selected_publications %}
<div class="pub-card">
  <img src="{{ p.image | relative_url }}" alt="publication image">
  <div>
    <div class="pub-title">{{ p.title }}</div>
    <div class="pub-meta">{{ p.authors }} · {{ p.venue }}</div>
    {% if p.bullets %}
      <ul class="pub-bullets">
      {% for b in p.bullets %}
        <li>{{ b }}</li>
      {% endfor %}
      </ul>
    {% endif %}
    {% if p.links %}
      <div class="pub-links">
      {% for l in p.links %}
        <a href="{{ l.url }}" target="_blank" rel="noopener">[{{ l.label }}]</a>
      {% endfor %}
      </div>
    {% endif %}
  </div>
</div>

{% endfor %}
