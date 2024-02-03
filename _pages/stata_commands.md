---
layout: page
title: Stata commands
permalink: /stata_commands/
description:
years: [2024]
nav:
nav_order:
---


<!-- _pages/stata_commands.md -->



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f stata_commands -q @*[year={{y}}]* %}
{% endfor %}

</div>