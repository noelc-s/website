---
display_to_feed: true
layout:     post
title:      Frobenius' Theorem
author:     Noel Csomay-Shanklin
tags: 		  Reading 
subtitle:  	
category:   reading
---
$\require{cancel}$

### Table of Contents
* TOC
{:toc}

# Preliminaries
## [Distributions](https://en.wikipedia.org/wiki/Distribution_(differential_geometry))
A distribution is a collection of subspaces of the tangent bundle assigned to every point on a manifold. That is, for every point $x\in M$, we assign an $n$-dimensional subspace $\Delta_x\subset T_xM$, which depends smoothly on $x$ and have constant dimension for all $x$.
### [Involutivity](https://encyclopediaofmath.org/wiki/Involutive_distribution)
A distribution $\Delta$ is involutive if for any two vector fields $X,Y\in \Delta$, $[X,Y]\in \Delta$
Examples:
Take $M=\mathbb{R}^3$ and coordinates $(x,y,z)$. Consider the distribution $\Delta=\left\\{\frac{\partial}{\partial x}, \frac{\partial}{\partial y}\right\\}$. Because $[X,X]=0$ for any vector field $X$, we simply need to notice that $\left[\frac{\partial}{\partial x}, \frac{\partial}{\partial y}\right]=0\in\Delta$ to conclude that $\Delta$ is involutive. Instead, consider $\Delta=\left\\{\frac{\partial}{\partial x}, x\frac{\partial}{\partial y}+\frac{\partial}{\partial z}\right\\}$. Now,
\\[
\begin{align}
\left[\frac{\partial}{\partial x}, x\frac{\partial}{\partial y}+\frac{\partial}{\partial z}\right] &= \left[\frac{\partial}{\partial x}, x\frac{\partial}{\partial y}\right]+\cancelto{0}{\left[\frac{\partial}{\partial x}, \frac{\partial}{\partial z}\right]}\\\
&=\frac{\partial}{\partial x}\left(x\frac{\partial}{\partial y}\right) - \cancelto{0}{x\frac{\partial}{\partial y}\left(\frac{\partial}{\partial x}\right)} \\\
&= \frac{\partial}{\partial y}
\end{align}
\\]
We require this to be a linear combination of the elements of $\Delta$; however, note that
\\[
\frac{\partial}{\partial y} = a\frac{\partial}{\partial x}+b\left(x\frac{\partial}{\partial y}+\frac{\partial}{\partial z}\right)
\\]
does not hold for any functions $a,b$ and therefore $\Delta$ is not involutive.
### Integrability 
A submanifold $N$ of $M$ is said to be an integrable manifold of $\Delta$ if $T_xN=\Delta$ for any $x\in N$. $\Delta$ is said to be completely integrable if there exists an integral manifold of $\Delta$ through every point $x\in M$.

# Frobenius' Theorem
A distribution $\Delta$ on a manifold $M$ is completely integrable if and only if it is involutive.



# Resources
Control of Stratified Systems with Robotic Applications
http://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Sherwood.pdf
https://faculty.math.illinois.edu/~kapovich/481-14/commutator.pdf
https://math.stackexchange.com/questions/1382071/involutive-distributions
https://www.mathi.uni-heidelberg.de/~lee/Andrea_Rincon.pdf


