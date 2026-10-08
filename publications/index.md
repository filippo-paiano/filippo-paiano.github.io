---
layout: default
title: Publications
---
{% assign groups = "article:Journal articles,preprint:Preprints" | split: "," %}
{% for g in groups %}
  {% assign pair = g | split: ":" %}
  {% assign items = site.data.publications | where: "type", pair[0] | sort: "year" | reverse %}
  {% if items.size > 0 %}
<h2>{{ pair[1] }}</h2>
<ul class="voci">
  {% for p in items %}
  <li>
    {% if p.link and p.link != "" %}<a href="{{ p.link }}">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}<br>
    <span class="tenue">{{ p.authors }}. {{ p.venue }} ({{ p.year }}).</span>
    {% if p.arxiv and p.arxiv != "" %}<a href="https://arxiv.org/abs/{{ p.arxiv }}">arXiv:{{ p.arxiv }}</a>{% endif %}
  </li>
  {% endfor %}
</ul>
  {% endif %}
{% endfor %}
