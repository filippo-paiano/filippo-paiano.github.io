---
layout: default
---
<p>
  {{ site.author.position }}<br>
  {{ site.author.affiliation }}
</p>

I work on calculus of variations and PDEs, more specifically on geometric variational problems and on elliptic and parabolic free boundary problems. My advisor is Bozhidar Velichkov.

<p class="tenue contatti">
  {% if site.author.email != "" %}<span>{{ site.author.email }}</span>{% endif %}
  {% if site.author.orcid != "" %}<span><a href="https://orcid.org/{{ site.author.orcid }}">ORCID</a></span>{% endif %}
  {% if site.author.arxiv != "" %}<span><a href="{{ site.author.arxiv | escape }}">arXiv</a></span>{% endif %}
  {% if site.author.cvgmt != "" %}<span><a href="{{ site.author.cvgmt }}">cvgmt</a></span>{% endif %}
  {% if site.author.scholar != "" %}<span><a href="{{ site.author.scholar }}">Scholar</a></span>{% endif %}
</p>
