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
    </div>

    <div class="zf-hero-image">
      <img src="{{ '/assets/images/zachpfp.jpeg' | relative_url }}" alt="Zach Feldman" />
    </div>

  </div>


  <!-- =====================================================
       Ghosted background behind the 4 tiles
       ===================================================== -->
  <div style="position:relative; border-radius:24px; overflow:hidden;">

    <img
      src="{{ '/assets/images/2024chassis.png' | relative_url }}"
      alt=""
      style="
        position:absolute;
        inset:0;
        width:100%;
        height:100%;
        object-fit:cover;
        opacity:.06;
        filter: blur(2px);
        pointer-events:none;
        z-index:0;
      "
    />

    <div class="zf-grid" style="position:relative; z-index:1;">

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


  <hr/>


  <!-- =====================================================
       Ghosted background behind About Me
       ===================================================== -->
  <div style="position:relative; border-radius:24px; overflow:hidden; padding: .25rem 0;">

    <img
      src="{{ '/assets/images/M-totaldeformation.png' | relative_url }}"
      alt=""
      style="
        position:absolute;
        inset:0;
        width:100%;
        height:100%;
        object-fit:contain;
        opacity:.07;
        filter: blur(1px);
        pointer-events:none;
        z-index:0;
      "
    />

    <div style="position:relative; z-index:1; padding: 0.75rem 0;">
      <h3>About Me</h3>

      <p>
        My name is Zach Feldman, and I am a Mechanical Engineering student at Cornell University with interests in product design,
        manufacturing, and hands-on engineering projects. I enjoy creating practical, meaningful solutions—from carbon-fiber components
        for Cornell Electric Vehicles to mechanical systems built in class and personal projects. I’m passionate about learning new
        engineering tools, building things that work, and continuously improving my technical skills.
      </p>

      <p>
        Take a look at <a href="{{ '/projects/' | relative_url }}">my projects</a> and <a href="{{ '/cv/' | relative_url }}">my CV</a>.
      </p>
    </div>

  </div>

</div>


