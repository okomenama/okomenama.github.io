---
layout: default
title: Contact
permalink: /contact/
---

# Contact

<ul class="entry-list">
  <li><span class="entry-main"><strong>Email</strong></span><span class="entry-date"><a href="mailto:{{ site.email }}">{{ site.email }}</a></span></li>
  {% if site.orcid and site.orcid != "" %}
  <li><span class="entry-main"><strong>ORCID</strong></span><span class="entry-date"><a href="{{ site.orcid }}" target="_blank" rel="noopener">{{ site.orcid }}</a></span></li>
  {% endif %}
  {% if site.researchmap and site.researchmap != "" %}
  <li><span class="entry-main"><strong>ResearchMap</strong></span><span class="entry-date"><a href="{{ site.researchmap }}" target="_blank" rel="noopener">{{ site.researchmap }}</a></span></li>
  {% endif %}
  {% if site.google_scholar and site.google_scholar != "" %}
  <li><span class="entry-main"><strong>Google Scholar</strong></span><span class="entry-date"><a href="{{ site.google_scholar }}" target="_blank" rel="noopener">{{ site.google_scholar }}</a></span></li>
  {% endif %}
  <li><span class="entry-main"><strong>Affiliation</strong></span><span class="entry-date">{{ site.affiliation }}</span></li>
  <li><span class="entry-main"><strong>Advisor</strong></span><span class="entry-date">{{ site.advisor }}</span></li>
</ul>

