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
        <a class="zf-btn" href="{{ '/cv/' | relative_url }}">CV</a>
        <a class="zf-btn" href="{{ '/about/' | relative_url }}">About</a>
      </div>

      <div style="margin-top:1.3rem; max-width: 60ch;">

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
          width: 300;
          height: 400;
          object-fit: cover;
          border-radius: 22px;
          border: 1px solid rgba(255,255,255,.16);
          box-shadow: 0 18px 55px rgba(0,0,0,.55);
        "
      />
    </div>

  </div>


  <!-- INDEX-ONLY OVERRIDE: kill hover enlarge + blue highlight -->
  <style>
    .zf-grid .zf-tile:hover{
      transform: none !important;
      border-color: rgba(255,255,255,.14) !important;
      box-shadow: var(--shadow2) !important;
    }
    .zf-grid .zf-tile{
      -webkit-tap-highlight-color: transparent;
      cursor: default;
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
        <span class="zf-tag">Cornell EV</span>
        <span class="zf-tag">Chassis Lead</span>
        <span class="zf-tag">Composites</span>
        <span class="zf-tag">Manufacturing</span>
      </div>
    </div>

    <div class="zf-tile">
      <h3>What I’m Looking For</h3>
      <div class="zf-tags">
        <span class="zf-tag">Spring 2027 Co-op</span>
        <span class="zf-tag">Summer 2027 Full Time Engineering Position</span>
      </div>
    </div>

  </div>


  <hr style="margin: 2.2rem 0;"/>


  <h3 style="margin-bottom: .9rem;">Highlighted Work</h3>

  <div style="
    display:grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.2rem;
  ">

    <img
      src="{{ '/assets/images/2024chassis.png' | relative_url }}"
      alt=""
      style="
        width:100%;
        height:200px;
        object-fit:cover;
        border-radius:22px;
        border:none;
        display:block;
        box-shadow:
          0 0 38px rgba(86,240,255,.25),
          0 0 18px rgba(139,92,246,.18);
      "
    />

    <img
      src="{{ '/assets/images/sidepartmold.jpg' | relative_url }}"
      alt=""
      style="
        width:100%;
        height:200px;
        object-fit:cover;
        border-radius:22px;
        border:none;
        display:block;
        box-shadow:
          0 0 38px rgba(86,240,255,.25),
          0 0 18px rgba(139,92,246,.18);
      "
    />

    <img
      src="{{ '/assets/images/M-totaldeformation.png' | relative_url }}"
      alt=""
      style="
        width:100%;
        height:200px;
        object-fit:cover;
        border-radius:22px;
        border:none;
        display:block;
        box-shadow:
          0 0 38px rgba(86,240,255,.25),
          0 0 18px rgba(139,92,246,.18);
      "
    />

  </div>


  <hr style="margin: 2.2rem 0;"/>


  <h3 style="margin-bottom:.7rem;">Contact</h3>

  <div class="zf-tile" style="padding: 1.2rem 1.2rem;">

    <p style="margin: 0 0 1rem 0;">
      Email me at
      <a href="mailto:YOUR_EMAIL@cornell.edu">YOUR_EMAIL@cornell.edu</a>
    </p>

    <div style="display:flex; gap:.9rem; align-items:center; flex-wrap:wrap;">

      <a
        href="https://www.linkedin.com/in/YOUR_LINKEDIN/"
        target="_blank"
        rel="noopener"
        title="LinkedIn"
        style="display:inline-flex; align-items:center; gap:.55rem;"
      >
        <span>LinkedIn</span>
      </a>

      <a
        href="https://github.com/YOUR_GITHUB"
        target="_blank"
        rel="noopener"
        title="GitHub"
        style="display:inline-flex; align-items:center; gap:.55rem;"
      >
        <span>GitHub</span>
      </a>

    </div>

  </div>

</div>


