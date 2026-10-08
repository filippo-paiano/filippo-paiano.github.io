---
layout: default
---
<div class="home">
  <div class="home-main">
    <p>
      {{ site.author.position }}<br>
      <a href="{{ site.author.affiliation_url }}">{{ site.author.affiliation }}</a>
    </p>
    <p>I work on calculus of variations and PDEs, more specifically on geometric variational problems and on elliptic and parabolic free boundary problems. My advisor is <a href="http://www.velichkov.it/">Prof. Bozhidar Velichkov</a>.</p>
    <p>See my <a href="{{ '/publications/' | relative_url }}">publications</a>, <a href="{{ '/activities/' | relative_url }}">activities</a> and <a href="{{ '/cv/' | relative_url }}">CV</a>.</p>
  </div>

  <aside class="contatti">
    {% if site.author.photo != "" %}<img class="foto" src="{{ site.author.photo | relative_url }}" alt="{{ site.author.name }}">{% endif %}
    <dl>
      {% if site.author.email != "" %}<dt>Email</dt><dd>{{ site.author.email }}</dd>{% endif %}
      {% if site.author.address != "" %}<dt>Address</dt><dd><a href="{{ site.author.affiliation_url }}">{{ site.author.affiliation }}</a><br>{% if site.author.office != "" %}{{ site.author.office }}<br>{% endif %}{{ site.author.address }}</dd>{% endif %}
      <dt>Links</dt>
      <dd>
        {% if site.author.arxiv != "" %}<a href="{{ site.author.arxiv | escape }}">arXiv</a><br>{% endif %}
        {% if site.author.cvgmt != "" %}<a href="{{ site.author.cvgmt }}">cvgmt</a><br>{% endif %}
        {% if site.author.orcid != "" %}<a href="https://orcid.org/{{ site.author.orcid }}">ORCID</a><br>{% endif %}
        {% if site.author.scholar != "" %}<a href="{{ site.author.scholar }}">Google Scholar</a><br>{% endif %}
      </dd>
    </dl>
  </aside>
</div>
