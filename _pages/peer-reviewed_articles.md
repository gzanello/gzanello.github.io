---
layout: page
permalink: /peer-reviewed_articles/
title: Peer-reviewed articles
description:
years: [2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011]
nav:
nav_order:
---


<!-- _pages/publications.md -->

Working with a range of talented co-authors and using both qualitative and quantitative primary and secondary data, I am interested in research at the intersection of agriculture, food, nutrition, and health predominately in low-income countries. I am interested in the food system as a whole, but also in its various components (from production to markets and food environments) and how this affects nutrition and health. My research questions often have a gender-focused angle.



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f publications -q @*[year={{y}}]* %}
{% endfor %}

</div>