---
title: "Julia Stoyanovich - Projects"
layout: gridlay
excerpt: "Julia Stoyanovich - Projects"
sitemap: false
permalink: /projects/
---


## Projects
{% assign number_printed = 0 %}
{% for proi in site.data.projects %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <a href="{{ proi.url }}">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ proi.photo }}" class="img-responsive" width="50%" style="float: left" />
  </a>
  <h4><a href="{{ proi.url }}">{{ proi.name }}</a></h4>
  <em>{{ proi.info }}</em><br>
  <p>{{ proi.description }}</p><br>
  <p>Publications:</p>

  {% if proi.number_pubs == 1 %}
  <a href="{{ proi.pub1.url }}">{{ proi.pub1.display }}</a>
  {% endif %}

  {% if proi.number_pubs == 2 %}
  <a href="{{ proi.pub1.url }}">{{ proi.pub1.display }}</a>,
  <a href="{{ proi.pub2.url }}">{{ proi.pub2.display }}</a>
  {% endif %}

  {% if proi.number_pubs == 3 %}
  <a href="{{ proi.pub1.url }}">{{ proi.pub1.display }}</a>,
  <a href="{{ proi.pub2.url }}">{{ proi.pub2.display }}</a>,
  <a href="{{ proi.pub3.url }}">{{ proi.pub3.display }}</a>
  {% endif %}

  {% if proi.number_pubs == 4 %}
  <a href="{{ proi.pub1.url }}">{{ proi.pub1.display }}</a>,
  <a href="{{ proi.pub2.url }}">{{ proi.pub2.display }}</a>,
  <a href="{{ proi.pub3.url }}">{{ proi.pub3.display }}</a>,
  <a href="{{ proi.pub4.url }}">{{ proi.pub4.display }}</a>
  {% endif %}

  {% if proi.number_pubs == 5 %}
  <a href="{{ proi.pub1.url }}">{{ proi.pub1.display }}</a>,
  <a href="{{ proi.pub2.url }}">{{ proi.pub2.display }}</a>,
  <a href="{{ proi.pub3.url }}">{{ proi.pub3.display }}</a>,
  <a href="{{ proi.pub4.url }}">{{ proi.pub4.display }}</a>,
  <a href="{{ proi.pub5.url }}">{{ proi.pub5.display }}</a>
  {% endif %}
  <br>


  <ul style="overflow: hidden">

  {% if proi.number_funding == 1 %}
  <li> {{ proi.funding1 }}</li>
  {% endif %}

  {% if proi.number_funding == 2 %}
  <li> {{ proi.funding1 }}</li>
  <li> {{ proi.funding2 }}</li>
  {% endif %}

  {% if proi.number_funding == 3 %}
  <li> {{ proi.funding1 }}</li>
  <li> {{ proi.funding2 }}</li>
  <li> {{ proi.funding3 }}</li>
  {% endif %}

  </ul>


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


