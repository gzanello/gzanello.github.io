---
layout: page
title: Published datasets
permalink: /published_datasets/
description:
years: [2023, 2019]
nav:
nav_order:
---


<!-- _pages/published_datasets.md -->



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f published_datasets -q @*[year={{y}}]* %}
{% endfor %}

</div>