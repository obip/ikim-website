---
layout: page
title: "Research Projects"
nav_active: projects
---

{% assign projects = site.posts | where_exp: "item","item.categories contains 'projects'" %}
<ul>
  {% for post in projects %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br />
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>