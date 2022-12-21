---
display_to_feed: false
layout:     post
title:      Summer Reading
subtitle:   A Roadmap
author:     Noel Csomay-Shanklin
tags:       Reading
category:   reading
---

## Underactuation
* Francis-Byrnes-Isidori Equations
* Simplest example of a non-full-state feedback linearizeable system with unstable zeros and nonzero coupling
* What is the exact difference between zero dynamics dynamic extensions and backstepping?
* Zeros are in some senses a design choice, but in some senses cannot be avoided. What are the invariants dictating that?
* What are sufficient conditions when you can use planning to converge to an equilibrium point in your zero dynamics? Is it sufficient coupling between the two coordinates? What does that mean?
* What is the nonlinear analog to defining a control with unstable zero dynamics? What are the analogous fundamental limits on performance?

## Multi-Rate Architecture
* Can further assumptions on the MPC program be removed if a higher level planner is used?
* Can C-MPC be used to plan trajectories at different time scales? (Sparse MPC waypoints but calling MPC ripper fast)
* Can Sampled-Data be incorporated to have a truly multi-rate apporach?

## MPC
* What does it mean to have a control invariant for a nonlinear system when all planning is in discrete time? Can we prove that what we did with AMBER was a good idea?
* Along with the above, how do I think about interpolating between these invariants, e.g. in a gait library.
* How do I get fesbile trajectories at time 0 for MPC?
* For C-MPC, can the acceleration of curves be related to the inputs? Can this be added as a constraint as well (likely nonlinear). Can I think about the projection of this onto a Bezier basis, and reason that minimizing bezier acceleration minimizes system acceleration and preserves variational principles?
* Can MPC plan through loss of relative degree? This surely won't work in a multi-rate framework though. Unless you use sampled-data?
* Why is it computationally better to avoid the forward dynamics integration and instead do FL with nonlinear input constraints? i.e. why is the reformulation we used with Manuel (or that Primbs used) any better?
* Understand reduced order model better (kino-dynamic, centroidal, potato, SRB, etc.)
### MPC as a Policy Planner
* What mechnaism allows shrinking tube MPC to become fixed tube MPC when disturbance policies are planned over? 
* Are there good approximations to mitigate the fact that this is an NP hard problem?
### Mixed Tube
* Mixed Tube MPC for LTV systems. Can LTV mpc really capture everything we need for nonlinear systems?
* What decompositions into actuated and underactauted states can be exploited by MPC programs?
* Can one step SQP be used on my actuated states, allowing me to only need to iterate to convergence on my underactuated states?
### Mixed Observability Problems
* Chat with Ugo.
### Planning Shortest Distance over Convex Bodies
* Chat with Andrew.

## Contacts
* Can contacts be modeled via integrals instead of as instantaneous points in time?
* How do we smooth gradient information before and after contact across the switching surface?
* What is the Linear Complementary Problem?

## Optimal Control
* Derivation of Hamilton-Jacobi-Bellman
* How do DDP and SQP apporaches to solving MPC programs differer?

## Discretization
* Exact, Forward Euler, Backward Euler, Tusin, and their properties
* A discrete differential geometric perspective on nonlinear controllability
* In what way do discretization schemes break invriants for dynamical systems? Was this manifested in C-MPC?

## Nonlinear Control
* What are the advantages and disadvantages of using different norms for Lyapunov functions?
* Does it ever make sense to allow the Lyapunov level set to be a decision variable? If so, || . ||2 can be used to retain convexity
* What is reachability geometrically?


