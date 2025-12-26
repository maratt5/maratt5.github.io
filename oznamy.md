---
layout: default
title: Oznamy
---

# Oznamy

Tu nájdete aktuálne oznamy pre vlastníkov bytov.

---

{% for post in site.posts %}
<div class="oznam">
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p><em>{{ post.date | date: "%d.%m.%Y" }}</em></p>
  <p>{{ post.excerpt }}</p>
</div>
{% endfor %}
