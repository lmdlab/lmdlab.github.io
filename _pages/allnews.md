---
title: "Wimmer Lab - News"
layout: textlay
excerpt: "Wimmer Lab at UCL."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
{% endfor %}
