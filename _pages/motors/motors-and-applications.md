---
title: Introduction to Motors & Power Generation
subtitle: A basic intro to motors and power generation, why they're useful, and what they can do for the world.
description: An open-source knowledge center on motor design, control, and testing for electric vehicles and robotics.
featured_image: /images/social.jpg
---

### Introduction

If you made it this far, you likely already know that a motor spins. And honestly, that's a pretty good start. Generally, this notebook starts with some familiarity of motors, but doesn't require more than that. We suggest you read the [concept map](/resources/motor_concept_map.pdf) that we generated to give you a better idea.

> A motor is an electro-mechanical transducer, it converts electrical energy into mechanical energy, and therefor is also capable of converting mechanical energy into electrical energy. It's magical of course, but we can explain that magic with physics. That's what we'll do here.

We promised our focus would be to be practical. So let's take a look at the [United Nations Sustinable Development Goals (SDGs)](https://sdgs.un.org/goals). Goal 7 is about **Affordable Clean Energy,** Goal 9 is about **Industry, Innovation, and Infrastructure,** Goal 12 and 13 relate to **Responsible Consumption and Production, and Climate Action,** all of these and more relate to motors. Motors are required to generate power, they will be vital to the transition to clean energy, so studying their design to develop more efficient machines is critical to the future. Understanding them, can help us understand different ways to build a better world. We'll focus a lot on motor's applications to the UN SDGs in this notebook by describing specific project.

<figure>
<img src="/images/social.jpg" alt="Trulli" style="width:100%">
<figcaption align = "center"><b>Fig.1 - This is the power unit from the first version of the MIT EVT's hydrogen motorcycle, it uses (2x) electric motors to drive the main output shaft.</b></figcaption>
</figure>

### A Technical Overview

There's a really good book on electric motors and motor control, it's where most of us started, and it's freely avaliable online: [Electric Motor Control by Sang Hoon Kim](https://www.sciencedirect.com/book/9780128121382/electric-motor-control). We'll borrow from some of his work as we build a story around motors. 

<figure>
<img src="kim_chart.png" alt="Trulli" style="width:100%">
<figcaption align = "center"><b>Fig.2 - Chart depicting the different kinds of motors from Sang Hoon Kim's Electric Motor Control, Chapter 1.</b></figcaption>
</figure>

<br>

There are *many kinds* of electric motors these days. And this is by nature of the number of applications for these systems. There are many systems that use motors, many have different requirements, and this results in many different types of motors as each type is optimized for different things. 

{% include post-components/gallery.html
	columns = 1
	full_width = true
	images = "robot.jpg,lathe.jpeg,bike.jpeg,kart.jpeg
	"
%}

1. The [MIT Cheetah 3 Robot](https://news.mit.edu/2018/blind-cheetah-robot-climb-stairs-obstacles-disaster-zones-0705) uses [brushless motors as actuators](https://fab.cba.mit.edu/classes/865.18/motion/papers/mit-cheetah-actuator.pdf) to run, and jump.
2. This lathe that we built for the MIT 2.72 Machine Design class uses a [CIM motor from FRC robots](https://motors.vex.com/vexpro-motors/cim-motor) to power its spindle.
3. This Ducati 750ss motorcycle uses a brushed electric motor to [start its engine](https://www.youtube.com/watch?v=7eN1gxH6lE4).
4. This go-kart uses an electric motor to drive around, and also charges its batteries when slowing down using [regenerative braking](https://auto.howstuffworks.com/auto-parts/brakes/brake-types/regenerative-braking.htm), we'll learn more about this kart later in the notebook!

Other systems such as Nuclear Power Plans, Hydro-electric Dams, and more use motors to generate power as well. Generally, the process of power generation uses *something* to turn a big turbine, and this turbine turns a motor which generates electric power. We'll study that power generation process as well. 

### Magnets and Materials

Motors work on the principals of electro-magnetics. So the physics that make them work, and the limitations associated with those physics come from understanding magnetics. Here are two great intro videos. We're talking about special relativity, materials, and so much more. We'll cover a lot of this but initial understanding is super helpful. 

{% include post-components/video.html
	url = "https://www.youtube.com/watch?v=hFAOXdXZ5TM"
	full_width = true
%}

{% include post-components/video.html
	url = "https://www.youtube.com/watch?v=1TKSfAkWWN0"
	full_width = true
%}