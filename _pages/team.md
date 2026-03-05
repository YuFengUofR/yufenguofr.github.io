---
layout: page
title: Team
permalink: /team/
nav: true
nav_order: 3
description: Members of the research group
---

## PhD Students

<ul class="team-list">
{% for m in site.data.team.phd %}
  <li class="team-item">
    <div class="team-line">
      {% if m.website %}
        <a href="{{ m.website }}" target="_blank" rel="noopener">{{ m.name }}</a>
      {% else %}
        {{ m.name }}
      {% endif %}
      {% if m.topic %} — <span class="team-topic">{{ m.topic }}</span>{% endif %}
      {% if m.start %} <span class="team-meta">({{ m.start }}–)</span>{% endif %}
    </div>

    {% if m.pubs %}
      <div class="team-pubs">Publications: {{ m.pubs }}</div>
    {% endif %}
  </li>
{% endfor %}
</ul>


## Master Students

<ul class="team-list">
{% for m in site.data.team.master %}
  <li class="team-item">
    <div class="team-line">
      {% if m.website %}
        <a href="{{ m.website }}" target="_blank" rel="noopener">{{ m.name }}</a>
      {% else %}
        {{ m.name }}
      {% endif %}
      {% if m.topic %} — <span class="team-topic">{{ m.topic }}</span>{% endif %}
      {% if m.start %} <span class="team-meta">({{ m.start }}–)</span>{% endif %}
    </div>

    {% if m.pubs %}
      <div class="team-pubs">Publications: {{ m.pubs }}</div>
    {% endif %}
  </li>
{% endfor %}
</ul>


## Undergraduate Students

<ul class="team-list">
{% for m in site.data.team.undergrad %}
  <li class="team-item">
    <div class="team-line">
      {% if m.website %}
        <a href="{{ m.website }}" target="_blank" rel="noopener">{{ m.name }}</a>
      {% else %}
        {{ m.name }}
      {% endif %}
      {% if m.topic %} — <span class="team-topic">{{ m.topic }}</span>{% endif %}
      {% if m.start %} <span class="team-meta">({{ m.start }}–)</span>{% endif %}
    </div>

    {% if m.pubs %}
      <div class="team-pubs">Publications: {{ m.pubs }}</div>
    {% endif %}
  </li>
{% endfor %}
</ul>


## Alumni

<ul class="team-list">
{% assign alumni_sorted = site.data.team.alumni | sort: "year" | reverse %}
{% for m in alumni_sorted %}
  <li class="team-item">
    <div class="team-line">
      {% if m.website %}
        <a href="{{ m.website }}" target="_blank" rel="noopener">{{ m.name }}</a>
      {% else %}
        {{ m.name }}
      {% endif %}
      {% if m.degree %} — <span class="team-topic">{{ m.degree }}</span>{% endif %}
      {% if m.year %} <span class="team-meta">{{ m.year }}</span>{% endif %}
      {% if m.now %} <span class="team-meta">, now at {{ m.now }}</span>{% endif %}
    </div>

    {% if m.pubs %}
      <div class="team-pubs">Publications: {{ m.pubs }}</div>
    {% endif %}
  </li>
{% endfor %}
</ul>