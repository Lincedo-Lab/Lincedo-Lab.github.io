---
title: "Lincedo Lab - Team"
layout: gridlay
excerpt: "Lincedo Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members


## Staff
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a href="{{ member.website }}">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i><br>
  <ul style="overflow: hidden">
  
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


## PhD Students
{% assign number_printed = 0 %}
{% for member in site.data.phd %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a href="{{ member.website }}">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i><br>
  <ul style="overflow: hidden">

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


## Visiting Students and Interns
{% for member in site.data.students %}
<i>{{ member.name }}</i>
{% endfor %}




## Alumni

### Former Team Members
{% for member in site.data.alumni_team_member %}
<i>{{ member.name }}</i>
{% endfor %}


### Former PhD Students
{% for member in site.data.alumni_members %}
<i>{{ member.name }}</i>
{% endfor %}


### Former Master and undergraduate students
{% for member in site.data.alumni_bsc_msc %}
<i>{{ member.name }}</i>
{% endfor %}


### Former Visiting students and Interns 
{% for member in site.data.alumni_visitors %}
<i>{{ member.name }}</i>
{% endfor %}