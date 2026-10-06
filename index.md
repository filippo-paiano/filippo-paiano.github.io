---
layout: default
---
<p>
  {{ site.author.position }}<br>
  {{ site.author.affiliation }}
</p>

[DA COMPILARE] Breve presentazione: interessi di ricerca, gruppo, supervisore.

<p class="tenue">
  {% if site.author.email != "" %}{{ site.author.email }} · {% endif %}
  {% if site.author.orcid != "" %}<a href="https://orcid.org/{{ site.author.orcid }}">ORCID</a> · {% endif %}
  {% if site.author.arxiv != "" %}<a href="{{ site.author.arxiv }}">arXiv</a> · {% endif %}
  {% if site.author.scholar != "" %}<a href="{{ site.author.scholar }}">Scholar</a> · {% endif %}
  <a href="https://github.com/{{ site.author.github }}">GitHub</a>
</p>
