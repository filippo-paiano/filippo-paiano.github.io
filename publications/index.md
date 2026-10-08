---
layout: default
title: Publications
---
<p class="tenue">All my publications are available on the <a href="{{ site.author.arxiv | escape }}">arXiv</a> and <a href="{{ site.author.cvgmt }}">cvgmt</a> repositories.</p>

{% assign groups = "article:Journal articles,preprint:Preprints" | split: "," %}
{% for g in groups %}
  {% assign pair = g | split: ":" %}
  {% assign items = site.data.publications | where: "type", pair[0] | sort: "year" | reverse %}
  {% if items.size > 0 %}
<h2>{{ pair[1] }}</h2>
<ul class="voci">
  {% for p in items %}
  <li>
    {{ p.title }}<br>
    <span class="tenue">{{ p.authors }}. {{ p.venue | markdownify | remove: "<p>" | remove: "</p>" | strip }} ({{ p.year }}).</span>
    {% if p.doi and p.doi != "" %}<a href="https://doi.org/{{ p.doi }}">doi:{{ p.doi }}</a>{% endif %}
    {% if p.arxiv and p.arxiv != "" %}<a href="https://arxiv.org/abs/{{ p.arxiv }}">arXiv:{{ p.arxiv }}</a>{% endif %}
  </li>
  {% endfor %}
</ul>
  {% endif %}
{% endfor %}
