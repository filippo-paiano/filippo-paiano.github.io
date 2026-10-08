---
layout: default
title: Activities
---
{% for s in site.data.activities %}
<h2>{{ s.section }}</h2>
<ul class="voci date-list">
  {% for v in s.items %}
  <li><span class="anno">{{ v.year }}</span>{{ v.title | markdownify | remove: "<p>" | remove: "</p>" | strip }}<span class="nota">{{ v.note | markdownify | remove: "<p>" | remove: "</p>" | strip }}</span></li>
  {% endfor %}
</ul>
{% endfor %}
