---
layout: page
title: Projects
description: "Things Coffee Method has built: open source tools, experiments, and side projects."
---

Stuff I've built. Add a new one by editing `_data/projects.yml`. No HTML required.

<ul class="cards">
{%- for p in site.data.projects %}
  <li class="card">
    <h2>{% if p.url %}<a href="{{ p.url }}">{{ p.name }}</a>{% else %}{{ p.name }}{% endif %}</h2>
    <p>{{ p.description }}</p>
    {%- for t in p.tags %}<span class="tag">{{ t }}</span>{% endfor -%}
  </li>
{%- endfor %}
</ul>
