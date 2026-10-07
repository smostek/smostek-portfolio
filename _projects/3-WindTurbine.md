---
layout: project
title: Wind Turbine Design
description: MAE 4021 Final Project
technologies: [Ansys Fluent, MATLAB]
image: /assets/images/stockWindFarm.jpg
---
As part of the final project of *MAE 4021 Wind Power* we were given the geometry of a small wind turbine blade along with data on its performance as measured in a real wind tunnel. We were then tasked with simulating the blade's performance over the same set of operating conditions in Ansys to compare with the experimental data. Finally, we had to develop a program to design and test a better turbine blade design using mathematical models. One might imagine that the latter performance evaluation method would be less accurate, but through my novel modelling approach I achieved greater agreement with the experimental data than did the CFD.

My full report can be read [here]({{ "/assets/Wind_Power_Final_Project.pdf" | relative_url }})

### Ansys
I'm not going to pretend to understand the function of every setting and sub-setting within this leviathan of a program (the particular simulations we were tasked with for this assignment came with a tutorial), but I am pretty confident in my ability to learn the relevant controls for a given situation.


<img src="{{'/assets/images/FluentMainPage.png' | relative_url}}" alt="Ansys Fluent" width="750" height="500">

An important tool that I discovered during this assignment was the ability to parameterize steps within the CAD program. This was important as the pitch angle of the blade was a variable within the simulations, but changing this variable would require redoing several steps of geometry and meshing. By parameterizing the pitch angle I saved a lot of time and energy.

The results of the CFD simulations compared to the reference wind turbine data is shown:

<img src="{{'/assets/images/AnsysVsRefData.png' | relative_url}}" alt="Ansys data vs reference" width="750" height="500">

### Design
My mathematical methodology behind the blade design and testing software was as unique as it was effective. The details are tedious and subtle and can be found within the report, but the short version is this: there are two independent models that can combine to give algebraic expressions for the forces on the blade in terms of its geometry and operating conditions; one model can easily incorporate aerodynamic drag, the other cannot. The textbook we were using assumed no drag for the majority of its derivation before adding a correction term to all the equations and claiming that could account for the drag. I was able to identify a flaw in this argument and rederive the equations with drag included from the beginning. The resulting program was able to generate the following blade performance predictions:

<img src="{{'/assets/images/MatlabVsRefData.png' | relative_url}}" alt="my code vs reference" width="750" height="500">

As you can see, my simple code generated coefficient of power values in far greater agreement with the reference data than did the commercial CFD software.
