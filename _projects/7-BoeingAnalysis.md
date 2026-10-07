---
layout: project
title: Engineering Ethics
description: MAE 4300 Project Writeup
technologies: [N/A]
image: /assets/images/boeing.png
---

On 29 October, 2018, Lion Air Flight 610, carried by a Boeing 737 Max 8, crashed off the coast of Java.

On 10 March 2019, Ethiopian Airlines Flight 302, also carried by a Boeing 737 Max 8, crashed within minutes of takeoff from Addis Ababa.

In the last 20 years, there have been 330 deaths on commercial airline flights in and around the US. These two Boeing crashes, which occured within 6 months of one another, resulted in 346 fatalities.

How do such tragic mistakes occur? As with most things resulting from human action, the answer is that a large effect was generated from the combined effect of myriad small decisions.

*This write-up and its placement on this website was an assignment for MAE 4300 Engineers and Society. I have chosen to leave it on the website as a record of how I analyze problems and of my commitment to thinking critically about systems both technical and political.*

#### History
In 2010, Airbus released the A320neo, delivering significant fuel efficiency benefits -- a benefit not only to the environment but also to airlines' fuel costs -- which consequently placed pressure on Boeing to deliver a competitve design. The result was the 737 Max.

Within aviation design, the general trend is for larger engines to be more efficient -- they require less pressure to generate the same amount of thrust force. The tradeoff of course, is that larger engines weigh more and create more drag. So as knowledge of aerodynamics and structural mechanics has grown, so too have airplane engines.

Separate from this engineering problem is an economic problem: Boeing's marketing team wanted to keep the company's customers loyal and guarantee a market for the new planes when they eventually reached production. So, they promised the updated 737 would not require any new pilot simulator training, and even went so far as to offer Southwest a million dollar rebate on each plane bought.

Here, then, is the needle Boeing engineers were tasked with threading: fit a larger engine onto an existing chassis without changing the plane's flight characteristics.

In order to fit the new engine onto the old wing, the engineers had to move it forward, which shifted the plane's balance and flight characteristics. Mission accomplished. But the engineers were clever: they could fix the problem with software. Borrowing an existing system from the military arm of the company, a pitch correction system called MCAS was added to the 737. 

To make a long story short, as development continued, Boeing consistently ignored red flags and even expanded the operational window of MCAS, with the ultimate effect being an enourmous single point of failure: should a plane's pitch sensor fail, its computer, thinking the plane was about to stall, would aggressively pitch the plane down. When this happened during takeoff, there was not enough time for pilots to correct the computer, leading to the two tragic crashes.

#### Systemic Failures
The question then remains, why was this long series of risky decisions not noticed and halted? Boeing's own management certainly cannot escape blame, as there were engineers and test pilots who raised concerns about the plane's safety but were ignored. But just as important is a trend for which it is much harder to find a scapegoat: deregulation. For a long time now, the prevailing attitude in Congress towards the federal bureaucracy has been a mix of a neoliberal disgust combined with a begrudging recognition of its necessity. The result was that the Federal Aviation Administration (among other regulatory agencies) has seen a steady decline in its funding, and thus has had to get creative with its resources. As its bandwidth decreased, the FAA relied more and more on delegation, a technique originally intended for superfluous design elements whereby Boeing employees would represent FAA interests.

This is how MCAS flew under the radar (pun not intended). The FAA delegated the certification of MCAS to Boeing, so never learned about the true scope of the system. This allowed Boeing to bury the design change and claim to airlines that that there were no new systems on which pilots needed to be trained.

The trouble is that when the root cause of a problem is not a single decision but rather the sum effect of a decades-long trend, a proper solution starts to appear politically daunting. Each of the major actors was acting rationally, if not cautiously, in response to the set of incentives presented by the system. As a point of comparison, Boeing's stagnation and ultimately deadly blundering is categorically indistinct from the series of blunders that led to the Great Recession a decade prior. In both cases, the frustrating truth is that while it is tempting to point fingers at the one who knocked the dominoes over, we cannot escape blame ourselves for empowering a system that spent decades lining those dominoes up.
