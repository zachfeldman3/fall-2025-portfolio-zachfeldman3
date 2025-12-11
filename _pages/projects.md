---
layout: default
title: <Your Name> - Portfolio
permalink: /projects/
---

#### Projects

- **Automatic Basketball Return System (MAE 2250)**  
  *Engineered an automated ball-return mini-hoop system using motors, 3D-printed flywheels, laser-cut acrylic, and Arduino.*  
  - Designed and manufactured integrated components  
  - Collaborated with a 5-member engineering team  
  - Demonstrated functionality during a final presentation

- **Falcon 9 Rocket (3D Modeling & Printing Personal Project)**  
  *Designed and 3D-printed a 2+ ft tall 1/128 scale Falcon 9 rocket using Fusion 360 and an IDEX printer.*  
  - Performed extensive tolerance and dual-extrusion testing  
  - Achieved precise multi-component fitment

- **Electronic Medical Device – Motorized Endotracheal Tube**  
  *Built a prototype using Arduino, servos, and coils to enable remote adjustment of endotracheal tube placement.*  
  - Received iterative feedback from EMTs and doctors  
  - Improved usability and mechanical design through prototyping

---

## My Projects

- [Torque Wrench Design Optimization]({{ site.baseurl }}/projects/torquewrench/)

{{ site.baseurl }}/projects/torquewrench/

{% comment %}
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
{% endcomment %}
