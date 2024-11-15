---
title: "Wimmer Lab - Publications"
layout: gridlay
excerpt: "Wimmer Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

Please see below for an in-progress full list, or use <a class="regtext" href="https://scholar.google.com/citations?hl=en&user=kCGU9rEAAAAJ&view_op=list_works&sortby=pubdate">Google Scholar</a> or <a class="regtext" href="https://pubmed.ncbi.nlm.nih.gov/?term=Wimmer+GE%5BAuthor%5D&sort=date">Pubmed</a>.
<br>

---

## Featured

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
 	<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: right" />
  <p><a class="pub1" href="{{ publi.link.url }}">{{ publi.title }}</a></p>
  <p><em>{{ publi.authors }}</em></p>
  <a class="pub2"> {{ publi.link.display }} </a>
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

---

## Full List (listing in progress)

Alternatively, please see <a class="regtext" href="https://scholar.google.com/citations?hl=en&user=kCGU9rEAAAAJ&view_op=list_works&sortby=pubdate">Google Scholar</a> or <a class="regtext" href="https://pubmed.ncbi.nlm.nih.gov/?term=Wimmer+GE%5BAuthor%5D&sort=date">Pubmed</a>.
<br><br>

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br>

{% endfor %}

