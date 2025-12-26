---
layout: default
title: Archív oznamov
---

# Archív oznamov podľa rokov

{% assign years = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}

{% for year in years %}
  <h2>{{ year.name }}</h2>
  <ul>
    {% for post in year.items %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span style="color:#777;">({{ post.date | date: "%d.%m.%Y" }})</span>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
