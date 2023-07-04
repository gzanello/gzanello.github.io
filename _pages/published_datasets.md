---
layout: page
title: Published Datasets
permalink: /published_datasets/
description:
years: [2023, 2019]
nav:
nav_order:
---


<!-- _pages/published_datasets.md -->

TEST TEST



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f published_datasets -q @*[year={{y}}]* %}
{% endfor %}

</div>