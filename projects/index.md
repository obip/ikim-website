---
layout: page
title: "Research Projects"
---

{% assign projects = site.posts | where_exp: "item","item.categories contains 'projects'" %}
<ul>
  {% for post in projects %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>