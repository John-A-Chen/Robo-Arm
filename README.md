Robo-Arm

A lightweight, actuator-efficient robotic arm inspired by research-grade biomimetic mechanisms.
This repository documents the full development process—from Generation 1 to Generation 2—including design decisions, SolidWorks optimisation, manufacturing considerations, and validation.

Overview

Robo-Arm is a compact, low-cost robotic arm prototype designed for education, rapid prototyping and small-scale manipulation tasks. The project was based on concepts from Sensors (MDPI):
“Design and Control of a Multi-Material Soft Robotic Arm With Embedded Fabric Sensors” (Al-Fahaam et al., 2020)
https://www.mdpi.com/1424-8220/20/15/4174

I reverse-engineered key features of the paper’s mechanical layout—not the soft robotic actuation but the geometric approach to motion efficiency, moment distribution, and space-constrained linkage behaviour. The project’s aim was to explore how similar performance principles could be replicated with rigid-body mechanisms and hobby-grade actuators.

Project Goals

Develop an actuator-efficient robotic arm using accessible materials and 3D printing.

Explore how four-bar linkages and passive geometry can amplify servo output while reducing torque load.

Iterate from Generation 1 to Generation 2 with improved range of motion and stability.

Validate design choices through SolidWorks simulation and physical prototyping.

Document engineering decisions for open-source reproducibility.

Generations
Generation 1

Generation 1 served as the baseline prototype.
Key characteristics:

Initial four-bar linkage (unoptimised).

Basic servo placement.

Limited range of motion, especially near extreme angles.

Good proof-of-concept but inefficient torque distribution.

Identified weak points in joint spacing, linkage ratios and servo overloading.

Generation 2

Generation 2 is a significant refinement, using engineering insights and simulation results.
Improvements include:

Optimised four-bar linkage, redesigned using SolidWorks Motion Studies.

Greater usable range of motion.

Reduced binding and dead-zones in the linkage.

Improved actuator efficiency through better force transmission geometry.

Cleaner cable routing and structural redesign.

More rigid structure → less unwanted flex and backlash.

Research Basis

Although the MDPI paper focuses on soft robotics, several core ideas were adapted:

From the paper I adopted:

The concept of distributing deformation/motion across multiple joints instead of relying on a single actuator to do all the work.

The insight that geometry can do work for you—proper linkage shape and length ratios can significantly reduce actuator strain.

The use of lightweight limb segments to minimise inertia and reduce required torque.

Forward and inverse kinematic constraints for workspace mapping.

By reverse-engineering the paper’s geometry and applying it to rigid mechanisms, this project explores whether inexpensive actuators can achieve higher performance through mechanical advantage rather than brute force.

CAD, Simulation and Analysis

All mechanical components were designed and iterated in SolidWorks.
Key workflows include:

SolidWorks four-bar linkage optimisation.

Range-of-motion analysis.

Interference checks.

Torque requirement estimation.

Motion study animation and kinematic validation.

Future releases may include:

STEP files

Fully annotated engineering drawings

Printed prototype photos

Control firmware and microcontroller integration

Repository Structure
/cad            – SolidWorks files for each generation  
/stl            – Exported STL files for 3D printing  
/docs           – Notes, sketches, and reference images  
/src            – (future) microcontroller code for actuation  
README.md       – Project documentation  

Why This Matters

Robotics is cool because it sits at the intersection of design, mechanics, control theory, and creativity.
This project aims to show that:

Good engineering doesn’t require expensive parts

Mechanical optimisation can outperform raw motor power

Iterative design leads to genuinely better robotics performance

Anyone can build research-grade mechanisms with the right approach

Future Work

Add sensors for closed-loop control

Implement inverse kinematics for trajectory planning

Experiment with tendon-driven actuation

Expand DOFs with additional linkages

Integrate ROS2 control pipeline

Further optimise structure for strength-to-weight ratio

Reference

Al-Fahaam, H., Davis, S., Nefti-Meziani, S. (2020). Design and Control of a Multi-Material Soft Robotic Arm With Embedded Fabric Sensors. Sensors, 20(15), 4174. https://www.mdpi.com/1424-8220/20/15/4174
