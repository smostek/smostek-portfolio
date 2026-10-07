---
layout: project
title: Additive Manufacturing
description: metal AM research
technologies: [MATLAB]
image: /assets/images/LPBF_FEM.png
---
<script type="text/javascript" async
     src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>
In the summer leading up to my final semester, I joined a additive manufacturing research group at Cornell, the Laboratory for Advanced Materials and Manufacturing. I was left very much at arm's length for the whole summer, given only vague directions about what exactly I was supposed to research with neither the PI nor the graduate student nominally advising me offering much direction or oversight. So, when over the first few weeks of introducing myself to the subject I noticed a strange oversight in the reference textbook I had found, there seemed little reason not to dig in. 

In Laser Powder Bed Fusion (LPBF), the two most immediate parameters that can be adjusted are the laser power \\(P\\) and speed \\(v\\). Unsurprisingly, if the laser slows down or is fed more power then the powder will melt more completely, so the ratio of these quantities \\(P/v\\) is pretty important to any discussion of the many particular situations in which the LPBF process needs to be fine-tuned for optimal part quality. What was bothering me is that what everything I was reading on overhang slag, surface roughness, keyholing, plumage, balling, etc. was simply referring to the variability of the output with respect to changes in \\(P\\) or \\(v\\) individually while ignoring an important question: what if you change both and keep \\(P/v\\) constant?

So I did what I do best: I grabbed a notebook and a pencil and started writing equations. I was expecting based on what I was reading that any formula for temperature that came out of the highly simplified moel I was developing should be able to be expressed in terms of the ratio \\(P/v\\), thus explaining why the specific values of the variables didn't seem to matter, but that wasn't at all the case; doubling the laser power would increase the powder temperature far more than doubling the speed would decrease it. The same amount of energy might be deposited, but it would be distributed very differently.

I would soon enough learn that, of course, I was not the first person to think about this. Rosenthal solved a very similar system to mine back in the 1940s in the context of welding and his solution gets used occasionally in LPBF literature to this day. 40 years later, another paper expanded on Rosenthal's work by solving precisely the same system as I had devised, though in a very different way. Meanwhile, there were a few modern papers cautioning against the overuse of Energy Density in analysis given the difference in output that can occur at equal values of \\(P/v\\).

What I did that was truly novel, and what I was tasked with drafting into a research paper over the following semester, was connect the temperature distribution that emerged from my model to the metallurgy of solidification. Crystal structure is very important to part quality in additive manufacturing, and crystal structure is determined by the temperature gradient and cooling rate at the transition from liquid to solid, which can be determined from the equations for temperature I determined. The main problem was data. In order to prove that my model had predictive value, it needed to be shown to match existing data, but with only a few hours a week to spare for the research, I wasn't able to farm enough data to draw any conclusions before graduation day hit.

### Variable Thermophysical Properties
One of the many subtleties overlooked by the simple model I designed is the fact that material properties, most significantly the thermal conductivity, change with temperature. In normal contexts this fact can be safely ignored, but in LPBF the temperature swings in the area around the laser are thousands of degrees. Incorporating this into the model introduces significant nonlinearities that make it impossible to solve analytically, though I'm still curious about this and the advanced math behind quasi-linear diffusion equations.

To get to the effects of variable conductivity more directly, I turned to Finite Element Modeling. Perhaps I may have gotten the answer slightly faster with a standard software package like Ansys, but instead I turned to MATLAB and its Partial Differential Equation Toolbox. This way I have full control over the nature of the equations and could much more easily process and visualize the data however I wanted. The header image for this page was created in MATLAB.
