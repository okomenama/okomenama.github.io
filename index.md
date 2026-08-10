---
layout: default
title: Home
---

<div class="profile">
  <div class="profile-photo placeholder" aria-hidden="true">AK</div>
  <div>
    <h1 class="profile-name">Amane Kubo</h1>
    <p class="profile-tagline">Ph.D. Student, Civil Engineering &middot; {{ site.affiliation }}<br>Advisor: {{ site.advisor }}</p>
    <div class="profile-links">
      <a href="mailto:{{ site.email }}">Email</a>
      <a href="{{ '/cv/' | relative_url }}">CV</a>
      <a href="{{ '/research/' | relative_url }}">Research</a>
      <a href="{{ '/publications/' | relative_url }}">Publications</a>
    </div>
  </div>
</div>

<p>
  I am a Ph.D. student in Civil Engineering at the University of Tokyo, advised by
  Yohei Sawada. 
</p>

## Research Interests

My research aims to establish the conditions under which mathematical models
and observations can be optimally combined for better climate prediction —
particularly around climate tipping points — and to inform policy-making for
climate mitigation that directly reflects state-of-the-art scientific
progress.

<ul class="interests-list">
  <li>Climate Tipping</li>
  <li>Climate Prediction</li>
  <li>Earth System Model</li>
  <li>Mathematical Statistics</li>
  <li>Dynamical Systems</li>
  <li>Quantum Computing</li>
</ul>

{% assign recent_research = site.research | sort: 'date' | reverse %}
{% if recent_research.size > 0 %}
## Recent Research

<div class="card-list">
  {% for item in recent_research limit: 3 %}
  <div class="card">
    <h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
    <p class="card-meta">
      {{ item.venue }}{% if item.date %} &middot; {{ item.date | date: "%b %Y" }}{% endif %}
    </p>
    <p class="card-summary">{{ item.summary }}</p>
  </div>
  {% endfor %}
</div>

<p><a href="{{ '/research/' | relative_url }}">See all research &rarr;</a></p>
{% endif %}
