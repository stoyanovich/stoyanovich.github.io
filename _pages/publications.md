---
title: "Julia Stoyanovich - Publications"
layout: gridlay
excerpt: "Julia Stoyanovich - Publications"
sitemap: false
permalink: /publications/
---


# Publications
Jump to [full-list](#full-list), [patents](#patents) and [thesis](#thesis)

## Highlights

{% assign number_printed = 0 %}
{% for publi in site.data.publications %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List

{% for publi in site.data.publications %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

## Patents
  - "Automatically and Adaptively Determining Execution Plans for Queries with Parameter Markers", Wei Fan, Guy Lohman, Volker Markl, Nimrod Megiddo, Jun Rao, David Simmen, Julia Stoyanovich. United States Patent: 7,958,113 (June 7, 2011); Assignee: IBM.
  - "Social Behavior Analysis and Inferring Social Networks for a Recommendation System", Sihem Amer-Yahia, Evgeniy Gabrilovich, Bo Pang, Julia Stoyanovich, Cong Yu. United States Patent: 8,073,794 (December 6, 2011); Assignee: Yahoo! Inc.

## Thesis
"Search and Ranking in Semantically Rich Applications", Columbia University PhD Thesis, 10/2009, [pdf](https://www.cs.drexel.edu/~julia/documents/thesis.pdf)
