---
layout: page
title: "Категории"
permalink: /categories/
---
<ul>
{% for categories in post.categories %}
  <li><a href="{{ categories.url }}">{{ categories.categories }}</a></li>
{% endfor %}
</ul>