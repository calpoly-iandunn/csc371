---
layout: page
title: "Lectures"
auto-title: true
---

<ul>
{% for lecture in site.data.lectures %}
{% if lecture.outbound %}
<li><a href="{{ lecture.outbound }}">{{lecture.number}} - {{lecture.title}}</a></li>
{% elsif lecture.link %}
<li><a href="{{ lecture.link | prepend: site.baseurl }}">{{lecture.number}} - {{lecture.title}}</a></li>
{% else %}
<li>{{lecture.number}} - {{lecture.title}}</li>
{% endif %}
{% endfor %}
</ul>
