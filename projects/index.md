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
  <li>
    <a href="https://mml.ikim.nrw/projects/">Medical Machine Learning Projects</a><br />
    The research group Medical Machine Learning works on developing and deploying cutting-edge machine learning methods with the goal of making a meaningful difference for patients, doctors, and hospital staff.
  </li>
  <li>
    <a href="https://ship-ai.ikim.nrw/tour/">Data Integration and AI in Radiology Projects</a><br />
    With more than thirty ongoing projects, the Smart Hospital Information Platform (SHIP) AI Team seeks to refine and expedite diagnoses and optimize the quality of patient care by the use of Artificial Intelligence. 
  </li>
  <li>
      <a href="https://annotationlab.ikim.nrw/">Annotation Lab</a><br />
      Creating a high-quality dataset is a crucial part of any machine learning project. Annotation Lab Essen, an organizational unit of the Institute for AI in Medicine and part of Essen University Hospital, benefits from the highest medical expertise and specializes in the annotation of medical data (images, text and beyond).
  </li>
  <li>
      <a href="https://diz.ikim.nrw/">Data Integration Centre Essen</a><br />
      As one of the German Medical Informatics Initiative’s (MII) data integration centres (DIC), the DIC Essen was established in recent years to enable the collection, integration, and exchange of medical data in such a way that it can be used effectively in clinical care and research. 
  </li>
</ul>