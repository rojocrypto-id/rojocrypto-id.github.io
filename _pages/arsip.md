---
layout: page
title: Arsip
---

<div id="archives">
  {% for category in site.categories %}
    <div class="archive-group">
      {% capture category_name %}{{ category | first }}{% endcapture %}
      <h3 id="{{ category_name | slugify }}">{{ category_name }}</h3>
      {% for post in site.categories[category_name] %}
        <article class="archive-item">
          <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
        </article>
      {% endfor %}
    </div>
  {% endfor %}
</div>