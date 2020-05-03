---
layout:     post
title:      Lie Theory
subtitle:   ""
author:     Noel Csomay-Shanklin
tags:       Reading
category:   reading
---
## Table of Contents
* TOC
{:toc}

## Lie Groups
Preliminary: See [group]({{ site.baseurl }}{% post_url 2020-03-22-MathTerms %}#group). A Lie group is a group whose elements are organized continuously and smoothly. As illustrative examples, consider the symmetry groups $D_4$ and $\mathbb{T}$. $D_4$ consists of the set of 90 degree rotations with group operation given by composition, and $\mathcal{U}(1)$ is unit circle in the complex plane, representing the set of continuous rotations about the origin, with group operation given by complex multiplication. It can easily be verified that these satisfy the group axioms. Groups can be used as symmetry preserving operations on sets through their group action. Using our examples, $D_4$ represents a group action for the set defining the square in the plane, and $\mathbb{T}$ is a group action for the circle in the plane. It is obvious to see that $D_4$ is discrete, and therefore cannot be a Lie group, whereas $\mathbb{T}$ is continuous and smooth and therefore admits Lie group structure.

## Lie Algebras
Preliminary: See [tangent bundle]({{ site.baseurl }}{% post_url 2020-03-22-MathTerms %}##tangent-bundle). Any Lie group gives ruse to its Lie algebra through the tangent space at the identity. As an example, consider $\mathbb{S}^1=\mathbb{T}$ as was used in the above section. The identity element of $\mathbb{S}^1$ is given by 1. The lie algebra $\mathfrak{s}^1$ is given by the tangent space of $\mathbb{S}^1$ at 1, $T_1\mathbb{S}^1=i\mathbb{R}\simeq \mathbb{R}$. The usefulness of Lie algebras is that the lie algebra is a vector space (linear), and there is a one-to-one correspondence with the associated (potentially nonlinear) Lie group. 

An excellent depiction and explanation of Lie groups and algebras from "A micro Lie theory for state estimation in robotics" [see first reference].
<img style="margin:20px 20px" src="https://noelc-s.github.io/website/img/LieTheory.png">
## Resources
* [A micro Lie theory for state estimation in robotics](https://arxiv.org/abs/1812.01537)
* [Physics from Symmetry](https://link.springer.com/book/10.1007/978-3-319-66631-0)
* [Lie groups and their Lie algebras](https://www.youtube.com/watch?v=mJ8ZDdA10GY&t=3501s)
* [Table of Lie groups](https://en.wikipedia.org/wiki/Table_of_Lie_groups)