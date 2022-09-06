---
layout: page
title: IKIM – the Institute for Artificial Intelligence in Medicine
nav_active: institute
---
Founded in 2019 the Institute for Artificial Intelligence in Medicine (IKIM) brings together researchers from a number of disciplines to perform research, improve patient care and innovate training of tomorrow’s physicians. The institute is part of the [University Medicine Essen](https://www.uk-essen.de) and the [University of Duisburg-Essen](https://www.uni-due.de).

Integrating clinical applications, lab-based research, information technology and computer science, the institute conducts applied and foundational research. We  cover a range of topics, including understanding and reasoning about medical data (including clinical reports, medical imagery, genome data) for e.g.  understanding oncologically relevant patterns in large and complex data, understanding molecular disease mechanisms for e.g. (skin-)cancer, and deciphering the role of the microbiome in health and disease for e.g. viral infection or sepsis.

The institute is constituted by a number of research groups and junior research groups. We use and devise a wide range of cutting-edge methods including (but not limited to) reproducible (bio-)informatics pipelines, virtual and augmented reality, machine learning (e.g.  federated learning, explainable AI), medical data warehousing, viral and bacterial genome sequencing, computer vision, single cell DNA sequencing, natural language understanding and sensor processing. 

To achieve these ambitious goals we develop solutions that can be used by clinicians, hospital staff, and researchers. 

The institute works towards a more individualized, targeted and sustainable future of medical care. At the University of Duisburg-Essen in the heart of the Ruhr area, equal opportunities are actually lived. Our goals: motivate, personalize, network.


{% assign members = '' | split: '' %}
{% for group in site.data.groups %}
    {% assign persons = site.data.people[group.name] | where_exp: "item", "item.roles contains 'board'" %}
    {% assign members = members | concat: persons %}
{% endfor %}

<h2 class="small-bottom-margin">Board</h2>
Prof. Dr. Michael Forsting, Speaker  
N.N., Geschäftsleitung  
{% for group in site.data.groups %} {% assign members = site.data.people[group.name] | where_exp: "item", "item.roles contains 'board'" %} {% for member in members %} {{ member.title }} {{ member.name }}, {% if group.url %} <a href="{{group.url}}"> {% else %} <a href="{{ '/groups/' | append: group.name | relative_url }}"> {% endif %} {{ group.label }}</a><br />{% endfor %}{% endfor %} N.N., scientific staff members  
N.N., Member from the group of the doctoral candidates and students respectively

<h2 class="small-bottom-margin">Steering Group</h2>
{% for p in site.data.people.steering-group %} {{ p.title }} {{ p.name }}, {{ p.affiliation }} <br /> {% endfor %}

<h2 class="small-bottom-margin">Scientific Advisory Board</h2>
{% for p in site.data.people.scientific-advisory-board %} {{ p.title }} {{ p.name }}, {{ p.affiliation }} <br /> {% endfor %}
