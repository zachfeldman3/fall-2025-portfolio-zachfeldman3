---
title: "Torque Wrench Design Optimization"
layout: default
permalink: /projects/torquewrench/
---
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.css">YY
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/contrib/auto-render.min.js"
    onload="renderMathInElement(document.body);"></script

# Torque Wrench Design Optimization

# Torque Wrench Hand Calculations (Material: Magnesium AZ31B)

---

## Material Properties

$$E = 6.5 \times 10^6 \ \text{psi}$$  
$$\sigma_y = 21 \ \text{ksi}$$  
$$\nu = 0.35$$  
$$GF = 2.0$$  

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

## Moment at the Strain Gauge

$$M = F(L - c)$$  

$$M = 50(12 - 2) = 50(10) = 500 \ \text{in-lbf}$$  

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

# Final Summary (AZ31B Magnesium)

# Final Summary (AZ31B Magnesium)

- Maximum stress: **16.0 ksi**  
- Yield strength: **21 ksi**  
- Factor of safety: **1.31**  
- Strain: **2460 μɛ**  
- Bridge output: **1.23 mV/V**  
- Hand-calculated deflection: **0.57 in**  

All requirements satisfied:
- **mV/V > 1.15** → ✔ 1.23 mV/V  
- **FS > 1.25** → ✔ 1.31  



