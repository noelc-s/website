---
display_to_feed: true
layout:     post
title:      "Robust Agility via Learned Zero Dynamics Policies"
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Using optimal control and learned output tracking to stabilize a 3D hopping robot.

## Abstract
We study the design of robust and agile controllers
for hybrid underactuated systems. Our approach breaks down
the task of creating a stabilizing controller into: 1) learning a
mapping that is invariant under optimal control, and 2) driving
the actuated coordinates to the output of that mapping. This ap-
proach, termed Zero Dynamics Policies, exploits the structure of
underactuation by restricting the inputs of the target mapping
to the subset of degrees of freedom that cannot be directly
actuated, thereby achieving significant dimension reduction.
Furthermore, we retain the stability and constraint satisfaction
of optimal control while reducing the online computational
overhead. We prove that controllers of this type stabilize hybrid
underactuated systems and experimentally validate our ap-
proach on the 3D hopping platform, ARCHER. Over the course
of 3000 hops the proposed framework demonstrates robust
agility, maintaining stable hopping while rejecting disturbances
on rough terrain.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/papers/ZDPApplication.pdf" frameborder="0" allowfullscreen></iframe>
