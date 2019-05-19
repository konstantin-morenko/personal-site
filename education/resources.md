---
title: Образовательные материалы
layout: page
permalink: /education/resources.html
---

{% for source in site.data.education.sources %}
  <div class="w3-panel w3-card"><h3><a href="{{ source.link }}">{{ source.title }}</a></h3>
  {% if source.desc %}
  <p>{{ source.desc }}</p>
  </div>
  {% endif %}
{% endfor %}
