---
layout: default
title: ""
permalink: /
---

<div class="zf-home">

  <div class="zf-hero zf-hero-split">

    <div class="zf-hero-text">
      <h1 class="zf-title">Zach Feldman</h1>

      <p class="zf-subtitle">
        Mechanical Engineering Junior at Cornell University
      </p>

      <div class="zf-actions">
        <a class="zf-btn primary" href="{{ '/projects/' | relative_url }}">View Projects →</a>
        <a class="zf-btn" href="{{ '/cv/' | relative_url }}">Resume</a>
        <a class="zf-btn" href="#contact">Contact</a>
      </div>

      <div class="zf-hero-body">
        <p style="margin: 0 0 .9rem 0;">
          My name is Zach Feldman, and I am a Mechanical Engineering student at Cornell University with interests in product design,
          manufacturing, and hands-on engineering projects.
        </p>

        <p style="margin: 0;">
          I enjoy creating practical, meaningful solutions—from carbon-fiber components for Cornell Electric Vehicles to mechanical
          systems built in class and personal projects. I’m passionate about learning new engineering tools, building things that
          work, and continuously improving my technical skills.
        </p>
      </div>
    </div>

    <div class="zf-hero-image">
      <img
        src="{{ '/assets/images/zachpfp.jpeg' | relative_url }}"
        alt="Zach Feldman"
        style="
          width: 320px;
          height: 400px;
          object-fit: cover;
          border-radius: 22px;
          border: 1px solid rgba(255,255,255,.16);
          box-shadow: 0 18px 55px rgba(0,0,0,.55);
          display:block;
        "
      />
    </div>

  </div>


<style>
/* ====== ONLY MOBILE FIXES ====== */

@media (max-width: 900px){

  html, body{
    overflow-x: hidden !important;
  }

  .zf-home{
    width: 100% !important;
    margin-left: auto !important;
    margin-right: auto !important;
    padding-left: 16px !important;
    padding-right: 16px !important;
    box-sizing: border-box !important;
  }

  .zf-home .zf-hero.zf-hero-split{
    grid-template-columns: 1fr !important;
    gap: 1.25rem !important;
    justify-items: center !important;
  }

  .zf-home .zf-hero-text{
    text-align: center !important;
    margin-left: 0 !important;
  }

  .zf-home .zf-hero-image{
    justify-content: center !important;
    padding-right: 0 !important;
  }

  .zf-home .zf-hero-image img{
    width: min(320px, 100%) !important;
    height: auto !important;
    aspect-ratio: 4 / 5;
  }

  .zf-highlight-grid{
    grid-template-columns: 1fr !important;
  }
}
</style>



  <div class="zf-grid">

    <div class="zf-tile">
      <h3>Interests</h3>
      <div class="zf-tags">
        <span class="zf-tag">Manufacturing</span>
        <span class="zf-tag">Composites</span>
        <span class="zf-tag">Additive</span>
        <span class="zf-tag">Design</span>
      </div>
    </div>

    <div class="zf-tile">
      <h3>Skills</h3>
      <div class="zf-tags">
        <span class="zf-tag">CAD</span>
        <span class="zf-tag">3D Printing</span>
        <span class="zf-tag">Machining</span>
        <span class="zf-tag">Manufacturing</span>
      </div>
    </div>

    <div class="zf-tile">
      <h3>What I’m Doing Now</h3>
      <div class="zf-tags">
        <span class="zf-tag">Chassis Lead</span>
        <span class="zf-tag">Composites Manufacturing</span>
        <span class="zf-tag">Ansys ACP/FEA</span>
        <span class="zf-tag">Ansys LPBF Research</span>
      </div>
    </div>

    <div class="zf-tile">
      <h3>What I’m Looking For</h3>
      <div class="zf-tags">
        <span class="zf-tag">Mechanical Engineering Job Opportunities</span>
      </div>
    </div>

  </div>


  <hr style="margin: 2.2rem 0;"/>


  <h3 style="margin-bottom: .9rem;">Highlighted Work</h3>

  <div class="zf-highlight-grid" style="
    display:grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.2rem;
  ">

    <img src="{{ '/assets/images/2024chassis.png' | relative_url }}" style="width:100%; height:200px; object-fit:cover; border-radius:22px; display:block; box-shadow: 0 0 38px rgba(86,240,255,.25), 0 0 18px rgba(139,92,246,.18);" />

    <img src="{{ '/assets/images/internalheadlight.png' | relative_url }}" style="width:100%; height:200px; object-fit:cover; border-radius:22px; display:block; box-shadow: 0 0 38px rgba(86,240,255,.25), 0 0 18px rgba(139,92,246,.18);" />

    <img src="{{ '/assets/images/M-totaldeformation.png' | relative_url }}" style="width:100%; height:200px; object-fit:cover; border-radius:22px; display:block; box-shadow: 0 0 38px rgba(86,240,255,.25), 0 0 18px rgba(139,92,246,.18);" />

  </div>


  <div style="display:flex; justify-content:center; margin-top: 1.6rem;">
    <a href="{{ '/projects/' | relative_url }}"
       class="zf-btn primary"
       style="padding:.9rem 1.6rem; border-radius:999px;">
      View All Projects →
    </a>
  </div>


  <hr style="margin: 2.2rem 0;"/>


  <h3 id="contact" style="margin-bottom:.7rem;">Contact</h3>

  <div class="zf-tile" style="padding: 1.2rem;">

    <p style="margin: 0 0 1rem 0;">
      Email me at
      <a href="mailto:zlf3@cornell.edu">zlf3@cornell.edu</a><br/>
      Call me at <a href="tel:19143567068">(914) 356-7068</a>
    </p>

    <a href="https://www.linkedin.com/in/zlf3/" target="_blank" rel="noopener">
      LinkedIn
    </a>

  </div>

</div>
