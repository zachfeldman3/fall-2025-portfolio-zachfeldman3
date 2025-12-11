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

# Material Properties (M42 Steel)

- Young's Modulus: $$E = 32 \times 10^6 \ \text{psi}$$
- Yield Strength: $$\sigma_y = 60 \ \text{ksi}$$
- Poisson's Ratio: $$\nu = 0.30$$
- Gauge Factor: $$GF = 2.0$$

---

# Geometry

- Length: $$L = 12 \ \text{in}$$
- Gage location: $$c = 2 \ \text{in}$$
- Vertical thickness: $$b = 0.50 \ \text{in}$$
- Horizontal width: $$h = 0.75 \ \text{in}$$

A torque of 600 in-lbf corresponds to:

$$
F = \frac{T}{L} = \frac{600}{12} = 50 \ \text{lbf}
$$

---

# Moment at Strain Gauge Location

$$
M = F(L - c)
$$

$$
M = 50(12 - 2) = 50(10) = 500 \ \text{in-lbf}
$$

---

# Cross-Section Properties

Moment of inertia (bending about horizontal neutral axis):

$$
I = \frac{h b^3}{12}
$$

$$
I = \frac{0.75(0.50^3)}{12}
= 0.0078125 \ \text{in}^4
$$

Distance from neutral axis:

$$
y = \frac{b}{2} = 0.25 \ \text{in}
$$

---

# Maximum Bending Stress

$$
\sigma_{\max} = \frac{M y}{I}
$$

$$
\sigma_{\max}
= \frac{500(0.25)}{0.0078125}
= 16.0 \ \text{ksi}
$$

---

# Factor of Safety Against Yield

$$
FS = \frac{\sigma_y}{\sigma_{\max}}
= \frac{60}{16.0}
= 3.75
$$

---

# Strain at the Gage

$$
\varepsilon = \frac{\sigma}{E}
$$

$$
\varepsilon = 
\frac{16{,}000}{32 \times 10^6}
= 5.00 \times 10^{-4}
= 500 \ \mu\varepsilon
$$

---

# Bridge Output (mV/V)

$$
\frac{\Delta R}{R}
= GF \cdot \varepsilon
= 2(5.00 \times 10^{-4})
= 1.00 \times 10^{-3}
$$

Quarter-bridge output:

$$
\frac{V_o}{V_{ex}}
\approx \frac{1}{4}
\left( \frac{\Delta R}{R} \right)
= 2.5 \times 10^{-4}
$$

For a 5 V excitation:

$$
V_o = 5(2.5 \times 10^{-4})
= 1.25 \ \text{mV}
$$

---

# Tip Deflection (Hand Calculation)

Cantilever beam deflection:

$$
\delta = \frac{F L^3}{3 E I}
$$

$$
\delta = 
\frac{50(12^3)}
{3(32 \times 10^6)(0.0078125)}
= 0.115 \ \text{in}
$$

ANSYS result:

$$
\delta_{\text{FEA}} \approx 0.085 \ \text{in}
$$

---

# Summary of Final Results

- Maximum stress: **16.0 ksi**
- Factor of safety: **3.75**
- Strain: **500 μɛ**
- Bridge output: **0.25 mV/V**
- Hand-calc deflection: **0.115 in**
- FEA deflection: **0.085 in**



