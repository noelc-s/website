---
display_to_feed: false
layout:     post
title:      "Nonlinear Model Predictive Control of a 3D Hopping Robot: Leveraging Lie Group Integrators for Dynamically Stable Behaviors"
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Nonlinear full-model MPC for a 3D hopping robot.

## Abstract
Achieving stable hopping has been a hallmark
challenge in the field of dynamic legged locomotion. Controlled
hopping is notably difficult due to extended periods of un-
deractuation combined with very short ground phases wherein
ground interactions must be modulated to regulate global state.
In this work, we explore the use of hybrid nonlinear model
predictive control paired with a low-level feedback controller
in a multi-rate hierarchy to achieve dynamically stable motions
on a 3D hopping robot. In order to demonstrate richer
behaviors on the manifold of rotations, both the planning and
feedback layers must be designed in a geometrically consistent
fashion; therefore, we develop the necessary tools to employ
Lie group integrators and appropriate feedback controllers.
We experimentally demonstrate stable 3D hopping, as well as
trajectory tracking and flipping in simulation.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/papers/HopperMPC.pdf" frameborder="0" allowfullscreen></iframe>
