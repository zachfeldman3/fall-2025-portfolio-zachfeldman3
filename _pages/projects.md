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
      <a class="gallery-item text-decoration-none" href="{{ p.url | relative_url }}"
         style="display:block; width: 460px;">
        
        <!-- image box -->
        <div style="height: 240px; display:flex; align-items:center; justify-content:center;">
          <img
          <img
            src="{{ p.image | relative_url }}"
            alt="{{ p.imagealt | default: p.title }}"
            style="height: 240px; width: auto; max-width: 100%; display: block; margin: 0 auto;"
          >
        </div>

        <p class="mb-0 text-break" style="white-space: normal; overflow: visible; margin-top: 10px;">
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

