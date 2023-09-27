---
layout: page
title: Book chapters
permalink: /book_chapter/
description:
years: [2023, 2022, 2020]
nav: 
nav_order:
---


<!-- _pages/book_chapter.md -->



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f book_chapter -q @*[year={{y}}]* %}
{% endfor %}

</div>
