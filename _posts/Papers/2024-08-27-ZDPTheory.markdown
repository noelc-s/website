---
display_to_feed: true
layout:     post
title:      "Constructive Nonlinear Control of Underactuated Systems via Zero Dynamics Policies"
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Using optimal control and learned output tracking to stabilize underactuated systems.

## Abstract
Stabilizing underactuated systems is an inherently
challenging control task due to fundamental limitations on how
the control input affects the unactuated dynamics. Decompos-
ing the system into actuated (output) and unactuated (zero)
coordinates provides useful insight as to how input enters the
system dynamics. In this work, we leverage the structure of this
decomposition to formalize the idea of Zero Dynamics Policies
(ZDPs)—a mapping from the unactuated coordinates to desired
actuated coordinates. Specifically, we show that a ZDP exists in
a neighborhood of the origin, and prove that combining output
stabilization with a ZDP results in stability of the full system
state. We detail a constructive method of obtaining ZDPs in
a neighborhood of the origin, and propose a learning-based
approach which leverages optimal control to obtain ZDPs with
much larger regions of attraction. We demonstrate that such a
paradigm can be used to stabilize the canonical underactuated
system of the cartpole, and showcase an improvement over the
nominal performance of LQR.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/papers/ZDPTheory.pdf" frameborder="0" allowfullscreen></iframe>
