---
layout: project
title: Product Design
description: One might expect a MechE to have more experience
technologies: [AutoDesk Fusion360]
image: /assets/images/autodeskLogo.png
---
The course project of *MAE 2250 Introduction to Mechanical Deisgn* was a group assignment in which we were tasked with designing and prototyping some product -- it was left deliberately vague. While I did learn a great deal of CAD and general design best practice from this assignment, in my mind it will always be principally associated with the truly abysmal group work dynamic I had to navigate. Suffice to say that I will be using the first-person singular pronouns in describing the product development process.

I've been playing the trombone at various degrees of rigor since elementary school, and one of the fundamental skills of the instrument that takes a long time to develop is slide control: it is very easy to put the slide in the wrong place and end up playing something very out of tune. So I designed a device that would attach onto the instrument and provide tactile feedback regarding the slide position. The main design challenges were

1. **Adjustability:** every trombone is different, so the feedback mechanism needs to be easily adjusted, ideally while holding the horn, but be resistant to accidental movement.
2. **Stability:** there isn't very much area on or around the trombone to attach something the length of the slide, so a rigid, impermanent connection needs to be established using very few points of contact.
3. **Portability:** both for the sake of manufacturing and end user convenience, the device should be constructed out of smaller segments that can easily be connected to reach the roughly 30" final length.

Fortunately, from a mechanical perspective, these challenges were able to be addressed mostly independently with the design elements as follows

### Adjustible Bump
<img src="{{'/assets/images/CADtb1.png' | relative_url}}" alt="cross section of first mechanism" width="397" height="300">

The outer body is the rod that runs the length of the trombone slide. The pink body on the left is the bump that provides tactile feedback. A spring is inserted into the back of this body and compressed by the button on the right. The large walls on the interior of this button provide the friction to keep the bump in place during use, and the button can be pressed to allow the whole system to slide along the length of the rod.

### Fabric Strap
<img src="{{'/assets/images/CADtb2.png' | relative_url}}" alt="cross section of second mechanism" width="270" height="300">

A long fabric strap is secured around the rod on the left. The semi-circular indent on top interfaces with the inlet tube of the trombone and the strap is wrapped around it. By threading the strap around the pair of rods on the right it happens that the strap can be tightened from the free end but lock in place when pulled from the fixed end.

### Snap Fit
<img src="{{'/assets/images/CADtb3.png' | relative_url}}" alt="cross section of third mechanism" width="397" height="182">

The rod was separated into 3 segments that could be easily connected and disconnected with this snap-fit mechanism.
