---
display_to_feed: false
layout:     post
title:      "Dynamically Feasible Path Planning in Cluttered Environments via Reachable Bézier Polytopes"
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Using Bezier reachable polytopes to perform nonconvex path planning.

## Abstract
The deployment of robotic systems in real world
environments requires the ability to quickly produce paths
through cluttered, non-convex spaces. These planned trajec-
tories must be both kinematically feasible (i.e., collision free)
and dynamically feasible (i.e., satisfy the underlying system
dynamics), necessitating a consideration of both the free space
and the dynamics of the robot in the path planning phase.
In this work, we explore the application of reachable Bézier
polytopes as an efficient tool for generating trajectories satisfy-
ing both kinematic and dynamic requirements. Furthermore,
we demonstrate that by offloading specific computation tasks
to the GPU, such an algorithm can meet tight real time
requirements. We propose a layered control architecture that
efficiently produces collision free and dynamically feasible paths
for nonlinear control systems, and demonstrate the framework
on the tasks of 3D hopping in a cluttered environment.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/papers/BezierPlanning.pdf" frameborder="0" allowfullscreen></iframe>
