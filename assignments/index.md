---
layout: page
active: assignments
title: "Assignments"
auto-title: true
---


## Written Assignments

{% for pair in site.data.assignments %}
  {% assign name = pair[0] %}
  {% assign assignment = pair[1] %}

  {% if assignment.type == 'assignment' and assignment.display != false %}
- [{{ assignment.title }} - {{ assignment.subtitle }}]({{ name }}) due {{ assignment.due }}
  {% endif %}
{% endfor %}



## Unity Labs

{% for pair in site.data.assignments %}
  {% assign name = pair[0] %}
  {% assign assignment = pair[1] %}

  {% if assignment.type == 'lab' and assignment.display != false %}
- [{{ assignment.title }} - {{ assignment.subtitle }}](../labs/{{ name }}) due {{ assignment.due }}
  {% endif %}
{% endfor %}

