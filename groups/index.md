---
layout: default
title: Research Groups
---

{% for group in site.data.groups %}
  {% assign heads = site.data.people | where: "position", "head" %}
  {% assign jrgs = site.data.people | where: "position", "jrg-head" %}
  <h4><a href="/groups/{{ group.name }}">{{ group.label }}</a>
  {% for head in heads %}
    {% if head.group == group.name %}
     {{ head.title }} {{ head.name }}
    {% endif %}
  {% endfor %}
  {% for head in jrgs %}
    {% if head.jrg == group.name %}
     {{ head.title }} {{ head.name }}
    {% endif %}
  {% endfor %}
  </h4>
{% endfor %}
