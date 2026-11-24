---
layout: default
title: Publications
permalink: /publications/
---

# Publications

{% assign today = site.time | date: "%Y-%m-%d" %}

## Journal Articles

<ul class="pub-list">
{% for p in site.data.cv.publications %}
  <li>
    {{ p.authors }} ({{ p.year }}). {% if p.url and p.url != "" %}<a href="{{ p.url }}" target="_blank" rel="noopener">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}.
    {% if p.venue and p.venue != "" %}<span class="pub-venue">{{ p.venue }}</span>{% if p.detail and p.detail != "" %}, {{ p.detail }}{% endif %}.{% endif %}
  </li>
{% endfor %}
</ul>

## Peer-Reviewed Conference Presentations

<ul class="pub-list">
{% for p in site.data.cv.presentations %}
  {% if p.category == "Peer-reviewed Conference" %}
  <li>
    {{ p.authors }}. “{{ p.title }}.” <span class="pub-venue">{{ p.venue }}</span>{% if p.location %}, {{ p.location }}{% endif %}, {{ p.date }}{% if p.type and p.type != "" %} ({{ p.type }}){% endif %}.{% if p.date_iso and p.date_iso >= today %} <span class="pub-upcoming">Upcoming</span>{% endif %}
  </li>
  {% endif %}
{% endfor %}
</ul>

## Invited Seminars

<ul class="pub-list">
{% for p in site.data.cv.presentations %}
  {% if p.category == "Invited Seminar" %}
  <li>
    {{ p.authors }}. “{{ p.title }}.” <span class="pub-venue">{% if p.url and p.url != "" %}<a href="{{ p.url }}" target="_blank" rel="noopener">{{ p.venue }}</a>{% else %}{{ p.venue }}{% endif %}</span>{% if p.location %}, {{ p.location }}{% endif %}, {{ p.date }}.{% if p.date_iso and p.date_iso >= today %} <span class="pub-upcoming">Upcoming</span>{% endif %}
  </li>
  {% endif %}
{% endfor %}
</ul>

## Workshops

<ul class="pub-list">
{% for p in site.data.cv.presentations %}
  {% if p.category == "Workshop" %}
  <li>
    {{ p.authors }}. “{{ p.title }}.” <span class="pub-venue">{{ p.venue }}</span>{% if p.location %}, {{ p.location }}{% endif %}, {{ p.date }}{% if p.type and p.type != "" %} ({{ p.type }}){% endif %}.{% if p.date_iso and p.date_iso >= today %} <span class="pub-upcoming">Upcoming</span>{% endif %}
  </li>
  {% endif %}
{% endfor %}
</ul>
