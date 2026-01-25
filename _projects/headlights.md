---
layout: default
title: "Headlights & Taillights"
description: CEV Lights
category: featured
image: /assets/images/internalheadlight.png
---


<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/contrib/auto-render.min.js"
        onload="renderMathInElement(document.body);"></script>

# Headlight & Taillights 

In previous years, Cornell Electric Vehicles (CEV) did not have integrated headlight or taillight systems. Although lighting is required by the Shell Eco-marathon regulations, our “headlights” and “taillights” were previously implemented as cutouts in the carbon-fiber chassis with LED strips duct-taped to the exterior (shown below). This solution met the bare minimum competition requirements but lacked durability, safety, and any alignment with real automotive design standards.

As part of a broader effort to make our vehicle more industry-representative, I led the development of a fully integrated, industry-grade headlight and taillight system. Beyond improving aesthetics, this project introduced meaningful functional upgrades, including improved mounting robustness, environmental protection, serviceability, and regulatory compliance. The goal was not only to elevate the visual quality of the car, but to create a lighting system that could realistically exist on a production vehicle.

# Headlights 

Shell Eco-marathon rules specify that headlights must be positioned 300 mm from the centerline of the vehicle. Because headlight geometry directly constrains allowable placement under this rule, the first step was to establish a viable headlight form factor before finalizing its mounting location.

Although the headlight design itself does not significantly affect aerodynamic or electrical performance, it plays a critical role in packaging, structural integration, and overall vehicle aesthetics. I developed 17 distinct headlight concepts in CAD, exploring variations in size, profile, and mounting geometry. Each design was evaluated for regulatory compliance, packaging feasibility within the carbon-fiber chassis, and visual coherence with the vehicle’s exterior.

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/allheadlights.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

After iterative review with both the mechanical and electrical subteams, we selected Design 13 as the final concept. This design best balanced aesthetic appeal, compliance with the 300 mm placement rule, and integration constraints imposed by the chassis geometry and internal wiring routes.

After finalizing the headlight geometry, I began designing the housing and mounting system. Designing the interface between the headlight housing and the nose was the most technically challenging aspect of the project. The chassis and nose geometry were originally created in Autodesk Alias using surface modeling, resulting in complex 3D curves. In contrast, the headlight system was modeled in Fusion 360, which is better suited for solid modeling. Reconciling these two workflows required extensive use of surface-based cutting and splitting operations, using the Alias-derived nose surface as a trimming tool within Fusion 360.

<div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/headlightcurve.png' | relative_url }}"
         style="max-width:100%; max-height:400px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      3D Sketch of Headlight Projected Onto Car Surface 
    </p>
  </div>
  </div>

This process was nontrivial due to frequent zero-intersection geometry errors and surface inconsistencies, which required iterative workarounds, alternate Boolean strategies, and carefully constructed lofts to transition between the curved surface interface and the rigid mounting geometry of the headlight housing. Once the nose interface was complete, I designed the remainder of the mounting system to secure the assembly at two structural points: the top of the wheel well and the underside of the baseplate, providing additional rigidity and load sharing.

A major limitation of the previous lighting setup was poor serviceability. Because the LED strips were taped into cutouts in the nose while the main electrical systems were mounted to the bulkhead, removing the nose required unplugging the headlight wiring. This made routine access to the front of the vehicle difficult and increased the risk of damaging electrical connections during maintenance.

To resolve this, I designed a modular headlight housing system that mounts partially to the removable nose and partially to the fixed baseplate. The nose-mounted portion of the headlight features a triangular sliding joint that interfaces with the remainder of the headlight assembly mounted to the baseplate. All lighting and electrical components are integrated into the baseplate-mounted portion, allowing the nose to be removed without disconnecting any wiring. This significantly improved serviceability, enabling quick access to the drivetrain and steering systems.

<div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/headlightnose.png' | relative_url }}"
         style="max-width:100%; max-height:350px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      How Nose Interfaces With Rest of Car
    </p>
  </div>

  <!-- Image 2 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/headlightinterface.png' | relative_url }}"
         style="max-width:100%; max-height:350px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      Sliding Joint Between Both Headlight Components
    </p>
  </div>
</div>

The triangular joint also serves as a locating feature, ensuring that the nose can be reinstalled in a repeatable, precise position without manual alignment. To achieve a smooth press-fit that was neither too tight nor too loose, I performed tolerance testing using scaled 3D-printed prototypes. By systematically varying hole sizes and clearances, I converged on a tolerance that produced a reliable, low-friction sliding fit suitable for repeated assembly and disassembly.

Because the full headlight assembly was large (approximately 3,000 in³) and featured complex geometry, it could not be 3D printed as a single part. To accommodate manufacturing constraints, I segmented the design into multiple interlocking components using a combination of sliding joints and pin-and-socket style alignment features. These features allowed the printed parts to be precisely assembled and permanently bonded, while preserving the press-fit triangular joints used for the removable nose interface.

<div style="text-align:center; margin:40px 0;">

  <!-- Images row -->
  <div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; flex-wrap:wrap;">

    <!-- Image 1 -->
    <div style="max-width:45%;">
      <img src="{{ '/assets/images/headlightattachment1.png' | relative_url }}"
           style="max-width:100%; max-height:350px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    </div>

    <!-- Image 2 -->
    <div style="max-width:45%;">
      <img src="{{ '/assets/images/headlightattachment2.png' | relative_url }}"
           style="max-width:100%; max-height:350px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    </div>

  </div>

  <!-- Combined caption -->
  <p style="margin-top:12px; font-style:italic; color:#555;">
    Interfacing of the Four Different Headlight Components
  </p>

</div>

This modular approach enabled rapid prototyping of complex geometry, ensured accurate assembly, and maintained the serviceability and structural robustness required for competition use.

<div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/fullcarheadlights.png' | relative_url }}"
         style="max-width:100%; max-height:400px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      Headlights on Full Car 
    </p>
  </div>
  </div>


# Taillights 

In parallel with the headlight development, I designed a fully integrated taillight housing system to meet functional, packaging, and environmental requirements. Unlike the headlights—which were designed around a single high-intensity light source—the taillights needed to support distinct braking and turn-signal indicators, driving a more segmented internal layout.

I used the same surface-driven workflow developed for the headlights, deriving geometry directly from the vehicle body using surface offsets, splitting tools, and Boolean combine/cut operations to ensure a seamless aerodynamic interface. However, the taillight geometry was more complex: the housing follows a continuously curved profile along its entire length, rather than transitioning from a curved surface to planar faces as in the headlight design.

The taillight assembly consists of two primary components:
1. a main structural housing that mounts directly to the baseplate, and
2. a secondary retention frame secured via heat-set inserts.

<div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/2componentaillight.png' | relative_url }}"
         style="max-width:100%; max-height:400px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      Taillight Split Into Both Components
    </p>
  </div>
  </div>

This frame captures a curved acrylic lens panel that slides into place, sealing and protecting the internal electronics from rain and debris—an environmental protection feature that was unnecessary for the internally mounted headlights.

To ensure serviceability and structural robustness, the complete taillight module is fastened to the baseplate using five 1/4-20 screws, allowing for quick removal while maintaining precise alignment and load distribution. The external placement of the taillights was enabled by packaging clearance beneath the rear baseplate tail, allowing the assembly to remain fully flush with the vehicle body without protrusions.

<div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/2componentaillight.png' | relative_url }}"
         style="max-width:100%; max-height:400px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      View Of Taillight Mounting Holes
    </p>
  </div>
  </div>

This design emphasized aerodynamic integration, manufacturability, environmental sealing, and modular service access, while maintaining visual consistency with the headlight architecture.

<div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/fullcartaillights.png' | relative_url }}"
         style="max-width:100%; max-height:400px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      Taillights on Full Car
    </p>
  </div>
  </div>

