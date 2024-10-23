---
display_to_feed: true
layout:     post
title:      "Planar Bipedal Locomotion with Nonlinear Model Predictive Control"
subtitle:   "Online Gait Generation using Whole-Body Dynamics"
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Full-model nonlinear MPC on a planar biped.

## Abstract
The ability to generate dynamic walking in real-
time for bipedal robots with input constraints and underactua-
tion has the potential to enable locomotion in dynamic, complex
and unstructured environments. Yet, the high-dimensional na-
ture of bipedal robots has limited the use of full-order rigid
body dynamics to gaits which are synthesized offline and then
tracked online. In this work we develop an online nonlinear
model predictive control approach that leverages the full-order
dynamics to realize diverse walking behaviors. Additionally,
this approach can be coupled with gaits synthesized offline
via a desired reference to enable a shorter prediction horizon
and rapid online re-planning, bridging the gap between online
reactive control and offline gait planning. We demonstrate the
proposed method, both with and without an offline gait, on the
planar robot AMBER-3M in simulation and on hardware.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/papers/AmberMPC.pdf" frameborder="0" allowfullscreen></iframe>


## Talk
[Link to Recording](https://mediaspace.wisc.edu/media/DW22_Csomay-Shanklin%2C+Noel+-+June+15th+2022%2C+7A39A39+pm/1_das1yjvq)

## Poster
<!-- Start Writing Below in Markdown -->
<iframe width="100%" height="1670" src="{{ site.baseurl }}/img/DynamicWalkingPoster2022Final.pdf">
