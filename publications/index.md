---
title: Publications
layout: page
---

{% assign pubs_by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}

{% for year_group in pubs_by_year %}
## {{ year_group.name }}

{% for pub in year_group.items %}
<div class="publication-item">
  <div class="pub-title">{{ pub.title }}</div>
  <div class="pub-authors">{{ pub.authors }}</div>
  <div class="pub-venue">
    <em>{{ pub.venue }}</em>{% if pub.volume %}, {{ pub.volume }}{% endif %}{% if pub.pages %}: {{ pub.pages }}{% endif %}.
  </div>
  <div class="pub-links">
    {% if pub.doi %}
    <a href="https://doi.org/{{ pub.doi }}" target="_blank" rel="noopener">DOI</a>
    {% endif %}
    {% if pub.pdf %}
    <a href="{{ pub.pdf }}" target="_blank" rel="noopener">PDF</a>
    {% endif %}
  </div>
</div>
{% endfor %}

{% endfor %}
