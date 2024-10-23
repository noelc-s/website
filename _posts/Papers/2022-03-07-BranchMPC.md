---
display_to_feed: false
layout:     post
title:      "Interactive multi-modal motion planning with Branch Model Predictive Control"
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Using branch MPC for planning.

## Abstract
Motion planning for autonomous robots and
vehicles in presence of uncontrolled agents remains a chal-
lenging problem as the reactive behaviors of the uncon-
trolled agents must be considered. Since the uncontrolled
agents usually demonstrate multimodal reactive behavior,
the motion planner needs to solve a continuous motion
planning problem under these behaviors, which contains
a discrete element. We propose a branch Model Predictive
Control (MPC) framework that plans over feedback policies
to leverage the reactive behavior of the uncontrolled agent.
In particular, a scenario tree is constructed from a finite
set of policies of the uncontrolled agent, and the branch
MPC solves for a feedback policy in the form of a trajectory
tree, which shares the same topology as the scenario tree.
Moreover, coherent risk measures such as the Conditional
Value at Risk (CVaR) are used as a tuning knob to adjust
the tradeoff between performance and robustness. The
proposed branch MPC framework is tested on an overtake
and lane change task and a merging task for autonomous
vehicles in simulation, and on the motion planning of an
autonomous quadruped robot alongside an uncontrolled
quadruped in experiments. The result demonstrates inter-
esting human-like behaviors, achieving a balance between
safety and performance.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/papers/chen22.pdf" frameborder="0" allowfullscreen></iframe>
