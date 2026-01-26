---
layout: default
title: "Automatic Basketball Return System"
description: Automatic Basketball Return System
category: class
image: /assets/images/basketballpurple2.png
---


<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/contrib/auto-render.min.js"
        onload="renderMathInElement(document.body);"></script>

# Automatic Basketball Return System
Cornell MAE 2250 | Team Design Project | Spring 2025
Role: Mechanical Design, Manufacturing Strategy, Assembly & Integration

## Problem

Mini basketball hoops are fun, but solo play is interrupted every time the ball has to be retrieved after a made shot. This makes it difficult to build rhythm and sustain practice or gameplay.

## Solution Overview

LeMiniHoop is a compact, over-the-door basketball return system that automatically sends the ball back to the shooter after each made shot. The system funnels the ball into a powered return mechanism and launches it back at adjustable speed and distance, enabling continuous solo play.

## System Architecture

Ball Handling & Return Mechanism:
- A gravity-fed ramp guides the ball into a pair of counter-rotating flywheels.
- The flywheels grip and launch the ball back to the shooter at the same height.
- Flywheels are driven by DC motors through a 100:12 gear reduction.
- Return distance is adjustable via a speed control knob.

<div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/systemarchitecture.png' | relative_url }}"
         style="max-width:100%; max-height:400px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      Ball Handling & Return Mechanism
    </p>
  </div>
  </div>

Structural Housing:
- Laser-cut acrylic side plates, base, and back wall form a rigid enclosure.
- Interlocking “puzzle-joint” edges constrain orientation and simplify alignment during assembly.

<div style="display:flex; gap:30px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:22%;">
    <img src="{{ '/assets/images/drawing1.png' | relative_url }}"
         style="max-width:100%; max-height:350px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
  </div>

  <!-- Image 2 -->
  <div style="text-align:center; max-width:22%;">
    <img src="{{ '/assets/images/drawing2.png' | relative_url }}"
         style="max-width:100%; max-height:350px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
  </div>

  <!-- Image 3 -->
  <div style="text-align:center; max-width:22%;">
    <img src="{{ '/assets/images/drawing3.png' | relative_url }}"
         style="max-width:100%; max-height:350px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
  </div>

  <!-- Image 4 -->
  <div style="text-align:center; max-width:100%;">
    <img src="{{ '/assets/images/drawing4.png' | relative_url }}"
         style="max-width:100%; max-height:350px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
  </div>

</div>

<!-- Single combined caption -->
<p style="text-align:center; margin-top:12px; font-style:italic; color:#555;">
  Drawings Of The Acrylic Housing
</p>

<div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:45%;">
    <img src="{{ '/assets/images/acryllic.png' | relative_url }}"
         style="max-width:100%; max-height:400px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      Final Laser Cut Acrylic Housing
    </p>
  </div>
  </div>


Controls & Feedback:
- Manual speed control knob governs flywheel RPM.
- LED lights embedded in the backboard flash when a shot is made, providing immediate visual feedback.

## Design & Build Process
I was heavily involved in the end-to-end mechanical build and integration of the prototype:
- Hand calculations to size flywheels, gearing, and motor requirements
- CAD design of the housing, ramp, gears, and flywheels
- 3D printing of flywheels
- Laser cutting of acrylic structural panels and gears
- Drilling, sawing, and manual fitting of axles and brackets
- Mechanical assembly and electrical wiring

## Design for Manufacturing (DFM)
I led the analysis of how the prototype would translate to scalable production:

Flywheels:
- 3D-printed PLA → rotationally molded polypropylene
        -Faster production
        -Improved mass consistency
        -Lower unit cost
  
Gears:
- Laser-cut acrylic → injection-molded acetal
        -Improved tolerance control
        -Better meshing and durability
  
Ramp:
- Laser-cut plywood → injection-molded polypropylene
        -Thin-wall redesign
        -Integrated mounting features
  
Axles:
- Hand-sawed + belt-sanded steel → CNC-milled steel
        - Improved concentricity and repeatability
  
## Design for Assembly (DFA)
I implemented multiple CAD and hardware changes to reduce assembly time and user error:
Added gear covers to:
- Shield moving components
- Prevent incorrect side-plate orientation (poka-yoke)
- Redesigned ramp mounting:
- Slot-and-tab → screw-mounted flanges
- Enabled ramp installation after housing assembly
- Reduced assembly from a multi-person operation to one person
- Standardized all fasteners to 8-32 hardware
- Replaced epoxy joints with mechanical fasteners for serviceability

## Key Engineering Challenges
Motor Spin-Up Limitation:
- The DC motors required continuous operation due to slow spin-up time, making motion-sensor-based triggering impractical. This exposed a core system-level limitation tied to motor selection and power management.

Tolerance Stack-Up: 
- Initial axle-to-gear fits required post-machining adjustment. I revised tolerance targets and interface fits to eliminate sanding and shimming in later iterations.

Late-Stage Interference: 
- Mechanical interference between the ramp and gear train revealed the importance of fully validating CAD assemblies before fabrication.

##  Outcome

The final prototype reliably returned the ball after made shots, supported adjustable launch distance, and provided interactive LED feedback. The system validated the mechanical concept while revealing key limitations tied to motor performance, gearing durability, and assembly complexity.

## Future Considerations: 

- Replace motors with faster spin-up units to enable sensor-based triggering
- Injection-mold ramp and gears for durability and consistency
- Integrate all mounts and electronics features directly into CAD
