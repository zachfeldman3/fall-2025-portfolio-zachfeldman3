---
title: "Torque Wrench Design Optimization"
layout: default
permalink: /projects/torquewrench/
---


<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/contrib/auto-render.min.js"
        onload="renderMathInElement(document.body);"></script>

# Torque Wrench Design Optimization


## Torque Wrench Hand Calculations (Material: Magnesium AZ31B)

---

## Material Properties

$$E = 6.5 \times 10^6 \ \text{psi}$$  
$$\sigma_y = 21 \ \text{ksi}$$  
$$\nu = 0.35$$  

---

## Geometry

$$L = 12 \ \text{in}$$  
$$c = 2 \ \text{in}$$  
$$b = 0.50 \ \text{in}$$  
$$h = 0.75 \ \text{in}$$  

Applied torque:

$$T = 600 \ \text{in-lbf}$$  

Equivalent force:

$$F = \frac{T}{L} = \frac{600}{12} = 50 \ \text{lbf}$$  

---

## Cross-Section Properties

Moment of inertia about horizontal neutral axis:

$$I = \frac{h b^3}{12}$$  

$$I = \frac{0.75(0.50^3)}{12}
= 0.0078125 \ \text{in}^4$$  

Distance from neutral axis:

$$y = \frac{b}{2} = 0.25 \ \text{in}$$  

---

## Maximum Bending Stress

$$\sigma_{\max} = \frac{M y}{I}$$  

$$\sigma_{\max}
= \frac{500(0.25)}{0.0078125}
= 16.0 \ \text{ksi}$$  

---

## Factor of Safety (Yield)

$$FS = \frac{\sigma_y}{\sigma_{\max}}$$  

$$FS = \frac{21}{16} = 1.31$$  

---

## Strain at the Strain Gauge

$$\varepsilon = \frac{\sigma}{E}$$  

$$\varepsilon = \frac{16{,}000}{6.5 \times 10^6}
= 0.00246$$  

$$\varepsilon = 2460 \ \mu\varepsilon$$  

---

## Strain-Gage Bridge Output (mV/V)

##Gauge Factor (GF) = 2$$

Resistance change:

$$\frac{\Delta R}{R} = GF \cdot \varepsilon$$  

$$\frac{\Delta R}{R} = 2(0.00246)
= 0.00492$$  

Quarter-bridge output:

$$\frac{V_o}{V_{ex}} = 
\frac{1}{4} \left( \frac{\Delta R}{R} \right)$$  

$$\frac{V_o}{V_{ex}}
= \frac{1}{4}(0.00492)
= 0.00123 \ \text{V/V}$$  

Convert to mV/V:

$$0.00123 \ \text{V/V}
= 1.23 \ \text{mV/V}$$  

---

## Tip Deflection

Cantilever deflection formula:

$$\delta = \frac{F L^3}{3 E I}$$  

Compute:

$$\delta = 
\frac{50(12^3)}
{3(6.5 \times 10^6)(0.0078125)}$$  

$$\delta = 0.567 \ \text{in}$$  

---

## Final Summary (AZ31B Magnesium)

- Maximum stress: **16.0 ksi**  
- Yield strength: **21 ksi**  
- Factor of safety: **1.31**  
- Strain: **2460 μɛ**  
- Bridge output: **1.23 mV/V**  
- Deflection: **0.57 in**  


## Basic Design Concept:

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/TW-asset-6.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">


## Engineering Drawing:

<a href="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/TorqueWrench+Drawing.pdf" target="_blank">
  <img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/TorqueWrench+Drawing.pdf"
       alt="Engineering Drawing Preview"
       style="max-width: 90%; height: auto; display: block; margin: auto;">
</a>

## FEM Model with Loads and Boundary Conditions

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/force+displacement.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">


The image above shows the finite element model used to validate the torque wrench design under the required 600 in-lbf load. The simulation replicates the real bending condition by fixing the drive end and applying the equivalent handle force.

---

### **1. Boundary Condition — Fixed Support at Drive End**

The yellow region represents the 3/8-inch square drive where the wrench interfaces with the socket.

- This region is fully constrained: **Ux = Uy = Uz = 0**
- This simulates the wrench being rigidly held at the bolt during tightening
- No rotation or translation is allowed at this end

This fixed support provides the reaction necessary for the wrench to develop torque.

---

### **2. Applied Load — 50 lbf Equivalent Force**

A torque of 600 in-lbf is applied by applying a force at the handle tip:

$$F = \frac{T}{L} = \frac{600\ \text{in-lbf}}{12\ \text{in}} = 50\ \text{lbf}$$

In the model:

- A **50 lbf** force (red arrow) is applied to the far right end face of the wrench
- The force direction is perpendicular to the beam, generating bending
- This creates the same moment experienced during actual wrench use

---
## Total Deformation / Deflection: 

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/M-totaldeformation.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

## Normal Stress: 

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/M-normalstressFULL.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/M-normalstress.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

## Normal Elastic Strain FEM Results:

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/M-normalelasticstrainSIDE" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/M-normalelasticstrain.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

## Maximum Principal Stress: 

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/M-maximumprincipalstressFULL.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/M-maximumprincipalstress.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">


## Sensitivity of the torque wrench in mV/V using strain at the gauge location: 

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/mv:v.png" 
     alt="Basic Design Concept"
     style="max-width: 90%; height: auto; display: block; margin: auto;">

In the ANSYS model, the strain probe at the gauge location reports a Z-direction strain that corresponds to a torque-wrench sensitivity of about 1.616 mV/V. This value is higher than the hand-calculated sensitivity of approximately 1.23 mV/V, but the two results are still reasonably close. The difference is expected because the finite element model captures the full 3-D deformation and localized strain distribution in the wrench, whereas the hand calculation relies on  idealized assumptions. Overall, the FEA result validates the hand-calculated estimate while providing a slightly more realistic prediction of the actual strain-based output

## Strain Gauge Selected:

A Vishay Micro-Measurements CEA-06-125UN-350 uniaxial foil strain gauge was selected for this design. This gauge has a 0.125-inch active grid length, a compact overall footprint of roughly 0.20 × 0.30 inches, a resistance of 350 Ω, and a gauge factor of 2.0, making it easy to bond to the 0.5-inch-wide wrench surface while providing accurate measurement of bending strains at the gauge location.

     
