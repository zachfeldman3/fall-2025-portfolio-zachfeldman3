---
title: "RC"
layout: default
permalink: /projects/RC/
---
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.4/dist/contrib/auto-render.min.js"
        onload="renderMathInElement(document.body);"></script>


        
# RC Car Dissection  

**Project Purpose and Role**

This project focuses on modeling the open-loop longitudinal dynamics of a small RC car using ordinary differential equations (ODEs), experimental observations, and system-level modeling techniques. The objective of the project is to understand how electrical inputs to the motor are converted into mechanical motion of the vehicle and how disturbances affect the system’s behavior.

My role in this project was to create and evaluate the **block diagram representation** of the RC car system. This involved translating the torque-based ODEs derived earlier in the project into a clear block-diagram structure, explaining the physical meaning of each component, and showing how the diagram relates to the governing equations and experimental measurements.

---

The block diagram of this system represents the open-loop longitudinal dynamics of our RC car. It simplifies the complex physical dynamics and electrical ODEs into individual components so that we can visualize how electrical energy is converted into mechanical motion. Instead of dealing directly with abstract differential equations, the block diagram breaks the system down into functional pieces, with each block representing a physical process or mathematical operation.

The block diagram shown is based specifically on the ODEs derived by Jason earlier in the project. It uses the **torque-based ODE formulation**, and disturbance torque has been included to take into account Callum’s experimental measurements. Ultimately, the diagram simplifies the conversion of electricity into torque production and captures the mechanical vehicle dynamics by providing a clear input–output structure. Because there is no feedback control implemented in our RC car, the block diagram represents an **open-loop system**.

<img src="https://zachfeldman3.github.io/fall-2025-portfolio-zachfeldman3/assets/images/BlockDiagram.png" 
     alt="Basic Design Concept"
     style="max-width: 50%; height: auto; display: block; margin: auto;">

The block diagram structure uses **torque**, not current, to model the system. This is because the signal entering the mechanical system from the motor is torque. The car itself—including the gears, wheels, and chassis—never receives current as a physical input. Because of this, the equation inside the open-loop mechanical block must use torque as the input, leading to the governing equation:


$$\dot{v} = \frac{T}{M_{eq}}$$


Additionally, the disturbance torque measured by Callum can only be considered in a block diagram where torque is treated as the input. This allows the disturbance torque $$T_d$$ to be added before the open-loop mechanical block. If the open-loop block instead used current as its input, there would be no physically meaningful location to include the disturbance torque.

The first block in the diagram represents the **input voltage**, $$V$$. This voltage corresponds to the command sent from the RC controller to the car. When a signal is sent, it sets the electrical potential that drives current into the DC motor. This voltage is the user’s control input and serves as the ultimate source of mechanical motion in the system. The voltage term $$V$$ appears explicitly in the electrical ODE derived earlier in the project.

Next, the **power amplifier and motor block** combines the battery power delivery, motor driver, and DC motor electrical dynamics. Within this block, electrical energy is converted into mechanical energy. The relationship

$$T_u = K_t i$$

is written below the block and represents the connection between motor current and produced torque. This equation allows the electrical and mechanical subsystems to be linked together. Ultimately, this block transforms the input voltage into a physically meaningful quantity—torque—that drives the drivetrain.

The next block represents the **disturbance torque**. Physically, this block captures forces arising from tire–ground interaction, drivetrain losses, and bearing and gear friction. All of these forces act as disturbances that oppose motion and slow down the vehicle. Callum measured these effects by comparing free-spinning operation, where disturbance torque is minimal, to on-ground operation, where rolling resistance (the primary source of loss) is present. The disturbance torque is added to the motor torque according to:

$$T = T_u + T_d$$


Since disturbances physically oppose torque, their inclusion alters system acceleration and steady-state velocity. This explains real-world differences between ideal and actual performance and highlights why disturbance torque must be included in the block diagram. The car experiences both motor torque and resistive torque, and it is the net torque that accelerates the system. This directly implements the equation:


$$M_{eq}\dot{v} = T$$


The **mechanical system block** represents the combined dynamics of the motor, gear train, wheels, and car mass. This block compresses multiple rotating bodies into a single equivalent inertia, $$M_{eq}$$. This simplification comes directly from Jason’s derivation:


$$M_{eq} = \frac{J_w + m r^2 + i_g^2 J_e}{r^2}$$


This formulation allows the car to be modeled using a single differential equation:


$$\dot{v} = \frac{T}{M_{eq}}$$


which describes how applied torque produces forward acceleration and how inertia resists changes in speed. In the original ODE derivation, disturbance torque was neglected for simplicity, but it has been explicitly added here in the block diagram to better reflect real-world behavior.

Finally, the output of the block diagram is the **angular velocity**, $$\omega$$. This corresponds to the angular velocity of the wheels and is related to the linear velocity by:


$$\omega = \frac{v}{r}$$


This output is directly measurable and serves as the quantity used later for transfer function development and state-space comparison.

Although block diagrams provide an accurate representation for a simplified RC car model, several limitations should be acknowledged. First, the motor dynamics are reduced to the single relationship $$T_u = K_t i$$, meaning that voltage saturation, motor inductance, back-EMF, and additional resistance effects are omitted. While some of these effects appear in the full electrical ODE, they were intentionally excluded here to maintain a simple open-loop model. Second, the mechanical system uses a single equivalent inertia $$M_{eq}$$, which assumes rigid, lossless drivetrain components. In reality, RC cars experience internal friction that is not accounted for. Nonlinear effects such as Coulomb friction, speed-dependent motor torque, and aerodynamic drag are also neglected. Finally, the disturbance torque is modeled as a simple additive term rather than as a function of velocity or surface conditions. While these assumptions are reasonable for this analysis, they limit the model’s predictive accuracy, particularly at higher speeds where these effects become more significant.

