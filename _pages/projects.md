---
layout: default
title: Projects
permalink: /projects/
---

## Class Projects

<div class="gallery-container w-100">
  <div class="project-gallery d-flex flex-wrap justify-content-start align-items-start gap-4 w-100">
    {% assign class_projects = site.projects | where: "category", "class" %}
    {% for p in class_projects %}
      <a class="gallery-item text-decoration-none" href="{{ p.url | relative_url }}">
        <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}">
        <p class="mb-0 text-break" style="white-space: normal; overflow: visible;">
          {{ p.title }}
        </p>
      </a>
    {% endfor %}
  </div>
</div>



## Personal Projects

*In Development*

## Professional Projects

*In Development*

