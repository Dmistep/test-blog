---
layout: page
title: "Категории"
permalink: /categories/
---
<ul>
{% for category in posts.categories %}
  <li><a href="{{ category.url }}">{{ category.categories }}</a></li>
{% endfor %}
</ul>