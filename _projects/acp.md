---
layout: default
title: "Chassis Structural Analysis"
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
I first performed hand calculations to estimate the compressive stress beneath the washer footprint using an effective diameter load-spreading model. The analysis focused on determining whether the required bolt preload could be achieved without exceeding the allowable compressive stress of the foam core.

The calculations showed that the preload required for proper bolt pretension would induce core compressive stresses well above the 203 psi crush limit, meaning the core would fail in local crushing long before reaching the necessary clamp force.

  <div style="display:flex; gap:40px; justify-content:center; align-items:flex-start; margin:40px 0; flex-wrap:wrap;">

  <!-- Image 1 -->
  <div style="text-align:center; max-width:100%;">
    <img src="{{ '/assets/images/baseplatecalcs2.png' | relative_url }}"
         style="max-width:100%; max-height:1200px; height:auto; border-radius:12px; display:block; margin:0 auto;" />
    <p style="margin-top:10px; font-style:italic; color:#555;">
      Hand Calculations
    </p>
  </div>
  </div>


## ANSYS ACP Validation

To validate the analytical results, we modeled the bolted region directly in ACP. The clamp load was applied through a representative washer diameter (≈0.75 in), and the through-thickness compressive stress in the foam core was evaluated under increasing preload.

A baseline preload of 1000 N was applied and scaled upward to determine the maximum allowable clamp force before core crushing occurred. The ACP failure results showed that core crushing began at approximately ~2000 N maximum allowable preload This value remains far below the force required to properly pretension a 1/2–20 bolt, confirming the hand-calculation conclusion.

## Engineering Conclusion
This study demonstrated that direct bolt pretensioning into a sandwich baseplate is not structurally viable without additional reinforcement. The governing failure mode is local foam core crushing, not facesheet tensile failure.

Based on these results, future design solutions include:
- Larger load-spreading washers
- Potted inserts or embedded hardpoints
- Local aluminum backing plates
- Solid laminate build-ups in bolted attachment regions
- This work combined first-principles hand analysis with composite FEA validation to guide a more robust chassis joint and mounting strategy.
