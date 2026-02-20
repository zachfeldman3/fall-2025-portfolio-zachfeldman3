---
layout: default
title: "Chassis Structural Analysis (Unfinished)"
description: ACP
category: featured
image: /assets/images/acpdeformation2.png
---
# Chassis Baseplate Structural Validation (ANSYS ACP)

The goal of this project was to verify that the carbon fiber sandwich chassis baseplate is structurally capable of sustaining the primary loads experienced by the vehicle. The baseplate is one of the most critical components in the chassis, as it supports the full mass of the car (≈220 kg) and serves as the primary load path between the suspension mounting regions and the rest of the structure.

The baseplate was designed as a carbon fiber sandwich panel with the following layup:

[90 / ±45 / 90] carbon fiber facesheet
0.5 in Divinycell foam core
[90 / ±45 / 90] carbon fiber facesheet

To evaluate the structure, we used ANSYS ACP (Composite PrepPost) to model the full sandwich laminate, including ply orientations, orthotropic material behavior, and core response. We applied the ACP composite failure evaluation tools to assess local stress concentrations and potential failure modes.


## Loading Environment

The baseplate experiences a combination of global and localized loads during operation, including:
- Vehicle weight and component mass, including driver loading
- Axial and drivetrain-related loads transmitted through chassis interfaces
- Suspension and wheel well load transfer, where forces enter the baseplate through bolted joints
  
Because many of these loads are introduced through mechanical attachments, joint integrity and local crushing resistance are critical design concerns.

## Bolt Pretensioning & Core Crushing Analysis

A key design question was whether the sandwich baseplate could safely support bolt clamp-up forces without crushing the foam core.
The joint under evaluation used a:
- 1/2–20 bolt
- The Divinycell foam core had a compressive crush strength of approximately: 203 psi

## Hand Calculation Approach

This analysis was performed to determine the maximum allowable bolt preload in the carbon-fiber sandwich baseplate without causing core crushing or local facesheet failure. Because the structure consists of carbon facesheets bonded to a 0.5-inch Divinycell core, bolt pretension introduces a localized compressive load path through the washer, facesheet, and core. To model this, a 45-degree load-spreading assumption was used to calculate an effective compression diameter beneath the washer, reflecting how compressive forces distribute through the core thickness. The corresponding annular area resisting compression was then determined, excluding the bolt hole.

The compressed core region was modeled as a short column in axial compression, and its stiffness was calculated using the classical relation k = AE/L, where A is the effective area, E is the core’s compressive modulus, and L is the core thickness. An allowable compression displacement was defined based on strain limits, and the maximum preload was computed using the linear elastic relation P = kΔ. A secondary stress check under the facesheet was performed using force divided by area to ensure local compressive stresses remained below allowable values. The resulting preload was then applied in ANSYS ACP to validate that no composite failure indices exceeded limits, confirming the analytical model.


  <div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:100%;">
    <img src="{{ '/assets/images/acphandcalcs2.png' | relative_url }}"
         style="max-width:100%; max-height:1200px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      Hand Calculations
    </p>
  </div>
  </div>


## ANSYS ACP Validation

To validate the analytical results, we modeled the bolted region directly in ACP. The clamp load was applied through a representative washer diameter (≈0.75 in), and the through-thickness compressive stress in the foam core was evaluated under increasing preload.

A baseline preload of 1000 N was applied and scaled upward to determine the maximum allowable clamp force before core crushing occurred. The ACP failure results showed that core crushing began at approximately ~2000 N maximum allowable preload This value remains far below the force required to properly pretension a 1/2–20 bolt, confirming the hand-calculation conclusion.

## Surface Mesh

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/acpmesh.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

## FEM Model with Loads and Boundary Conditions

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/acpforces2.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

## Total Deformation

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/acpdeformation3.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

## Equivalent Stress (Von Misses)

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/acpestress.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

## Equivalent Elastic Strain

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/acpstrain.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

## Maximum Principal Elastic Strain

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/acppstrain.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">



## Engineering Conclusion
This study demonstrated that direct bolt pretensioning into a sandwich baseplate is not structurally viable without additional reinforcement. The governing failure mode is local foam core crushing, not facesheet tensile failure.

Based on these results, future design solutions include:
- Larger load-spreading washers
- Potted inserts or embedded hardpoints
- Local aluminum backing plates
- Solid laminate build-ups in bolted attachment regions
- This work combined first-principles hand analysis with composite FEA validation to guide a more robust chassis joint and mounting strategy.
