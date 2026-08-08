---
layout: default
title: Publications
permalink: /publications/
---

# Publications

<p class="note-box">
This page is generated from <code>_data/cv.yml</code> — add a new item under
<code>publications</code> or <code>presentations</code> in that file and it
appears here automatically, in the order listed (newest first).
</p>

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
    {{ p.authors }}. “{{ p.title }}.” <span class="pub-venue">{{ p.venue }}</span>{% if p.location %}, {{ p.location }}{% endif %}, {{ p.date }}{% if p.type and p.type != "" %} ({{ p.type }}){% endif %}.
  </li>
  {% endif %}
{% endfor %}
</ul>

## Workshops

<ul class="pub-list">
{% for p in site.data.cv.presentations %}
  {% if p.category == "Workshop" %}
  <li>
    {{ p.authors }}. “{{ p.title }}.” <span class="pub-venue">{{ p.venue }}</span>{% if p.location %}, {{ p.location }}{% endif %}, {{ p.date }}{% if p.type and p.type != "" %} ({{ p.type }}){% endif %}.
  </li>
  {% endif %}
{% endfor %}
</ul>
