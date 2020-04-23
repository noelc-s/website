---
layout:     post
title:		Stochastic Least Squares
subtitle:   An Application of Modules
author:     Noel Csomay-Shanklin
tags: 		Math Reading
category:   reading
---
## Table of Contents
* TOC
{:toc}

## Intro
Let us consider the problem of finding the least squares estimate of the following optimization problem
\\[
\begin{equation}
\begin{aligned}
\min_{x} \quad & \\|y-Hx\\|^2
\end{aligned}
\end{equation}
\\]

## Deterministic Least Squares
Perhaps the most familiar approach to solving this is the calculus approach. Namely, we take the derivative with respect to $x$ and set it equal to zero
\\[
\\begin{align\*}
0 &= \\frac{\\partial}{\\partial x} \\|y-H x\\|^2 \\\
&= \\frac{\\partial}{\\partial x} x^\*H^\*Hx-x^\*H^\*y -  y^\*Hx+y^\*y \\\
&= 2 H^\*H\\hat{x} - 2H^\*y \\\
H^\*H\\hat{x}&=H^\*y
\\end{align\*}
\\]

The last equation in the above sequence is the well-known normal equation. The following discussion will try to arrive at the same solution from the geometric viewpoint.

We will begin by letting $x\in\mathbb{C}^n$ and $y\in\mathbb{C}^N$. We start by interpreting the cost function of (1) as
\\[
\\|y-H \\hat{x}\\|^2 = \\left\\| y-\\sum_{i=0}^{n-1}h_i\\hat{x}(i)\\right\\|^2
\\]
where $h_i$ are the columns of $H$. Almost tautologically, in order for $\hat{x}$ to be the minimizing solution there must be no variation of $\hat{x}(i)$ which could result in a lower cost. Stated another way, we have
\\[
y-\\sum_{i=0}^{n-1}h_i\\hat{x}(i) \\perp h_i,\\qquad i=0,...,n-1,
\\]
or, equivalently,
\\[
h_i^\*\\left(y-\\sum_{i=0}^{n-1}h_i\\hat{x}(i)\\right)=0,\\qquad i=0,...,n-1
\\]
which is identical to 
\\[
H^\*Hx=H^\*y.
\\]
Hence, the solution to the normal equations (the minimizing solution) can be viewed as the projection of $y$ onto the span of the columns of $H$.

## Scalar Stochastic Least Squares
In this case, we consider $x$ as a complex scalar zero-mean random variable, and $y$ as a complex vector-valued zero-mean random variable. Specifically, we have
\\[
y=\\begin{pmatrix}y_1\\\ \\vdots \\\ y_N\\end{pmatrix},\\qquad x\\in\\mathbb{C}.
\\]
We assume $\hat{x}$ is a linear combination of the form
\\[
\\hat{x}=\\sum_{i=0}^{N-1}\\hat{k}_i y_i \\equiv \\hat{x}=\\hat{K}y
\\]
where each $\hat{k}_i$ is a deterministic scalar. We would like to minimize 
\\[
P(\\hat{K}) \\triangleq E[x-\\hat{x}][x-\\hat{x}]^\*,
\\]
or stated another way, find a $\hat{K}$ such that for any $K\ne\hat{K}$ and any scalar $a$, $aP({K})a>aP(\hat{K})a$. Similar to before, perhaps the most employed method to solving the above problem is to differentiate and set equal to zero
\\[
\\begin{align\*}
0&=\\frac{\\partial }{\\partial aK} aP({K})a \\\
&= \\frac{\\partial }{\\partial aK} aE[x-\\hat{x}][x-\\hat{x}]^\*a  \\\
&=\\frac{\\partial }{\\partial aK} a[R_x -R\_\{xy\} K^\* -K R\_\{yx\}+K R_y K^\*]^\*a \\\
&=-R\_\{xy\} + \hat{K} R_y \\\
\\implies R\_\{xy\}  &= \hat{K} R_y
\\end{align\*}
\\]
For a geometric interpretation, we can regard the individual elements $y_1,...y_N,x$ as being vectors in some abstract vector space. In order to perform the same projection that we did in the deterministic least squares problem, we need to define a valid inner product. We propose $\langle A,B \rangle = \mathbb{E}(AB^*)$ for abstract vectors $A$ and $B$. This inner product can be verified to satisfy the required axioms. We can now proceed exactly as we did with the deterministic case, i.e. the minimizing $K$ is one which satisfies
\\[
\\begin{align\*}
x-\\hat{K} y \\perp y_i,&\\qquad i=0,...,N-1 \\\
\\langle x,y_i\\rangle = \\hat{K} \\langle y,y_i\\rangle ,&\\qquad i=0,...,N-1 \\\
\\langle x,y\\rangle &= \\hat{K} \\langle y,y\\rangle \\\
 \\mathbb{E}[xy^\*] &= \\hat{K} \\mathbb{E}[yy^\*] \\\
R\_\{xy\}  &= \\hat{K} R_y
\\end{align\*} 
\\]
Similar to before, we view this equation as the "projection" of $x$ onto the "span of the column space" of y.
## Vector Values Stochastic Least Squares
In the previous two examples, we employed the idea of a vector space over the field of the reals. This can be seen from the fact that our inner product mapped vectors to scalars. For the vector-valued stochastic least squares problem, we will need to utilize the idea of a module, which extends the idea of vector spaces from fields to rings. 

We start by considering the module over the ring of $n\times n$ matrices, which are themselves a matrix ring over the ring of the complex numbers (which admit the even stronger field structure). We can then define an inner product exactly the same as before, i.e. $\langle A,B \rangle = \mathbb{E}(AB^*)$, which results in a (covariance) matrix for arbitrary elements $A$ and $B$ of our defined module. Here is where this construction truly shines: defined in this way, all the prior developments in more canonical vector spaces hold in this abstract setting, and we again retrieve $R\_\{xy\}  = \hat{K} R_y$ where everything is in the form of matrices.




