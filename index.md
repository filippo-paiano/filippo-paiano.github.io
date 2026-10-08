---
layout: default
---
<p>
  {{ site.author.position }}<br>
  {{ site.author.affiliation }}
</p>

I work on calculus of variations and PDEs, more specifically on geometric variational problems and on elliptic and parabolic free boundary problems. My advisor is Bozhidar Velichkov.

<p class="tenue">
  {% if site.author.email != "" %}{{ site.author.email }} · {% endif %}
  {% if site.author.orcid != "" %}<a href="https://orcid.org/{{ site.author.orcid }}">ORCID</a> · {% endif %}
  {% if site.author.arxiv != "" %}<a href="{{ site.author.arxiv }}">arXiv</a> · {% endif %}
  {% if site.author.scholar != "" %}<a href="{{ site.author.scholar }}">Scholar</a> · {% endif %}
  <a href="https://github.com/{{ site.author.github }}">GitHub</a>
</p>
