---
layout: default
title: Projects
permalink: /projects/
---

## Class Projects

<div class="project-gallery">
  {% assign class_projects = site.projects | where: "category", "class" %}
  {% for p in class_projects %}
    <a class="gallery-item" href="{{ p.url | relative_url }}">
      <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}">
      <p>{{ p.title }}</p>
    </a>
  {% endfor %}
</div>

## Personal Projects

*In Development*

## Professional Projects

*In Development*

