---
layout: default
title: Oznamy
pagination: true
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

<div style="margin-top:2rem; font-weight:600;">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" style="margin-right:1rem;">← Novšie</a>
  {% endif %}

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}">Staršie →</a>
  {% endif %}
</div>
