---
layout: page
title: Book chapters
permalink: /book_chapter/
description:
group_by: year
group_order: descending
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