---
layout: default
title: ARCHIVE
permalink: /archive/
---
<div class="archive-page">
  <h1>ARCHIVE</h1>
  <p class="tagline">Browse the daily briefing by month.</p>
  {% assign years = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
  {% for year in years %}
    <h2 class="archive-year">{{ year.name }}</h2>
    {% assign months = year.items | group_by_exp: "post", "post.date | date: '%m'" %}
    {% for month in months %}<details class="month-group"><summary>{{ year.name }} / {{ month.name }}</summary><ul class="post-list">{% for post in month.items %}<li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>{% endfor %}</ul></details>{% endfor %}
  {% endfor %}
</div>
