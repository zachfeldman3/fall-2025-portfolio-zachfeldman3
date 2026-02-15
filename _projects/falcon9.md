---
layout: default
title: "Falcon 9 Rocket Model"
description: Falcon 9 Model Rocket 
category: featured
image: /assets/images/falcon9tall4.png
---

Multi-Material IDEX CAD & Additive Manufacturing Project
1:144 Scale Modular Falcon-Style Rocket Assembly (Raise3D E2)
This project involved the complete CAD design and multi-material additive manufacturing of a 1:144 scale Falcon-style rocket assembly, developed specifically around the constraints and capabilities of an Independent Dual Extruder (IDEX) 3D printing workflow. The objective was to create a highly repeatable, support-free, press-fit model that could be produced as an essentially finished part directly off the printer—eliminating the need for painting, heavy post-processing, or permanent bonding.
The final design was optimized for manufacturability, modular replacement, and repeatable production, using only four primary printed components with clean mechanical interfaces. Total material cost was approximately $10, demonstrating an efficient, low-cost, high-quality prototyping workflow.
Printing Platform and Manufacturing Constraints
Printer: Raise3D E2 (IDEX dual extruder system)
Material: PETG (all components)
Nozzle Diameter: 0.4 mm
Layer Height: 0.10 mm (high-resolution finish)
Multi-material process: Purge tower used for clean transitions
Support strategy: Entire assembly designed to print without supports
Total print time: < 24 hours across all modules
A key design constraint was limiting each printed module to a maximum of two colors per part, while still achieving clear visual and functional separation between engine hardware, structural features, and airframe surfaces.
Bottom-Up System Architecture and Design Development
1. Engine Base Module (Merlin Cluster + Structural Reinforcement)
The design process began at the lowest section of the rocket with the Merlin engine cluster. A single engine was modeled and duplicated into a full nine-engine array using the circular pattern tool.
Early prototypes revealed a major durability issue: the engines were initially connected only through a small tip interface and would snap off easily during handling. To solve this, I redesigned the base with a recessed engine seating indentation, allowing each Merlin to print into the structure rather than protruding as a fragile feature.
This modification significantly improved robustness and made the engine cluster mechanically stable.
Key improvements:
Engine snap-off failure resolved through recessed mounting geometry
Hollow internal base to reduce material usage and print time
Clean color transition from black base structure to gray engine hardware
Supportless Printing Orientation
To eliminate supports entirely, the base module was printed upside down, ensuring that the Merlin nozzle edges and fine features printed upward rather than downward. Printing in the opposite orientation would have required extensive supports and reduced surface quality.
Chamfers were also added throughout the design to maintain printable overhang angles and improve press-fit insertion.
2. Internal Press-Fit Alignment Core
The base module includes a hollow internal cavity and a cylindrical press-fit insert with an alignment feature. This internal core provides:
Axial structural reinforcement
Repeatable alignment for stacking the next stage
A clean modular interface without fasteners or adhesives
3. Main Body Module (Landing Legs + Dual Extrusion Features)
The central body section incorporates the landing leg geometry, modeled once and repeated symmetrically using circular patterning.
This module was printed using dual extrusion due to the external black structural accents running vertically along the stage. These features were integrated directly into the print rather than painted, improving durability and repeatability.
The upper portion includes a reduced-diameter cylinder designed as a self-aligning press-fit interface to the interstage above.
4. Interstage / Grid Fin Module (Complex Surface Modeling)
The upper black module houses the grid fin region, which was one of the most geometrically complex portions of the project. The grid fins were modeled using curved surfaces combined with repeated patterned cutting operations to achieve a realistic lattice structure while maintaining slicer-friendly thickness.
This module is hollow and also serves as an internal housing volume for the vacuum Merlin engine component of the upper stage.
5. Upper Stage Module (Vacuum Merlin + Removable Assembly)
The top stage includes a vacuum Merlin engine printed in gray, integrated into a white fairing/body structure. The interface was designed with smooth press-fit tolerances, allowing the entire upper engine module to be removed and reinserted cleanly.
This modular approach enables:
Easy disassembly
Replacement of individual damaged modules
A clean finished assembly without permanent bonding
Engineering Challenges and Iterative Development
This project required extensive calibration and iterative refinement, with approximately 30 prototype prints produced to converge on reliable fit and surface quality.
Key challenges addressed included:
PETG warping and shrink effects
Press-fit tolerances initially too tight or too loose
Dual-extrusion color bleed requiring purge optimization
Layer adhesion tuning for thin structural features
Slicer stability for lattice/grid fin geometry
Final press-fit interfaces were designed around a clearance of approximately:
0.01 inches for consistent friction-fit assembly
Outcome and Skills Demonstrated
The final result is a fully modular, support-free, multi-material rocket assembly that can be printed repeatedly with minimal post-processing and replaced component-by-component if damaged.
Skills demonstrated:
Advanced CAD modeling and modular mechanical design
Circular patterning for propulsion and structural symmetry
Design-for-additive-manufacturing (DfAM) without supports
Multi-material IDEX process planning and calibration
Press-fit tolerance engineering and iterative prototyping
Complex surface + lattice modeling for grid fin structures
