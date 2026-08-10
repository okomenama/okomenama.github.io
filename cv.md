---
layout: default
title: CV
permalink: /cv/
---

# CV

{% if site.cv_pdf_available %}
<p><a class="btn" href="{{ site.cv_pdf | relative_url }}" target="_blank" rel="noopener">Download full CV (PDF)</a></p>
{% endif %}

## Education

<ul class="entry-list">
{% for e in site.data.cv.education %}
  <li>
    <span class="entry-main">
      <strong>{{ e.degree }}</strong> — {{ e.institution }}<br>
      {{ e.field }}{% if e.advisor %}, Advisor: {{ e.advisor }}{% endif %}
      {% if e.thesis %}<br>Thesis: “{{ e.thesis }}”{% endif %}
      {% if e.notes %}<br>{{ e.notes }}{% endif %}
    </span>
    <span class="entry-date">{{ e.date }}</span>
  </li>
{% endfor %}
</ul>

## Awards & Grants

<ul class="entry-list">
{% for a in site.data.cv.awards %}
  <li><span class="entry-main">{{ a.name }}</span><span class="entry-date">{{ a.date }}</span></li>
{% endfor %}
</ul>

## Other Competitive Research Funds

<ul class="entry-list">
{% for f in site.data.cv.funding %}
  <li><span class="entry-main">{{ f.name }}</span><span class="entry-date">{{ f.date }}</span></li>
{% endfor %}
</ul>

## Research Internships

<ul class="entry-list">
{% for i in site.data.cv.internships %}
  <li>
    <span class="entry-main"><strong>{{ i.name }}</strong>{% if i.description and i.description != "" %}<br>{{ i.description }}{% endif %}</span>
    <span class="entry-date">{{ i.date }}</span>
  </li>
{% endfor %}
</ul>

## Activities

<ul class="entry-list">
{% for a in site.data.cv.activities %}
  <li>
    <span class="entry-main"><strong>{{ a.name }}</strong>{% if a.description and a.description != "" %}<br>{{ a.description }}{% endif %}</span>
    <span class="entry-date">{{ a.date }}</span>
  </li>
{% endfor %}
</ul>

## Other Skills

<p>
{{ site.data.cv.skills.languages | join: ", " }}<br>
Programming &amp; Applications: {{ site.data.cv.skills.programming | join: ", " }}<br>
{{ site.data.cv.skills.certificates | join: ", " }}
</p>

<p>See the <a href="{{ '/publications/' | relative_url }}">Publications</a> page for the full list of journal articles, conference presentations, and workshops.</p>
