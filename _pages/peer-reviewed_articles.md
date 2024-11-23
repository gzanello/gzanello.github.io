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

Collaborating with a range of talented co-authors and leveraging both qualitative and quantitative primary and secondary data, my research focuses on the intersection of agriculture, food, nutrition, and health, predominantly in low-income countries. I examine the food system as a whole, as well as its individual components -- ranging from production to markets and food environments -- and their impact on nutrition and health. Many of my research questions incorporate a strong gender-focused perspective.



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f publications -q @*[year={{y}}]* %}
{% endfor %}

</div>