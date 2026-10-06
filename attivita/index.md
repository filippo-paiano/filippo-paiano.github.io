---
layout: default
title: Attività
---
{% for s in site.data.attivita %}
<h2>{{ s.sezione }}</h2>
<ul class="voci">
  {% for v in s.voci %}
  <li><span class="anno">{{ v.anno }}</span>{{ v.descrizione | markdownify | remove: "<p>" | remove: "</p>" }}</li>
  {% endfor %}
</ul>
{% endfor %}
