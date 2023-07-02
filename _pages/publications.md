---
layout: page
permalink: /publications/
title: Publications
description:
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010, 2009]
nav: false
nav_order: 2
---


<script>
function filterSubject(filter) {
  var list = document.getElementById("publicationList");
  var rows = list.getElementsByClassName("row");
  
  // Loop through all rows, hide those which don't match the selected filter
  for (i = 0; i < rows.length; i++) {
    var primaryClass = rows[i].getElementsByClassName("category-tag")[0];
	if (primaryClass.textContent.indexOf(filter) > -1) {
        rows[i].style.display = "";
    } else {
        rows[i].style.display = "none";
    }
  }
  
  // Loop through all sections, hide those which are empty
  var years = list.getElementsByClassName("year");
  for (i = 0; i < years.length; i++) {
    var count = 0;
    for (j = 0; j < rows.length; j++) {
	  var section_tag = rows[j].getElementsByClassName("section-tag")[0];
	  if (section_tag.textContent == years[i].textContent && rows[j].style.display == "") { count++; }
	}
	if (count != 0) {
	  years[i].style.display = "";
	} else {
	  years[i].style.display = "none";
	}
  }
}
</script>


TEST TEXT


<center>
<p>
<abbr class="{{site.data.badge_colors['red']}}" onclick="filterSubject('')" style="cursor: pointer;">all</abbr>&ensp;
<abbr class="{{site.data.badge_colors['darkgrey']}}" onclick="filterSubject('article')" style="cursor: pointer;">Articles</abbr>&ensp;
<abbr class="{{site.data.badge_colors['darkgrey']}}" onclick="filterSubject('techreport')" style="cursor: pointer;">Policy Reports</abbr>
<abbr class="{{site.data.badge_colors['darkgrey']}}" onclick="filterSubject('manual')" style="cursor: pointer;">Datasets</abbr>
</p>
</center>



<div id="publicationList" class="publications">
 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>