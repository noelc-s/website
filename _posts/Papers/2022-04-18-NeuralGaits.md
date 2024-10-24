---
display_to_feed: true
layout:     post
title:      "Neural Gaits: Learning Bipedal Locomotion via Control Barrier Functions and Zero Dynamics Policies"
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Using control barrier functions to define a stable walking gait for a biped.

## Abstract
This work presents Neural Gaits, a method for learning dynamic walking gaits through the enforce-
ment of set invariance that can be refined episodically using experimental data from the robot. We
frame walking as a set invariance problem enforceable via control barrier functions (CBFs) defined
on the reduced-order dynamics quantifying the underactuated component of the robot: the zero
dynamics. Our approach contains two learning modules: one for learning a policy that satisfies
the CBF condition, and another for learning a residual dynamics model to refine imperfections of
the nominal model. Importantly, learning only over the zero dynamics significantly reduces the
dimensionality of the learning problem while using CBFs allows us to still make guarantees for the
full-order system. The method is demonstrated experimentally on an underactuated bipedal robot,
where we are able to show agile and dynamic locomotion, even with partially unknown dynamics.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/papers/gaits.pdf" frameborder="0" allowfullscreen></iframe>
