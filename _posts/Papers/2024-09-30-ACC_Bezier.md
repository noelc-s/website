---
display_to_feed: false
layout:     post
title:      Bezier Reachable Polytopes
subtitle:   Efficient Certificates for Robust Motion Planning with Layered Architectures
author:     Noel Csomay-Shanklin
tags: 		  Research
category:   research
---

## Overview
Reachable sets in Bezier polynomial space can be represented as polytopes.

## Abstract
Control architectures are often implemented in
a layered fashion, combining independently designed blocks
to achieve complex tasks. Providing guarantees for such
hierarchical frameworks requires considering the capabilities
and limitations of each layer and their interconnections at
design time. To address this holistic design challenge, we
introduce the notion of Bézier Reachable Polytopes – certificates
of reachable points in the space of Bézier polynomial reference
trajectories. This approach captures the set of trajectories that
can be tracked by a low-level controller while satisfying state
and input constraints, and leverages the geometric properties
of Bézier polynomials to maintain an efficient polytopic repre-
sentation. As a result, these certificates serve as a constructive
tool for layered architectures, enabling long-horizon tasks to
be reasoned about in a computationally tractable manner.

## Paper
<iframe style="width:100%" height="1000px" src="https://noelc-s.github.io/website/img/BezierPolytopes.pdf" frameborder="0" allowfullscreen></iframe>
