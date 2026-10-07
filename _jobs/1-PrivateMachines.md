---
layout: project
title: Private Machines
description: High-Security Servers
technologies: [Fusion, ANSYS]
image: /assets/images/PrivateMachines.png
---
My first job out of college was as the sole Mechanical Engineer at a small start-up specializing in high security servers. 

Network security is hardly the usual domain of MechEs, and indeed the majority of the team was focused on software, but the company's unique Enforcer Servers are designed to meet the strictest level of data security (NIST FIPS 140-3 Level 4) which requires being tamper-proof physically as well as digitally. This involved putting all of the important PCBs in a sealed box, inside of another sealed box, which creates an imposing heat transfer problem: how do you cool the cpu when there are at least 2 thermal interfaces and 4 inches of metal between it and the outside air?

The solution I inhereted was essentially to just accept an 80C operating temperature for the cpu at max power. Technically below the maximum operating temperature but clearly not ideal. Some quick math suggested that the maximum temperature difference between the cpu and the outermost surface should be about 18C. We were getting about 45.

This is indicative of the mechanical design writ large.

Trying to rationalize the design of the many machined and sheet metal components taught me a great deal about Design for Manufacturability (DFM), heat transfer and contact mechanics, CAD best practice, how to run and evaluate FEA and CFD simulations, as well as general engineering decision-making, and along the way I was able to almost halve the number of screws we used in our server chassis. But unfortunately I was let go before I could truly reap the fruits of my labor.

So why was I fired?

The short answer is that I wasn't actually told why. What little feedback I was given (all post-termination) points to the root cause being simply "personality conflict." So, to be perfectly clear about my professional personality: I am not a loose cannon nor am I incapable of formality or humility. I know well what I know and what I don't, and I know how I work and learn best. If I was seen as insubordinate it was because I do not mutely kowtow to seniority, though I always keep my disagreements respectful. Quite frankly, the fault was with the CEO -- I was not the first engineer to be dropped unceremoniously from Private Machines and I suspect I will not be the last.
