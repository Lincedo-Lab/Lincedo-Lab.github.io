---
title: "Lincedo Lab - Publications"
layout: gridlay
excerpt: "Lincedo Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

(For a selected publications see [below](#selected-publications) or go to [Google Scholar](https://scholar.google.nl/citations?user=Tp1RdIQAAAAJ&hl=en).)

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p><em>{{ publi.authors }}</em></p>
  <p><a href="{{ publi.url }}">{{ publi.display }}</a></p>
  <p>{{ publi.description }}</p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> <b><font color="#FF0000">{{ publi.news2 }}</font></b></p>
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


## Selected Publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.url }}">{{ publi.display }}</a>   <b><font color="#FF0000">{{ publi.news2 }}</font></b><br />

{% endfor %}

<p> &nbsp; </p>
