---
layout: project
title: Dynamics
description: Physics not for the faint of heart
technologies: [MATLAB]
image: /assets/images/Mathsplosion.png
---
Dynamics is the physics of motion, a means of turning the complexity of the trajectories of rigid bodies into math. The trouble is that very few mechanical systems correspond to analytically solvable systems of differential equations. One way to deal with this is to simulate the solutions, which was the focus of *MAE 4730 Intermediate Dynamcis*. The other, more rigorous way is to manipulate the equations into forms that can be approximated as linear systems within a particular range of motion, which was the focus of *41522 Advanced Dynamics and Vibrations* (taken abroad at The Technical University of Denmark).

### Simulation
<img src="{{'/assets/images/RollingAnimation.gif' | relative_url}}" alt="animation of simulation of 3D rolling squared" width="270" height="275">

The most technically impressive simulation I've ever created was for my final report for MAE 4730 and involved a ball rolling within a hemispherical shell that itself could roll. It is probably difficult to internalize why this should be so complicated, but it required over 80 lines of densely mathematical code just to calculate the equations of motion governing the 18 independent variables of the system, and that's before actually running the simulation and animating the result.

Another simulation of which I'm particularly proud is a model of a satellite pitch control system using reaction wheels. This was actually part of my final project for *MAE 3260 System Dynamics* as the main focus was not the simulation itself but rather how the linear control law for the reaction wheels interacted with the nonlinear physics of the equations of motion of the satellite's angular momentum.

<img src="{{'/assets/images/SatelliteAnimation.gif' | relative_url}}" alt="animation of simulation of reaction wheel satellite" width="222" height="275">

I've made a [repository](https://github.com/smostek/Dynamics) on GitHub for these and other simulation scripts if you are interested in running them for yourself.

### Linearization
Consider the familiar motion of a rigid pendulum: though intuitive and reliably modeled as a simple harmonic oscillator, an accurate model of its full range of motion is nonlinear and, if drag is included, not explicitly solvable. Now imagine vibrating the pendulum's pivot point up and down rapidly. Why? Because, unintuitively, this causes the pendulum to become stable pointing straight up. Understanding how and why that kind of strange behavior, especially when caused by vibrations, is at the heart of nonlinear dynamics.

For my final project of my nonlinear dynamics class, I analyzed the vibration response of a tensioned beam with a point mass in its middle. I'd recommend just looking at page 6 of [the report]({{ "/assets/41522_FinalReport.pdf" | relative_url }}) if you want to get a sense of how daunting the math gets.
