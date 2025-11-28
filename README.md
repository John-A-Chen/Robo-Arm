```markdown
# Robo-Arm  
A lightweight, actuator-efficient robotic arm inspired by research-grade robotic mechanisms.  
This repository documents the development of the arm across **Generation 1 → Generation 2**, focusing on mechanical optimisation, linkage design, and SolidWorks validation.

---

## Overview  
Robo-Arm is a compact, low-cost robotic arm prototype. The design draws on ideas from:

**Al-Fahaam, Davis & Nefti-Meziani (2020)**  
*Design and Control of a Multi-Material Soft Robotic Arm With Embedded Fabric Sensors*  
https://www.mdpi.com/1424-8220/20/15/4174

I reverse-engineered aspects of the paper’s geometry—not the soft robotic materials—to understand how motion can be made more efficient through **mechanical advantage**, **distributed motion**, and **linkage ratios**.  
The goal was to replicate the efficiency principles using rigid 3D-printed parts and hobby-grade actuators.

---

## Project Goals  
- Develop an actuator-efficient robotic arm using simple, accessible components  
- Improve performance by optimising a **four-bar linkage**  
- Iterate from Gen 1 to Gen 2 with measurable improvements in range of motion  
- Use SolidWorks simulation to validate design decisions  
- Keep the design open-source and easy to replicate  

---

## Generations

### Generation 1  
The baseline prototype.

**Characteristics:**  
- Unoptimised four-bar linkage  
- Limited range of motion (especially at extremes)  
- High torque load on the main actuator  
- Some binding and awkward linkage angles  
- Served mainly as a functional proof of concept  

### Generation 2  
A significantly improved design informed by SolidWorks analysis.

**Key Improvements:**  
- **Optimised four-bar linkage** (better ratios + reduced binding)  
- Smoother and larger range of motion  
- Improved actuator efficiency  
- Reduced structural flex and backlash  
- Cleaner and more compact geometry  

---

## Research Influence  
Key ideas adapted from the Sensors paper include:  
- Distributing motion across multiple joints instead of relying on one actuator  
- Using geometry to reduce torque requirements  
- Lightweight structural design to reduce inertia  
- Kinematic reasoning for workspace prediction  

These concepts were reverse-engineered and applied to a rigid linkage system to explore whether similar efficiency gains could be achieved without soft actuators.

---

## CAD + Simulation  
All parts were designed and refined in SolidWorks.

**Engineering steps included:**  
- Four-bar mechanism optimisation  
- Motion studies + range-of-motion analysis  
- Interference checks  
- Evaluating torque requirements  
- Iterative prototyping  

Planned additions:  
- STEP files  
- Annotated engineering drawings  
- Assembly instructions  
- Photos of prototypes  

---

## ROS / ROS2?  
I am still uncertain whether ROS or ROS2 is necessary for a small arm like this.  
While ROS would allow:  
- higher-level planning  
- simulation  
- sensor fusion  
- modular control  

…it may also be overkill for:  
- a small number of DOFs  
- simple kinematic paths  
- microcontroller-level control loops  

For now, the project is hardware-focused, and ROS integration is a “maybe later” experiment.

---

## Repository Structure  
```

/cad            SolidWorks source files
/stl            STL exports for printing
/docs           Notes and references
/src            (future) control firmware
README.md       Documentation

```

---

## Why This Project  
This project shows how mechanical optimisation and thoughtful geometry can dramatically improve actuator performance, even with inexpensive hardware. Robotics is fun because it merges design, mechanics, simulation and experimentation—and iterating from Gen 1 to Gen 2 demonstrates real engineering progress.

---

## Reference  
Al-Fahaam, H., Davis, S., & Nefti-Meziani, S. (2020). *Design and Control of a Multi-Material Soft Robotic Arm With Embedded Fabric Sensors.* Sensors, 20(15), 4174. https://www.mdpi.com/1424-8220/20/15/4174
```
