---
layout: default
title: Projects
permalink: /projects/
---

## Class Projects

<div class="gallery-container">
  <div class="project-gallery d-flex flex-wrap gap-4 justify-content-start">
    {% assign class_projects = site.projects | where: "category", "class" %}
    {% for p in class_projects %}
      <div class="gallery-item">
        <a href="{{ p.url | relative_url }}">
          <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}" />
          <p class="text-wrap text-break mb-0">{{ p.title }}</p>
        </a>
      </div>
    {% endfor %}
  </div>
</div>




## Personal Projects

*In Development*

## Professional Projects

*In Development*

