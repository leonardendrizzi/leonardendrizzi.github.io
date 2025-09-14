---
layout: default
title: Teaching
permalink: /teaching/
---

# Teaching

{% for course in site.data.teaching.courses %}
### {{ course.title }}
{{ course.blurb }}

{% for week in course.weeks %}
#### {{ week.title }}
<ul>
  {% for f in week.files %}
  <li><a href="{{ f.path }}">{{ f.label }}</a></li>
  {% endfor %}
</ul>
{% endfor %}

---
{% endfor %}

{% if site.data.teaching.previous_courses and site.data.teaching.previous_courses.size > 0 %}
### Previous Courses
<ul>
  {% for c in site.data.teaching.previous_courses %}
    <li>
      {% if c.url %}
        <a href="{{ c.url }}">{{ c.title }}</a>
      {% else %}
        {{ c.title }}
      {% endif %}
      {% if c.notes %} — {{ c.notes }}{% endif %}
    </li>
  {% endfor %}
</ul>
{% endif %}
