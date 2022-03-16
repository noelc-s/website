---
display_to_feed: true
layout:     post
title:      Nonlinear Controllability
subtitle:   An Application of Differential Geometry and Frobenius Theorem
author:     Noel Csomay-Shanklin
tags: 		  Reading
category:   reading
---

### Table of Contents
* TOC
{:toc}

## Linear Controllability
A linear system is controllable if for any $x_0, x_f \in \mathbb{R}^n$ there exists a $T > 0$ and $u: [0,T] \to\mathbb{R}$ such that if $x(0) = x_0$ then the corresponding solution satisfies $x(T) = x_f$.

### Solution to linear systems
The solution to 
\\[
\dot x = Ax + Bu
\\]
is given by:
\\[
x(t) = x_0e^{At} + \int_0^t e^{A(t-\tau)Bu(\tau)d\tau}.
\\]
<!-- Proof:
Differentiating both sides we get:
\\[
\dot x(t) = Ax_0e^{At} + \int_0^t Ae^{A(t-\tau)}Bu(\tau)d\tau + Bu(t) = Ax + Bu.
\\]
$$\tag*{$\blacksquare$}$$
 -->

### Controllable Subspace
Without loss of generality, assume that $x_0=0$ (any system that is controllable from $x_0=0$ is controllable from any nonzero initial state). Under a change of variables, we have 
\\[
x(t) = \int_0^t e^{A\tau}Bu(t-\tau)d\tau.
\\]
From Cayley-Hamilton, we can write any analytic function of an $n\times n$ matrix as an $(n-1)^{th}$ degree polynomial of the matrix. Specifically, we get
\\[
e^{At} = \sum_{i=0}^{n-1}\alpha_i(t)A^i
\\]
for some $\alpha_i(t) \in \mathbb{R}$. Substituting this into our above expression, we get
\\[
\begin{align}
x(t) &= \int_0^t \left(\alpha_0(t)Bu(t-\tau) + \alpha_1(t)ABu(t-\tau) + \dots + \alpha_{n-1}A^{n-1}Bu(t-\tau)\right)d\tau \notag \\\\\
&= B \int_0^t \alpha_0(t)u(t-\tau) + AB\int_0^t\alpha_1(t)u(t-\tau) + \dots + A^{n-1}B\int_0^t\alpha_{n-1}u(t-\tau)d\tau. \notag
\end{align}
\\]

The smallest A-invariant subpace containing B



### Distribution

## Frobenius Theorem
A nonsingular distribution is completely integrable if and only if it is involutive

### Tangent Bundle

### Nonsingular Distributions



### Complete Integrability

### Involutivity

### Proof

## Nonlinear Controllability

The definition of nonlinear controllability is more nuanced.


## Resources
[Nonlinear Control Systems -- Isidori](https://link.springer.com/book/10.1007/978-1-84628-615-5)
[Feedback Systems -- Astrom, Murray](http://www.cds.caltech.edu/~murray/books/AM08/pdf/fbs-public_24Jul2020.pdf)
[Linear Controllability](https://ocw.mit.edu/courses/aeronautics-and-astronautics/16-30-feedback-control-systems-fall-2010/lecture-notes/MIT16_30F10_lec10.pdf)
[Derivative of a Delta Dirac impulse](https://dsp.stackexchange.com/questions/68732/what-is-the-first-derivative-of-dirac-delta-function)
[Cayley-Hamilton](https://en.wikipedia.org/wiki/Cayley%E2%80%93Hamilton_theorem)