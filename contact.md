---
layout: page
title: Contact
---
<section>
  <h1>Contact</h1>
  <p>Feel free to contact me <a href="mailto:wiktor.rorot@student.uw.edu.pl" target="_blank">through my email</a> or <a href="https://twitter.com/intent/tweet?text=%40WiktorRorot" target="_blank">tweet at me</a>.</p>
  <!-- <img src="/assets/img/profile.jpg" alt="This is me"> -->
  <p>You can also follow me.</p>
  <div class="social-media">
      <nav>
        {% for item in site.data.settings.social %}
          <a href="{{ item.link }}" target="_blank"><i class="fa fa-{{ item.icon }}" aria-hidden="true"></i></a>
        {% endfor %}
      </nav>
  </div>
</section>
