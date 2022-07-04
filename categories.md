---
layout: page
title: "Категории"
permalink: /categories/
---
<ul>
{% for categories in site.categories %}
  <li><a href="{{ categories.url }}">{{ categories.categories }}</a></li>
{% endfor %}
</ul>