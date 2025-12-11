---
title: "Torque Wrench Design Optimization"
layout: default
permalink: /projects/torquewrench/
---

# Torque Wrench Design Optimization

# Torque Wrench Hand Calculations (M42 Tool Steel)

## Material Properties (M42 Steel)
\[
E = 32 \times 10^6 \, \text{psi}
\]
\[
\sigma_y = 60 \, \text{ksi}
\]
\[
\nu = 0.30
\]
Gauge factor:
\[
GF = 2.0
\]

---

## Geometry
\[
L = 12 \, \text{in}, \qquad 
c = 2 \, \text{in}
\]
\[
b = 0.50 \, \text{in} \quad (\text{vertical thickness})
\]
\[
h = 0.75 \, \text{in} \quad (\text{horizontal width})
\]

A 600 in-lbf torque applied at the handle corresponds to a force:
\[
F = \frac{T}{L} = \frac{600}{12} = 50 \, \text{lbf}
\]

---

## Moment at Strain Gauge Location
\[
M = F (L - c)
\]
\[
M = 50(12 - 2) = 50(10) = 500 \, \text{in-lbf}
\]

---

## Cross-Section Properties  
Rectangular section bending about the horizontal neutral axis:
\[
I = \frac{h b^3}{12}
\]
\[
I = \frac{0.75(0.50^3)}{12}
= 0.0078125 \, \text{in}^4
\]

Distance from neutral axis to outer fiber:
\[
y = \frac{b}{2} = 0.25 \, \text{in}
\]

---

## Maximum Bending Stress
\[
\sigma_{\max} = \frac{My}{I}
\]
\[
\sigma_{\max} = 
\frac{500(0.25)}{0.0078125}
= 16.0 \, \text{ksi}
\]

---

## Factor of Safety Against Yield
\[
FS = \frac{\sigma_y}{\sigma_{\max}}
= \frac{60}{16.0}
= 3.75
\]

---

## Strain at the Strain Gauge
\[
\varepsilon = \frac{\sigma}{E}
\]
\[
\varepsilon = 
\frac{16{,}000}{32 \times 10^6}
= 5.00 \times 10^{-4}
\]
\[
\varepsilon = 500 \, \mu\varepsilon
\]

---

## Bridge Output (mV/V)
Quarter-bridge approximation:
\[
\frac{\Delta R}{R} = GF \cdot \varepsilon
\]
\[
\frac{\Delta R}{R} = 2(5.00 \times 10^{-4})
= 1.00 \times 10^{-3}
\]

Quarter-bridge output:
\[
\frac{V_o}{V_{ex}} 
\approx \frac{1}{4} \left( \frac{\Delta R}{R} \right)
\]
\[
\frac{V_o}{V_{ex}}
= \frac{1}{4}(1.00 \times 10^{-3})
= 2.50 \times 10^{-4}
\]

Thus the sensitivity is:
\[
\boxed{
\frac{V_o}{V_{ex}} = 0.25 \, \text{mV/V}
}
\]

If using a 5V excitation:
\[
V_o = (0.25 \, \text{mV/V})(5 \, \text{V})
= 1.25 \, \text{mV}
\]

---

## Tip Deflection (Hand Calculation)
For a cantilever beam:
\[
\delta = \frac{F L^3}{3 E I}
\]

\[
\delta = 
\frac{50(12^3)}{
3(32 \times 10^6)(0.0078125)
}
\]

\[
\delta = 0.115 \, \text{in}
\]

ANSYS Simulation Result:
\[
\delta_{\text{FEA}} \approx 0.085 \, \text{in}
\]

Difference explained by:
- drive-block stiffening,
- reduced effective beam length,
- 3D constraint effects,
- shear deformation.

---

## Final Results Summary

\[
\sigma_{\max} = 16.0 \, \text{ksi}
\]

\[
FS = 3.75
\]

\[
\varepsilon = 500 \, \mu\varepsilon
\]

\[
\frac{V_o}{V_{ex}} = 0.25 \, \text{mV/V}
\]

\[
\delta_{\text{hand}} = 0.115 \, \text{in}, 
\quad
\delta_{\text{ANSYS}} = 0.085 \, \text{in}
\]

All results consistent with the beam model and simulation constraints.


