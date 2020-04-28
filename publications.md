---
layout: page
title: Publications
---

<div class="publist">
  <ul>
    {% for post in site.categories.publication %}
      {% if post.work-type == 'paper' %}
        <li>
          <a href="{% if post.ref-doi %}http://dx.doi.org/{{ post.ref-doi }}
            {% else %}{{ post.url | prepend: site.baseurl }}{% endif %}">
            <h2>{{ post.ref-authors }} ({{ post.ref-year }}).</h2></a>
          <p>
            {{ post.ref-title }}.
            <em>{{ post.ref-journal}}</em>
            {% if post.ref-vol %}, {{ post.ref-vol }}{% endif %}.
            {% if post.ref-doi %}
              <a href="http://dx.doi.org/{{ post.ref-doi }}">
                doi: {{ post.ref-doi }}
              </a>
            {% endif %}
          </p>
        </li>
      {% endif %}
    {% endfor %}
  <ul>
</div>
