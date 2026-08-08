---
layout: default
title: Research
permalink: /research/
---

# Research

Representative research topics, with slide decks and short summaries. New
entries are added incrementally as new work is presented — see
[`README.md`](https://github.com/okomenama/okomenama.github.io#adding-a-research-entry)
for how this page is updated.

{% assign items = site.research | sort: 'date' | reverse %}
<div class="card-list">
  {% for item in items %}
  <div class="card">
    <h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
    <p class="card-meta">
      {{ item.venue }}{% if item.location %}, {{ item.location }}{% endif %}
      {% if item.date %}&middot; {{ item.date | date: "%b %Y" }}{% endif %}
      {% if item.presentation_type %}&middot; {{ item.presentation_type }}{% endif %}
    </p>
    {% if item.tags %}
    <div>{% for tag in item.tags %}<span class="tag">{{ tag }}</span>{% endfor %}</div>
    {% endif %}
    <p class="card-summary">{{ item.summary }}</p>
    <p class="card-links">
      <a href="{{ item.url | relative_url }}">Details &rarr;</a>
      {% if item.pdf %}<a href="{{ item.pdf | relative_url }}" target="_blank" rel="noopener">Slides (PDF)</a>{% endif %}
      {% if item.paper_url %}<a href="{{ item.paper_url }}" target="_blank" rel="noopener">Paper</a>{% endif %}
    </p>
  </div>
  {% endfor %}
</div>
