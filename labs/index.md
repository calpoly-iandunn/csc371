---
layout: page
active: labs
title: "Labs"
auto-title: true
---


## Unity Labs

{% for pair in site.data.assignments %}
  {% assign name = pair[0] %}
  {% assign assignment = pair[1] %}

  {% if assignment.type == 'lab' and assignment.display != false %}
- [{{ assignment.title }} - {{ assignment.subtitle }}](../labs/{{ name }}) due {{ assignment.due }}
  {% endif %}
{% endfor %}

