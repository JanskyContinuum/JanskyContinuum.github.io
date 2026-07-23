---
layout: default
title: Projekty
---

# My Projects

Below you'll find a selection of my engineering projects, including both personal work and collaborative efforts. They also happen to be the ones I'm not too embarrassed to put on the internet. Any resemblance to planned career development is almost certainly intentional.

<ul>
  {% for project in site.projects %}
    <li>
      <strong><a href="{{ project.url }}">{{ project.title }}</a></strong>
    </li>
  {% endfor %}
</ul>