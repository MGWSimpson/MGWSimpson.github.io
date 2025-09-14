---
layout: default
title: research
permalink: /research/
---


{% assign items = site.research | sort: "order" %}
<div class="research-list">
  {% for p in items %}
    <article class="research-card">
      <h2><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h2>
      {% if p.summary %}<p>{{ p.summary }}</p>{% endif %}
      {% if p.tags %}<p><em>{{ p.tags | join: ", " }}</em></p>{% endif %}
      {% if p.links %}
        <p>
          {% if p.links.paper %}<a href="{{ p.links.paper }}">Paper</a>{% endif %}
          {% if p.links.code %} • <a href="{{ p.links.code }}">Code</a>{% endif %}
          {% if p.links.demo %} • <a href="{{ p.links.demo }}">Demo</a>{% endif %}
        </p>
      {% endif %}
    </article>
  {% endfor %}
</div>


coming soon..