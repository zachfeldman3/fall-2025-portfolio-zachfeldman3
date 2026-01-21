—--
layout: default 
title: Projects 
permalink: /projects/ 
--- 

## Featured Engineering Projects 

<div class="gallery-container w-100"> 
  <div class="project-gallery d-flex flex-wrap justify-content-start align-items-start gap-4 w-100"> 
    {% assign featured_projects = site.projects | where: "category", "featured" %} 
    {% for p in featured_projects %} 
      <a class="gallery-item text-decoration-none" href="{{ p.url | relative_url }}" style="display:block; width: 460px;"> 
        
        <!-- image box --> 
        <div style="height: 240px; display:flex; align-items:center; justify-content:center;"> 
          <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}" style="max-height: 240px; max-width: 100%; height:auto; width:auto; object-fit: contain; display:block;" > 
        </div> 

        <!-- title --> 
        <p class="mb-0 text-break" style="margin-top: 6px; text-align:center;"> 
          {{ p.title }} 
        </p> 

      </a> 
    {% endfor %} 
  </div> 
</div> 

## Course Projects 

<div class="gallery-container w-100"> 
  <div class="project-gallery d-flex flex-wrap justify-content-start align-items-start gap-4 w-100"> 
    {% assign class_projects = site.projects | where: "category", "class" %} 
    {% for p in class_projects %} 
      <a class="gallery-item text-decoration-none" href="{{ p.url | relative_url }}" style="display:block; width: 460px;"> 
        
        <!-- image box --> 
        <div style="height: 240px; display:flex; align-items:center; justify-content:center;"> 
          <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}" style="max-height: 240px; max-width: 100%; height:auto; width:auto; object-fit: contain; display:block;" > 
        </div> 

        <!-- title --> 
        <p class="mb-0 text-break" style="margin-top: 6px; text-align:center;"> 
          {{ p.title }} 
        </p> 

      </a> 
    {% endfor %} 
  </div> 
</div> 
