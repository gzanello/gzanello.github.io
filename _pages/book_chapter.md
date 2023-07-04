---
layout: page
title: Book Chapters
permalink: /book_chapter/
description:
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011]
nav: 
nav_order:
---


<!-- _pages/book_chapter.md -->

TEST TEST



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f book_chapter -q @*[year={{y}}]* %}
{% endfor %}

</div>