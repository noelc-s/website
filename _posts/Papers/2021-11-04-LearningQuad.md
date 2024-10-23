---
display_to_feed: false
layout:     post
title:      "Online Learning of Unknown Dynamics for Model-Based Controllers in Legged Locomotion"
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Learning parametric uncertainty on a biped and a quadruped.

## Abstract
The performance of a model-based controller can
severely suffer when its model inaccurately represents the real
world dynamics. We propose to learn a time-varying, locally linear
residual model along the robot’s current trajectory, to compensate
for the prediction errors of the controller’s model. Supervised
learning is performed online, as the robot is running in the unknown
environment, using data collected from its immediate past. We
theoretically investigate our method in its general formulation,
then apply it to a bipedal controller derived from the full-order
dynamics of virtual constraints, and a quadrupedal controller
derived from a simplified model of contact forces. For a biped in
simulation, our method consistently outperforms the baseline and
a recent learning-based method. We also experiment with a 12 kg
quadruped in simulation and real world, where the baseline fails
to walk with 10 kg of payload but our method succeeds.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/papers/sun2021online.pdf" frameborder="0" allowfullscreen></iframe>
