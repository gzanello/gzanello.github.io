---
layout: page
permalink: /teaching/
title: Teaching
description: #Materials for courses you taught. Replace this text with your description.
years: [Current, Past]
nav: true
nav_order: 4
---



<!-- _pages/teaching.md -->

<div id="publicationList" class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f teaching -q @*[year={{y}}]* %}
{% endfor %}

</div>

