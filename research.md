---
layout: default
title: Research
permalink: /research/
---

# Research

---

### Working Papers
_(hopefully) coming soon_

---

### Work in Progress

{% assign wips = site.data.research.wip | default: empty %}
{% if wips and wips.size > 0 %}
<ul>
  {% for p in wips %}
  <li>
    <strong>{{ p.title }}</strong><br>
    {% if p.coauthors and p.coauthors.size > 0 %}
      <em>with 
      {% for a in p.coauthors %}
        {% if a.url %}
          <a href="{{ a.url }}">{{ a.name }}</a>
        {% else %}
          {{ a.name }}
        {% endif %}
        {% unless forloop.last %}, {% endunless %}
      {% endfor %}
      </em>
    {% endif %}
    {% if p.notes %}<br><em>{{ p.notes }}</em>{% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p>No public descriptions yet.</p>
{% endif %}

---