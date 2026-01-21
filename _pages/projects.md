---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-page">

  <section class="page-hero">
    <div class="kicker">Portfolio</div>
    <h1>Projects</h1>
    <p>Featured work and course projects — clean, visual, and quick to scan.</p>
  </section>

  <section class="section">
    <div class="section-title">
      <h2>Featured Engineering Projects</h2>
      <p>High-impact work I’m most proud of.</p>
    </div>

    <div class="grid cols-3">
      {% assign featured_projects = site.projects | where: "category", "featured" %}
      {% for p in featured_projects %}
        <a class="card text-decoration-none" href="{{ p.url | relative_url }}">
          <div class="sheen"></div>

          <!-- image -->
          <div style="height: 240px; display:flex; align-items:center; justify-content:center;">
            <img
              src="{{ p.image | relative_url }}"
              alt="{{ p.imagealt | default: p.title }}"
              style="max-height: 240px; max-width: 100%; height:auto; width:auto; object-fit: contain; display:block; border-radius: 16px; border: 1px solid rgba(255,255,255,0.10);"
            >
          </div>

          <!-- title “box” (pill) -->
          <div style="display:flex; justify-content:center; margin-top: 12px;">
            <span class="tag accent" style="font-size: 13px; padding: 8px 14px;">
              {{ p.title }}
            </span>
          </div>
        </a>
      {% endfor %}
    </div>
  </section>

  <section class="section">
    <div class="section-title">
      <h2>Course Projects</h2>
      <p>Selected academic work (design + analysis).</p>
    </div>

    <div class="grid cols-3">
      {% assign class_projects = site.projects | where: "category", "class" %}
      {% for p in class_projects %}
        <a class="card text-decoration-none" href="{{ p.url | relative_url }}">
          <div class="sheen"></div>

          <!-- image -->
          <div style="height: 240px; display:flex; align-items:center; justify-content:center;">
            <img
              src="{{ p.image | relative_url }}"
              alt="{{ p.imagealt | default: p.title }}"
              style="max-height: 240px; max-width: 100%; height:auto; width:auto; object-fit: contain; display:block; border-radius: 16px; border: 1px solid rgba(255,255,255,0.10);"
            >
          </div>

          <!-- title “box” (pill) -->
          <div style="display:flex; justify-content:center; margin-top: 12px;">
            <span class="tag" style="font-size: 13px; padding: 8px 14px;">
              {{ p.title }}
            </span>
          </div>
        </a>
      {% endfor %}
    </div>
  </section>

</div>


