---
layout: page
title: Projects
---
<section>
 <h2>Ongoing</h2>
  <div class="project-container">
    {% for project in site.data.settings.main-projects %}
      <a href="{{ site.github.url }}/{{ project.url }}">
            <h3>{{ project.name }}</h3>
            <p>{{ project.blurb }}</p>
      </a>
    {% endfor %}
  </div>
</section>
<section>
 <h2>Ideas for the future</h2>
  <div class="project-container">
    {% for project in site.data.settings.future-projects %}
      <a href="{{ site.github.url }}/{{ project.url }}">
            <h3>{{ project.name }}</h3>
            <p>{{ project.blurb }}</p>
      </a>
    {% endfor %}
  </div>
</section>
<!--
<section>
  <h1>Side Projects</h1>
  <div class="project-container">
    {% for project in site.data.settings.side-projects %}
      <a href="{{ site.github.url }}/{{ project.file }}">
            <h2>{{ project.name }}</h2>
            <p>{{ project.blurb }}</p>
      </a>
    {% endfor %}
  </div>
</section>
-->
