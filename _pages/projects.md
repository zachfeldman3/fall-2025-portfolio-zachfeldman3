---
layout: project
title: Projects
permalink: /projects/
---

<h2>Class Projects</h2>

<div class="project-gallery">
  {% assign class_projects = site.projects | where: "category", "class" %}
  {% for p in class_projects %}
    <a class="gallery-item" href="{{ p.url | relative_url }}">
      <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}">
      <p>{{ p.title }}</p>
    </a>
  {% endfor %}
</div>

## Class Projects

- [Torque Wrench Design Optimization]({{ site.baseurl }}/projects/torquewrench/)

- [Fluid Mechanical Dissection]({{ site.baseurl }}/projects/FMD/)

- [RC Car Dissection]({{ site.baseurl }}/projects/RC/)

## Personal Projects

*In Development*

## Professional Projects

*In Development*

    <div class="gallery-container">
      <div class="project-gallery">
        {% for project in site.projects %}
          <div class="gallery-item">
            <a href="{{ project.url | relative_url }}">
              <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" />
              <p>{{ project.title }}</p>
            </a>
          </div>
        {% endfor %}
      </div>
    </div>
