---
layout: project
title: Math Research
description: N points on a sphere
technologies: [MATLAB]
image: /assets/images/bigFreaknShape.png
---
<script type="text/javascript" async
     src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

In freshman year, I accidentally came up with a math problem so hard it would remove the next two years of my free time: What are all the equilibrium distributions of \\(n\\) mutually repulsive points confined to a sphere? 

A full explanation of the problem along with all relevant code can be found on my [GitHub page](https://github.com/smostek/n-points-on-a-sphere).


### Problem Statement
Consider \\(n\\) points confined to a unit sphere with its center at \\(o\\) and let \\(C \\) be the set of position vectors associated with those \\(n\\) points. Each represents an electron and thus experiences a force described by Coulomb's Law:

$$\vec{F}_i=\sum_{\substack{k=1 \\ k\neq i}}^{n}\vec{F}_{ik} = \sum_{\substack{k=1 \\ k\neq i}}^{n} r_{ik}^{-3}\vec r_{ik}$$

Where \\(r_{ik}\\) is the magnitude of \\(\vec r_{ik}\\), and in general a vector without its hat is to be interpreted as its magnitude. Because the points are confined to the sphere, the radial component of each force vector \\(\vec F_i^R=\hat r_{io}\left(\hat r_{io}\cdot\vec F_i\right)\\) can be ignored. The goal is to find every equilibrium distribution, that is, every arrangement for which the tangential component \\(\vec F_i^{\perp} = \vec F_i-\vec F_i^R\\) of every point's force has zero magnitude. To that end, we define the "Cross Sum" (so named because it was initially formulated using a cross-product) as the average of the magnitudes of these tangential components:

$$ CS(C) = \frac{1}{n}\sum_{i=1}^n F_i^{\perp} $$

The challenge is now to create an algorithm that takes just a single value, \\(n\\), and returns every distribution \\(C\\) for which \\(CS(C)=0\\). Such distributions will be called "solutions."

### Minimization
This is a highly nonlinear problem: the effect of a combination of individual changes looks nothing like the combination of the individual effects of the same changes. For instance, near the beginning of this project I designed my own gradient descent algorithm to attempt to minimize the Cross Sum, but outside of a few niche applications it didn't work very well for this project as any gradient descent algorithm relies on the assumption that the objective function can be locally approximated as linear, which is not true in this case. Indeed, I have found that the literature surrounding the closely related Thomson Problem is in large part dedicated to the testing of novel minimization techniques on this particularly thorny system. I have, however, found success with a relatively simple technique: move all points simultaneously a small step in the direction of their force. It is more complicated than that of course -- how small is "small" exactly -- but that is the general method and it has allowed me to confidently identify solutions up to about \\(n=12\\).

### Initial Positions
Any optimization method needs a starting point, or in this case many starting points as there will be several equilibrium distributions for a given value of \\(n\\). With how finicky the minimization process can be, finding all of the shapes requires, in a sense, knowning what all of the distributions will be ahead of time, or at least getting close enough that the minimizer can actually succeed. For a long time, the initial position generation relied on the observation that solutions tend to have points lie in parallel bands. The icosahedron below, for instance, can be oriented so as to have the structure (1 5 5' 1), that is a north pole above a pentagon above a rotated pentagon above a south pole.

<img src="{{'/assets/images/Icosahedron.png' | relative_url}}" alt="animation of simulation of 3D rolling squared" width="317" height="328">

Since this naming convention can also work in reverse, my method of generating intial positions amounted to identifying all of the unique and valid names for a given value of \\(n\\). What I ultimately realized, however, is that while this parallel polygon framework is valid, it is merely indicative of a deeper truth: symmetry. 

It is difficult to discuss the implications of incorporating symmetry group theory into this project at a lay level, as the vocabulary gets technical quickly and difficult to explain in text. Suffice to say that the function I wrote just to identify a ploygon's symmetry from the coordinates of its vertices runs nearly 400 lines of code long.

The mesmerizing animation below is an attempt to help communicate the difficulty of this problem. All of the yellow points are reflections of the blue control point such that the distribution always has \\(T_d\\) symmetry. The black lines represent the potential energy contour experienced by the blue point; the goal is for the blue point to reach the local minimum, but every time it moves the surface changes.

<img src="{{'/assets/images/contourAnimation.gif' | relative_url}}" alt="animation of simulation of 3D rolling squared" width="325" height="305">
