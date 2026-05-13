---
layout: default
title: "Mechatronics Robot Competition Project"
description: Mechatronics Robot Competition Project
category: class
image: /assets/images/mechrobot.png
---

# Mechatronics Robot Competition

Led the design, CAD development, manufacturing, electrical integration, and controls strategy for a high-speed autonomous competition robot designed to rapidly collect cubes in a one-minute arena challenge. Rather than following the common sensor-heavy approach used by most teams, I focused the entire robot architecture around a simpler but highly optimized strategy: reaching the cube field before opponents and collecting a majority of the scoring objects in a single aggressive sweep. The robot used a fully hard-coded autonomous path tuned through extensive iterative testing, prioritizing repeatability, acceleration, and speed over reactive sensing systems.

I independently designed the robot chassis and intake system in CAD, iterating through seven major revisions to optimize weight distribution, turning stability, and cube collection efficiency. The intake geometry was specifically shaped to funnel cubes inward while maintaining a lightweight structure that could withstand repeated high-speed impacts. Because nearly the entire project budget was consumed by a single large-format 3D print, the design process required careful upfront planning and validation rather than relying on rapid re-manufacturing cycles.

A major focus of the project was extracting significantly higher drivetrain performance than competing robots despite all teams receiving identical hardware. To achieve this, I developed a custom 15V power configuration by wiring the provided 6V and 9V battery systems in series, dramatically increasing motor speed and acceleration. Running the electronics above their rated voltage introduced reliability challenges, so I implemented electrical mitigation strategies including capacitors across motor terminals to suppress voltage spikes and prevent brownouts during rapid load changes. Extensive testing was performed to balance maximum speed with system stability and component survivability.

I also developed the robot’s autonomous controls architecture in embedded C using AVR register-level programming. To eliminate the startup delay caused by Arduino resets used by most teams, I implemented a push-button launch system that allowed the control code to remain preloaded before each round, enabling instantaneous robot deployment when the match began. Movement timing, turning radii, and path geometry were repeatedly refined through testing to maximize consistency and cube acquisition efficiency.

The final robot placed first overall in competition, validating the design philosophy of prioritizing strategic simplicity, aggressive optimization, and execution speed over unnecessary system complexity.
