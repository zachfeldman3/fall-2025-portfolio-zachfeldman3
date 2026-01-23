---
layout: default
title: ""
permalink: /
---

<div class="zf-home">

  <div class="zf-hero zf-hero-split">

    <!-- LEFT SIDE -->
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

      <!-- About Me INSIDE HERO -->
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

    <!-- RIGHT SIDE: SQUARE PORTRAIT -->
    <div class="zf-hero-image">

      <img
        src="{{ '/assets/images/zachpfp.jpeg' | relative_url }}"
        alt="Zach Feldman"
        style="
          width: 300px;
          height: 400px;
          object-fit: cover;
          border-radius: 22px;
          border: 1px solid rgba(255,255,255,.16);
          box-shadow: 0 18px 55px rgba(0,0,0,.55);
        "
      />

    </div>

  </div>


  <!-- Tiles section stays the same -->
  <div class="zf-grid">

    <a class="zf-tile" href="{{ '/about/' | relative_url }}">
      <h3>Interests</h3>
      <div class="zf-tags">
        <span class="zf-tag">Manufacturing</span>
        <span class="zf-tag">Composites</span>
        <span class="zf-tag">Additive</span>
        <span class="zf-tag">Design</span>
      </div>
    </a>

    <a class="zf-tile" href="{{ '/projects/' | relative_url }}">
      <h3>Skills</h3>
      <div class="zf-tags">
        <span class="zf-tag">CAD</span>
        <span class="zf-tag">3D Printing</span>
        <span class="zf-tag">Machining</span>
        <span class="zf-tag">Manufacturing</span>
      </div>
    </a>

    <a class="zf-tile" href="{{ '/projects/' | relative_url }}">
      <h3>What I’m Doing Now</h3>
      <div class="zf-tags">
        <span class="zf-tag">Cornell EV</span>
        <span class="zf-tag">Chassis Lead</span>
        <span class="zf-tag">Composites</span>
        <span class="zf-tag">Manufacturing</span>
      </div>
    </a>

    <a class="zf-tile" href="{{ '/cv/' | relative_url }}">
      <h3>What I’m Looking For</h3>
      <div class="zf-tags">
        <span class="zf-tag">Spring 2027 Co-op</span>
        <span class="zf-tag">Summer 2027 Full Time Engineering Position</span>
      </div>
    </a>

  </div>

</div>


