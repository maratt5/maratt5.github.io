---
layout: default
title: Oznamy
pagination: 
  enabled: true
  collection: posts
---

<h3>Tu nájdete aktuálne oznamy pre vlastníkov bytov.</h3>

---

{% for post in paginator.posts %}
<div class="oznam">
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p><em>{{ post.date | date: "%d.%m.%Y" }}</em></p>
  <p>{{ post.excerpt }}</p>
</div>
{% endfor %}

{% if paginator.total_pages > 1 %}
<div class="pagination">
  <div>
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path }}">← Novšie</a>
    {% endif %}
  </div>
  
  <span>Strana {{ paginator.page }} z {{ paginator.total_pages }}</span>

  <div>
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path }}">Staršie →</a>
    {% endif %}
  </div>
</div>
{% endif %}
