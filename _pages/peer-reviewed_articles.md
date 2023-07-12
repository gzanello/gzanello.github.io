---
layout: page
permalink: /peer-reviewed_articles/
title: Peer-reviewed articles
description:
nav:
nav_order:
---


<!-- _pages/publications.md -->

TEST TEST



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f publications -q @*[year={{y}}]* %}
{% endfor %}


</div>