---
layout: page
title: "Категории"
permalink: /categories/
---
<ul>
{% for post in site.posts %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>