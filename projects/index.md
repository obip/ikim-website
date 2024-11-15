---
layout: page
title: "Research Projects"
nav_active: projects
---

{% assign projects = site.posts | where_exp: "item","item.categories contains 'projects'" %}

{% for post in projects %}
* [{{ post.title }}]({{ post.url | relative_url }})<br />{{ post.excerpt }}
{%- endfor -%}
* [Medical Machine Learning Projects](https://mml.ikim.nrw/projects)<br />
  The research group Medical Machine Learning works on developing and deploying cutting-edge machine learning methods with the goal of making a meaningful difference for patients, doctors, and hospital staff.
* [https://ship-ai.ikim.nrw/tour/](Data Integration and AI in Radiology Projects)<br />
  With more than thirty ongoing projects, the Smart Hospital Information Platform (SHIP) AI Team seeks to refine and expedite diagnoses and optimize the quality of patient care by the use of Artificial Intelligence.
* [Annotation Lab](https://annotationlab.ikim.nrw)<br />
  Creating a high-quality dataset is a crucial part of any machine learning project. Annotation Lab Essen, an organizational unit of the Institute for AI in Medicine and part of Essen University Hospital, benefits from the highest medical expertise and specializes in the annotation of medical data (images, text and beyond).
* [Data Integration Centre Essen](https://diz.ikim.nrw)<br />
  As one of the German Medical Informatics Initiative’s (MII) data integration centres (DIC), the DIC Essen was established in recent years to enable the collection, integration, and exchange of medical data in such a way that it can be used effectively in clinical care and research. 
* [Snakemake workflow mangement system](https://snakemake.github.io)<br />
  The Snakemake workflow management system is one of the most widely used frameworks for reproducible data science.
* [Bioconda](https://bioconda.github.io)<br />
  The Bioconda project packages and distributes life science related research software. With over 300 million downloads it is the most widely used resource for automated and reproducible life science related software deployment.