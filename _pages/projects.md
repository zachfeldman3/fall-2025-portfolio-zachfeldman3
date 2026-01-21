---
layout: default
title: Projects
permalink: /projects/
---

<h1 class="zf-page-title">Projects</h1>

<h2 class="zf-section-title">Featured Engineering Projects</h2>

<div class="zf-projects-grid">
  {% assign featured_projects = site.projects | where: "category", "featured" %}
  {% for p in featured_projects %}
    <a class="zf-project-card" href="{{ p.url | relative_url }}">
      <div class="zf-project-media">
        <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}">
      </div>
      <div class="zf-project-body">
        <div class="zf-project-name">{{ p.title }}</div>
        {% if p.subtitle %}
        <div class="zf-project-sub">{{ p.subtitle }}</div>
        {% endif %}
      </div>
    </a>
  {% endfor %}
</div>

<h2 class="zf-section-title">Course Projects</h2>

<div class="zf-projects-grid">
  {% assign class_projects = site.projects | where: "category", "class" %}
  {% for p in class_projects %}
    <a class="zf-project-card" href="{{ p.url | relative_url }}">
      <div class="zf-project-media">
        <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}">
      </div>
      <div class="zf-project-body">
        <div class="zf-project-name">{{ p.title }}</div>
        {% if p.subtitle %}
        <div class="zf-project-sub">{{ p.subtitle }}</div>
        {% endif %}
      </div>
    </a>
  {% endfor %}
</div>

