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

      <div style="margin-top:1.3rem; max-width: 62ch;">

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


  <!-- INDEX-ONLY OVERRIDES -->
  <style>
    /* HERO: remove dead space between text and image */
    .zf-hero.zf-hero-split{
      display:grid !important;
      grid-template-columns: 1.55fr 0.85fr !important; /* tighter than before */
      gap: 1.2rem !important;                          /* controls spacing */
      align-items:center !important;
    }

    .zf-hero-text{
      max-width: none !important;  /* allow the column to use its full width */
    }

    .zf-hero-image{
      justify-content:flex-end !important; /* keeps image near right edge */
      display:flex !important;
    }

    /* If you still see a big gap, this pulls the image LEFT a bit */
    .zf-hero-image img{
      margin-left: -18px !important;
    }

    /* kill hover enlarge + blue highlight on the 4 tiles */
    .zf-grid .zf-tile:hover{
      transform:none !important;
      border-color: rgba(255,255,255,.14) !important;
      box-shadow: var(--shadow2) !important;
    }
    .zf-grid .zf-tile{
      -webkit-tap-highlight-color: transparent;
      cursor: default;
    }

    /* make tags less gray + slightly bolder */
    .zf-grid .zf-tag{
      color: rgba(234,240,255,.85) !important;
      font-weight: 500 !important;
    }

    /* Mobile */
    @media (max-width: 900px){
      .zf-hero.zf-hero-split{
        grid-template-columns: 1fr !important;
        gap: 1.25rem !important;
      }
      .zf-hero-text{
        text-align:center !important;
      }
      .zf-hero-image{
        justify-content:center !important;
      }
      .zf-hero-image img{
        margin-left: 0 !important;
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


  <!-- GLOWY CTA BUTTON -->
  <div style="display:flex; justify-content:center; margin-top: 1.6rem;">

    <a
      href="{{ '/projects/' | relative_url }}"
      style="
        display:inline-flex;
        align-items:center;
        gap:.6rem;
        padding: .9rem 1.6rem;
        border-radius: 999px;
        border: 1px solid rgba(86,240,255,.45);
        background: linear-gradient(135deg, rgba(86,240,255,.22), rgba(139,92,246,.18));
        color: var(--text);
        font-weight: 600;
        letter-spacing: .02em;
        box-shadow:
          0 0 22px rgba(86,240,255,.35),
          0 0 12px rgba(139,92,246,.25),
          0 16px 38px rgba(0,0,0,.55);
        transition: transform .18s ease, box-shadow .18s ease, filter .18s ease;
      "
      onmouseover="
        this.style.transform='translateY(-2px)';
        this.style.boxShadow='0 0 32px rgba(86,240,255,.55), 0 0 18px rgba(139,92,246,.35), 0 22px 55px rgba(0,0,0,.65)';
        this.style.filter='brightness(1.08)';
      "
      onmouseout="
        this.style.transform='none';
        this.style.boxShadow='0 0 22px rgba(86,240,255,.35), 0 0 12px rgba(139,92,246,.25), 0 16px 38px rgba(0,0,0,.55)';
        this.style.filter='none';
      "
    >
      View All Projects →
    </a>

  </div>


  <hr style="margin: 2.2rem 0;"/>


  <h3 id="contact" style="margin-bottom:.7rem;">Contact</h3>

  <div class="zf-tile" style="padding: 1.2rem 1.2rem;">

    <p style="margin: 0 0 1rem 0;">
      Email me at
      <a href="mailto:zlf3@cornell.edu">zlf3@cornell.edu</a><br/>
      Call me at <a href="tel:19143567068">(914) 356-7068</a>
    </p>

    <div style="display:flex; gap:.9rem; align-items:center; flex-wrap:wrap;">

      <a
        href="https://www.linkedin.com/in/zlf3/"
        target="_blank"
        rel="noopener"
        title="LinkedIn"
        style="display:inline-flex; align-items:center; gap:.55rem;"
      >
        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" aria-hidden="true">
          <path d="M6.94 6.5A2.44 2.44 0 1 1 6.94 1.62a2.44 2.44 0 0 1 0 4.88Z" stroke="currentColor" stroke-width="1.8"/>
          <path d="M2.8 22.5h4.3V8.6H2.8v13.9Z" stroke="currentColor" stroke-width="1.8"/>
          <path d="M9.7 22.5h4.2v-7.1c0-1.9.4-3.8 2.8-3.8s2.4 2.2 2.4 3.9v7h4.2v-7.9c0-4-2.1-6.1-5.2-6.1-1.7 0-3 .9-3.6 1.8h-.1V8.6H9.7v13.9Z"
                stroke="currentColor" stroke-width="1.8"/>
        </svg>
        <span>LinkedIn</span>
      </a>

    </div>

  </div>

</div>


