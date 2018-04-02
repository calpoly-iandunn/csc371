---
layout: page
active: assignments
title: "Assignments"
auto-title: true
---

<div class="alert alert-dismissible alert-warning">
  <button type="button" class="close" data-dismiss="alert">&times;</button>
  <strong>Warning:</strong> Any assignment with a due-date before the start of the quarter is not ready yet.
  Some new assignments will also be added.
</div>


## Written Assignments

{% for pair in site.data.assignments %}
  {% assign name = pair[0] %}
  {% assign assignment = pair[1] %}

  {% if assignment.type == 'assignment' %}
- [{{ assignment.title }} - {{ assignment.subtitle }}]({{ name }}) due {{ assignment.due }}
  {% endif %}
{% endfor %}

