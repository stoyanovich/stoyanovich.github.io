---
title: "Julia Stoyanovich - Students"
layout: gridlay
excerpt: "Julia Stoyanovich - Students"
sitemap: false
permalink: /students/
---

## PhD Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}></i><br>
  <i>{{ member.org }}</i>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Past Members

### PhD Student
<ul style="overflow: hidden">
<li> Vera Zaychik Moffitt </li>
</ul>

### Visiting scholar
<ul style="overflow: hidden">
<li> Lovro Ilijasic </li>
</ul>

### Bachelor and Master Students
<ul style="overflow: hidden">
<li> Shishir Kharel </li>
<li> Matthew Bucci </li>
<li> Simona D'Avanzo </li>
<li> Charles Gilliam </li>
<li> Akhil Kapoor </li>
<li> Halima Olapade </li>
<li> Sanjana Raj </li>
</ul>

## External Collaborators
<ul style="overflow: hidden">
<li> Serge Abiteboul (INRIA & ENS Cachan, France) </li>
<li> Benny Kimelfeld (Technion, Israel) </li>
<li> Gerome Miklau (UMass, Amherst, USA) </li>
<li> Batya Kenig (Technion, Israel) </li>
</ul>