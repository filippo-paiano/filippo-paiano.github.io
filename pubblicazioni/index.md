---
layout: default
title: Pubblicazioni
---
{% assign gruppi = "articolo:Articoli,preprint:Preprint,tesi:Tesi" | split: "," %}
{% for g in gruppi %}
  {% assign coppia = g | split: ":" %}
  {% assign voci = site.data.pubblicazioni | where: "tipo", coppia[0] | sort: "anno" | reverse %}
  {% if voci.size > 0 %}
<h2>{{ coppia[1] }}</h2>
<ul class="voci">
  {% for p in voci %}
  <li>
    {% if p.link and p.link != "" %}<a href="{{ p.link }}">{{ p.titolo }}</a>{% else %}{{ p.titolo }}{% endif %}<br>
    <span class="tenue">{{ p.autori }}. {{ p.sede }}.</span>
    {% if p.arxiv and p.arxiv != "" %}<a href="https://arxiv.org/abs/{{ p.arxiv }}">arXiv:{{ p.arxiv }}</a>{% endif %}
  </li>
  {% endfor %}
</ul>
  {% endif %}
{% endfor %}
