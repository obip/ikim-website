---
layout: page
title: IKIM – the Institute for Artificial Intelligence in Medicine
nav_active: institute
---
In 2019, the Institute for Artificial Intelligence in Medicine (IKIM) was one of the first in Germany to start work in this important field of innovation.
 
Our special advantage: We work in close cooperation with the established classical medical disciplines. This is because we are part of the Medical Faculty of the University of Duisburg Essen and the University Hospital Essen and are thus integrated into an excellent scientific environment. An absolute location advantage of our institute. And the IKIM was equipped with five newly established professorships right from the start.

IKIM’s goal is to scientifically analyze and further develop the possibilities of artificial intelligence in medicine, thus making it available for patient care and establishing it in the training of tomorrow’s physicians. For no less than better therapies in the future and thus for the well-being of mankind.

The university medical center in Essen is already a recognized pioneer in the field of digitalization in medicine in Germany. In terms of patient care, Essen has firmly established itself as one of the first Smart Hospitals in Germany. The IKIM will help make NRW the leading region for artificial intelligence in Germany.

__Artificial intelligence will revolutionize medical research.__
  

Using AI, completely unknown highly complex correlations, patterns and causalities can be recognized. University medicine is predestined for this.


__Research is not an end in itself__
 
Research is not an end in itself. The rapid application of scientific findings to patients is an integral part of our concept. Our goal: Personalized medicine becomes possible for the general population and for a wide range of diseases.

__Our goals: motivate, personalize, network__
  
AI will revolutionize medical teaching and create the basis for training all future physicians in a more individual, targeted and sustainable way. At the University of Duisburg-Essen in the heart of the Ruhr area, equal opportunities are actually lived. Our goals: motivate, personalize, network.


{% assign members = '' | split: '' %}
{% for group in site.data.groups %}
    {% assign persons = site.data.people[group.name] | where_exp: "item", "item.roles contains 'board'" %}
    {% assign members = members | concat: persons %}
{% endfor %}

<h2 class="small-bottom-margin">Board</h2>
Prof. Dr. Michael Forsting, Speaker  
N.N., Geschäftsleitung  
{% for group in site.data.groups %} {% assign members = site.data.people[group.name] | where_exp: "item", "item.roles contains 'board'" %} {% for member in members %} {{ member.title }} {{ member.name }}, <a href="{{ '/groups/' | append: group.name | relative_url }}"> {{ group.label }}</a><br />{% endfor %}{% endfor %} N.N., scientific staff members  
N.N., Member from the group of the doctotal candidates and students respectively

<h2 class="small-bottom-margin">Steering Group</h2>
{% for p in site.data.people.steering-group %} {{ p.title }} {{ p.name }}, {{ p.affiliation }} <br /> {% endfor %}

<h2 class="small-bottom-margin">Scientific Advisory Board</h2>
{% for p in site.data.people.scientific-advisory-board %} {{ p.title }} {{ p.name }}, {{ p.affiliation }} <br /> {% endfor %}