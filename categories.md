---
layout: post
title: "Категории"
permalink: /categories/
---
<ul>
{% for post in site.posts %}
  <li><a href="{{ post.url | relative_url}}">{{ post.categories | escape}}</a></li>
{% endfor %}
</ul>