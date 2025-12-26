---
layout: default
title: Oznamy
pagination: 
  enabled: true
  collection: posts
---

# Oznamy

Tu nájdete aktuálne oznamy pre vlastníkov bytov.

---

{% for post in paginator.posts %}
<div class="oznam">
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p><em>{{ post.date | date: "%d.%m.%Y" }}</em></p>
  <p>{{ post.excerpt }}</p>
</div>
{% endfor %}

{% if paginator.total_pages > 1 %}
<div style="margin-top:2rem; font-weight:600;">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" style="margin-right:1rem;">← Novšie</a>
  {% endif %}
  
  <span style="color:#666;">Strana {{ paginator.page }} z {{ paginator.total_pages }}</span>

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" style="margin-left:1rem;">Staršie →</a>
  {% endif %}
</div>
{% endif %}
