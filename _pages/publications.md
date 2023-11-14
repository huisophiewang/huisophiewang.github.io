---
layout: page
permalink: /publications/
title: publications
description: 
preprint_years: [2023]
paper_years: [2023, 2021, 2017]
nav: true
---

<div class="publications">

<h1>preprints</h1>
{% bibliography -f preprints -q @*[status=review]* %}
{% bibliography -f preprints -q @*[status=maj-revision]* %}
{% bibliography -f preprints -q @*[status=min-revision]* %}

{% for y in page.preprint_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

<h1>published</h1>
{% for y in page.paper_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
