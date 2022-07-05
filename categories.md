---
layout: post
title: "Категории"
permalink: /categories/
---
<!-- <ul>
{% for post in site.posts %}
  <li><a href="{{ post.url | relative_url}}">{{ post.categories | first}}</a></li>
{% endfor %}
</ul> -->


<div id="archives" class="">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>
    <div class="container">
<div class="row">
<div class="col-md-2">
    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
</div>
      </div>
  </div>
{% endfor %}
</div>


