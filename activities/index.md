---
layout: default
title: Activities
---
{% for s in site.data.activities %}
<h2>{{ s.section }}</h2>
<ul class="voci">
  {% for v in s.items %}
  <li><span class="anno">{{ v.when }}</span>{{ v.text | markdownify | remove: "<p>" | remove: "</p>" }}</li>
  {% endfor %}
</ul>
{% endfor %}
