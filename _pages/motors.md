---
title: Motors
subtitle: Learn about motors, motor design, motor control, and testing! 
description: An open-source knowledge center on motor design, control, and testing for electric vehicles and robotics.
featured_image: /images/social.jpg
---

## The Basics

[A 'Learning Map' for Motors](/resources/motor_concept_map.pdf)

[Introduction to this Notebook](/intro)

[Introduction to Motors, and their Applications](/motors-and-applications)

[List of Recommended Software](/software)

[List of Recommended Resources](/links)

## Brushed DC Motors Selection + Control

### Fundementals of DC Brushed Motors + Control

[Brushed DC Motors—an Overview]()
- Brushed Motor Physics Equation Derived, Torque Speed Curve, Etc 
- https://www.youtube.com/watch?v=CWulQ1ZSE3c
- https://www.youtube.com/watch?v=pxtRlKs0pAg

[Pulse-Width-Modulation + its Applications to Motor Control, the H-Bridge]()

[Current (Torque) Control of a Brushed DC Motor]()
- Start w/ a simple DC motor that can do current control (NO GATE DRIVE CHIP, just use an H-bridge controller and current sensor, modular)

[Drive Control Bandwith Analysis]()
- How do you know if your motor drive and system is "good enough" for your application

### Designing Commercial-Off-the-Shelf Brushed Motor Systems (COTS) --> INTEGRATE THIS WITH BRUSHLESS COTS SYSTEMS AS WELL!!!

**Like just "designing COTS motor systems"**

[Selecting a Brushed Motor for an Application]()
- gear ratios, torque speed curves, etc 

[Selecting a Motor Controller for an Application + Interfacing With It]()
- when should you NOT design a motor controller, when can you use something else for a motor controller 

[Encoders + Encoder Selection]()

[Using Power Converters as Motor Controllers (The Prius Power Stage Case Study)]()

[Power Analysis, Programming Power Curves (Go-Kart Throttle Response Case Study)]()

### Building your Own Motor Controller

[Design of Brushed Motor Controllers]()

- general layout
- fet selection
- current sensing 
- power stage and protection
- regenerative braking... etc etc 
- inputs / outputs 

[Sensing Precision, PWM Switching Frequency, and Effects on Control]()

- Design of Brushed Motor Inverters (fet selection, current sensing, PWM clock speeds)
- Regenerative Braking in Brushed Systems (without a gate drive chip)
- Introduction to Gate Drive Chips + Why you might want to Use them

## Brushless DC Motors Selection + Control

- Brushless DC Motors overview, three-phase, PEAK POWER POINT AND SATURATION (T/S curves)
- Simple forms of brushless motor control
- Field-Oriented Control + Theory, torque control of three-phase motors (using a small BLDC and something like an O-Drive)
- SVM (space-vector modulation)
- Calibration routines, current sensing, encoders and state estimation for commutation 
- Designing an Inverter for three-phase brushless motor control w/ a Gate Drive chip 
- Designing an Inverter for three-phase brushless motor control with Discrete Gate Drivers + Current Sensing (circuitden.com/blog/11)
- Regenerative Braking in Brushless Systems 

## Higher Level Forms of Control! 

- Speed Control, Position Control
- Impedance Control! (fun applications)
- Field Weakening Control for BLDC motors
- Stat Machines in Motor Control + Triggering Switches 

## Power Generation

## Motor Design + Testing

[Introduction to Motor Design](/motor_design_1)

- Poles Slots
- Brush wear for brushed systems
- Bearing selection + design
- Ansys Motor CAD 
- Dyno systems
- efficiency maps, power maps 

Check out: https://keysan.me/ee564/ (for motor design)


**BORROW THINGS FROM 2.74 BUT RE-WRITE MOST OF IT!!!**

**WHY DO WE NOT NEED REGEN PROTECTION FOR A DYNO WITH TWO MOTORS??**

**HOW TO ESIMATE TORQUE SPEED CURVE FROM MAGNETIC SATURATION, PEAK POWER POINT, FREE SPEED b/c PPP =/ the Knee**


**DON't RE-WRITE THINGS THAt DON'T NEED RE-WRITING THE SAME WAY WE DID THE PCB CLASS**

**We will see, but all tutorials might be in STMCubeIDE not MBED and we'll explain why (optimization of code)**


# other resources 

https://rlib.redarm.in/post/winding-pattern/

https://www.electrical4u.com/armature-winding-pole-pitch-coil-span-commutator-pitch/

maybe this too? https://www.tutorialspoint.com/pitch-factor-or-coil-span-factor-in-alternator#:~:text=The%20coil%20span%2Dfactor%20or,also%20known%20as%20chording%20factor.

great video: https://www.youtube.com/watch?v=rTsRSTzeqaM

also good: https://www.youtube.com/watch?v=Tq5O7ma-xno

http://www.davidsonsales.com/public/pdfs/CoilPitch.pdf

