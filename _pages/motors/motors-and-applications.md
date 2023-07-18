---
title: Introduction to Motors & Power Generation
subtitle: A basic intro to motors and power generation, why they're useful, and what they can do for the world.
description: An open-source knowledge center on motor design, control, and testing for electric vehicles and robotics.
featured_image: /images/social.jpg
---

### Introduction

If you made it this far, you likely already know that a motor spins. And honestly, that's a pretty good start. Generally, this notebook starts with some familiarity of motors, but doesn't require more than that. We suggest you read the [concept map](/resources/motor_concept_map.pdf) that we generated to give you a better idea.

> A motor is an electro-mechanical transducer, it converts electrical energy into mechanical energy, and therefor is also capable of converting mechanical energy into electrical energy. It's magical of course, but we can explain that magic with physics. That's what we'll do here.

We promised our focus would be to be practical. So let's take a look at the [United Nations Sustinable Development Goals (SDGs)](https://sdgs.un.org/goals). Goal 7 is about **Affordable Clean Energy,** Goal 9 is about **Industry, Innovation, and Infrastructure,** Goal 12 and 13 relate to **Responsible Consumption and Production, and Climate Action,** all of these and more relate to motors. Motors are required to generate power, they will be vital to the transition to clean energy, so studying their design to develop more efficient machines is critical to the future. Understanding them, can help us understand different ways to build a better world. We'll focus a lot on motor's applications to the UN SDGs in this notebook by describing specific projects.

<figure>
<img src="/images/social.jpg" alt="Trulli" style="width:100%">
<figcaption align = "center"><b>Fig.1 - This is the power unit from the first version of the MIT EVT's hydrogen motorcycle, it uses (2x) electric motors to drive the main output shaft.</b></figcaption>
</figure>

<br>

Motors are all around us, and not only is studying them both useful and practical, but incredibly interesting because of the complexity of the system. Designing motors requires and understanding of electromagnetics, but also materials science, and mechanical design—that too at a very detailed level. Designing of motor control requires an understanding of controls of course, but also sensing, electrical design, power systems, discrete-time microcontroller programming, and signal processing. Motors and motor control span so many aspects of sicence an engineering that learning about it allows an engineering to become well-versed in many skills at the same time while also remaining incredibly focused on the design of a single system. It's very unique in that way. That why more people should study motors, but we're pretty biased.

### A Technical Overview

There's a really good book on electric motors and motor control, it's where most of us started, and it's freely avaliable online: [Electric Motor Control by Sang Hoon Kim](https://www.sciencedirect.com/book/9780128121382/electric-motor-control). We'll borrow from some of his work as we build a story around motors. 

<figure>
<img src="kim_chart.png" alt="Trulli" style="width:100%">
<figcaption align = "center"><b>Fig.2 - Chart depicting the different kinds of motors from Sang Hoon Kim's Electric Motor Control, Chapter 1.</b></figcaption>
</figure>

<br>

The book starts by describing just how many types of motors exist. And there are *many kinds* of electric motors these days. This is by nature of the number of applications for these systems. There are many systems that use motors, many have different requirements, and this results in many different types of motors as each type is optimized for different things. 

Motors can be powered by [AC power, or DC power](https://www.youtube.com/watch?v=Wm75XgbqHBY). Some motors can be directly run, others require a motor controller to control them. All of this depends on their design. The most common motors are induction motors, the cheapest motors are brushed ones. We'll go into detail in both brushed and brushless systems and describe their design and their control. Know there are more types, and after you master these types, understanding the rest will be easier.

In this notebook, we will **focus on the design and analysis of DC motor control systems both brushed and brushless.** AC systems will not be considered for now, but we might add them later. Honestly, we don't know much about them. 

### Applications

The following includes some example applications of motors pulled from things we have worked on previously. But there are many more, and we'll spread examples out over the entire learning process **and include many examples that relate directly to the UN SDGs.** 

{% include post-components/gallery.html
	columns = 1
	full_width = true
	images = "robot.JPG,lathe.jpeg,bike.jpeg,kart.jpeg
	"
%}

The slideshow above contains just a few ones to start with.

1. The [MIT Cheetah 3 Robot](https://news.mit.edu/2018/blind-cheetah-robot-climb-stairs-obstacles-disaster-zones-0705) uses [brushless motors as actuators](https://fab.cba.mit.edu/classes/865.18/motion/papers/mit-cheetah-actuator.pdf) to run, and jump.
2. This lathe that we built for the MIT 2.72 Machine Design class uses a [CIM motor from FRC robots](https://motors.vex.com/vexpro-motors/cim-motor) to power its spindle.
3. This Ducati 750ss motorcycle uses a brushed electric motor to [start its engine](https://www.youtube.com/watch?v=7eN1gxH6lE4).
4. This go-kart uses an electric motor to drive around, and also charges its batteries when slowing down using [regenerative braking](https://auto.howstuffworks.com/auto-parts/brakes/brake-types/regenerative-braking.htm), we'll learn more about this kart later in the notebook!

Other systems such as Nuclear Power Plants, Hydro-electric Dams, and more use motors to generate power as well. Generally, the process of power generation uses *something* to [turn a big turbine](https://www.youtube.com/watch?v=20Vb6hlLQSg), and this turbine turns a motor which generates electric power. We'll study that power generation process as well. 

### Magnets and Materials

Motors work on the principals of electro-magnetics. So the physics that make them work, and the limitations associated with those physics come from understanding magnetics. Here are two great intro videos. We're talking about special relativity, materials, and so much more. We'll cover a lot of this but initial understanding is super helpful. 

*We apologize for the links while we get video embedding to work... HTML is hard OK.*

1. [Magnets, How do they Work?](https://www.youtube.com/watch?v=hFAOXdXZ5TM)
2. [Special Relativity, Magnets, Electricity](https://www.youtube.com/watch?v=1TKSfAkWWN0)

### Helpful Content Going In

Like we described in the concept map, we're going to have to assume some amount of knowledge. Otherwise this website would take up the rest of the internet. But we'll try not to assume a lot, and we'll try to link resources that will help you learn the basics. Here's a link to a bunch of stuff that will help along the way, a lot is repeated in the resources page. We'll try to tell you when we're assuming knowledge, we will try not to assume too much.

| Physics E&M at the high-school level | [Intro E&M](https://ocw.mit.edu/courses/8-02-physics-ii-electricity-and-magnetism-spring-2007/) | [a good physics book](https://www.thriftbooks.com/w/thinking-physics-understandable-practical-reality_lewis-carroll-epstein/250662/item/11836090/?utm_source=google&utm_medium=cpc&utm_campaign=pmax_new_books&utm_adgroup=&utm_term=&utm_content=&gclid=EAIaIQobChMIpOLcpPeYgAMVQ_DjBx0B2AkZEAQYASABEgLNFfD_BwE#idiq=11836090&edition=2984862) | [Circuit Analysis](https://ocw.mit.edu/courses/6-002-circuits-and-electronics-spring-2007/) |

| Soldering, Wiring, and other Lab Skills | [MIT PCB Design Population/Debugging](https://pcb.mit.edu/lectures/lab_05/) | [Basic Soldering](https://pcb.mit.edu/lectures/lab_03/) | [Multimeter /Scope /Debugging](https://pcb.mit.edu/lectures/lecture_05/) |

##### For Higher-Level Stuff like Motor Controller Design

| Power Electronics / Circuit Design Course | [Intro Electronics](https://www.edx.org/course/circuits-and-electronics-1-basic-circuit-analysi-2?irclickid=SV7Tbk2nFxyPUdOTffz%3AQSDvUkFzbKwMmxd9xs0&utm_source=affiliate&utm_medium=Class%20Central&utm_campaign=Harvard%27s%20Computer%20Science%20for%20Python%20Programming_&utm_content=TEXT_LINK&irgwc=1) | [Practical Electronics for Inventors](http://instrumentacion.qi.fcen.uba.ar/libro/Scherz.pdf) | [Power Electronics](https://ocw.mit.edu/courses/6-334-power-electronics-spring-2007/) |

| PCB Design | [The Art + Science of PCB Design](https://pcb.mit.edu) |

| ST Microcontroller Programming (STM32) | [Link to their online knowledge base](https://www.st.com/content/st_com/en/support/learning/stm32-education.html) |

Most of the other stuff, we will cover. **We'll come out and tell you now that basic circuits and E&M we won't cover on this site. Everything else, even the advanced resources we linked will be covered in some form.** The resources page will have more links to things that you can use to learn, but we reccomend an understanding of E&M going into this notebook.

**Ready? Yea? Let's get started!**