---
layout:     post
title:      Mathematical Terminology
author:     Noel Csomay-Shanklin
tags: 		  Reading 
category:   reading
---
A list of mathematical terms I have come across and needed to look up.
## Table of Contents
* TOC
{:toc}

## Spaces
---
### Topological Space
Informally, a set of points, along with a set of neighbourhoods for each point satisfying a set of axioms relating points and neighbourhoods. Formally, let $X$ be a set, and let $\mathscr{U}$ be a collection of subsets of $X$. $\mathscr{U}$ is called a topology on X if
1. $X,\emptyset\in\mathscr{U}$;
2. $\\{U_{\alpha}\\}$, an arbitrary collection of elements of $\mathscr{U}$, implies that $\cup_{\alpha}U_\alpha\in\mathscr{U}$;
3. $\\{U_j \\}^n_{j=1}$, a finite collection of elements of $\mathscr{U}$, implies that $\cap_{j=1}^n U_j\in\mathscr{U}$

The pair $(X,\mathscr{U})$ is called a topological space, and the elements of $\mathscr{U}$ are called open sets.

### Metric Space
Informally, a metric space is a space imbued with a "sense of distance". Formally, let $X$ be a set. A function $d:X\times X\to\mathbb{R}$ is said to be a matric on $X$ if 
1. $d(u,v)\ge0$ for all $u,v\in X$, and $d(u,v)=0$ if and only if $u=v$;
2. $d(u,v)=d(v,u)$ for all $u,v\in X$; and
3. $d(u,v)\le d(u,w)+d(w,v)$ for all $u,v,w\in X$.

The pair $(X,d)$ is called a metric space.

### Dual Space
Any vector space $V$ has a corrseponding dual vector space, $V^\*$, consisting of all linear functionals on V. Formally, given any vector space $V$ over a field $\mathbb{F}$, the (algebraic) dual space $V^*$ is the set of all linear maps $\varphi:V\to\mathbb{F}$.

## Topology-esque
---
### Morphism
A morphism is a strucutre-preserving map between mathematical structures of the same type.
### Endomorphism
A morphism from an object to itself. An endomorphism that is also an isomorphism is an automorphism.
#### Example
The orthogonal projection onto a line is an endomorphism on the plane which is not an automorphism.
### Isomorphism
A bijective morphism.
### Homomorphism
A mapping between two algebraic objects, which preserves operation in those objects. 
### Homeomorphism
A continuous topological isomorphism. In other words, it is a continuous function between topological spaces with continuous inverse.
### Diffeomorphism
A differentiable homeomorphism, i.e. a continously differentiable mapping between topological spaces with continuously differentiable inverse.
### Examples
Let $(G, * )$ and $(H,\cdot)$ be two groups. A group homomorphism is a map $\rho:G\to H$ that satisfies $\rho (a*b)=\rho(a)\cdot \rho(b)$. If $\rho$ is bijective, then it is a group isomorphism. In this case, $G$ and $H$ are isomorphic, written as $G\cong H$.

## Differential Geometry
---
### [Manifold](https://en.wikipedia.org/wiki/Manifold)
Informally, a manifold is a "surface", i.e. a space that is locally Euclidean. Formally, a (topological) manifold is a second countable Hausdorff space that is locally homeomorphic to Euclidean space.
### [Foliage](https://en.wikipedia.org/wiki/Foliation)
An equivalence relation on an $n$-manifold, the equivalence classes being connected, injectively immersed submanifolds, all of the same dimension $p$, modeled on the decomposition of the real coordinate space $\mathbb{R}^n$ into the cosets $x+\mathbb{R}^p$ of the standardly embedded subspace $\mathbb{R}^p$.
### [Fiber Bundle](https://en.wikipedia.org/wiki/Fiber_bundle#Examples)
Informally, a fiber bundle is locally a product space, but globally may have a different topological structure. If the fiber bundle is just a product space, it is known as the trivial bundle. 
#### Sections of Fiber Bundles
Let $B$ be the base space, $F$ be the fiber, and $E$ be the total space of the fiber bundle. A section of the fiber bundle $E$ is given by a continuous map $\sigma:B\to E$ such that $\pi(\sigma(x))=x$ for all $x\in B$. A section of the tangent bundle $TM$ is a vector field on $M$.
#### Examples
Consider the base space $B=\mathbb{S}^1$, the Fiber $F=\mathbb{R}$, and the trivial bundle $E=B\times F$, which manifests itself as a cylinder. An example of a nontrivial fiber bundle with the same form would be the M\"obius strip. If instead $F=\mathbb{S}^1$, the trivial bundle would be the torus and the klein bottle would be an example of a nontrivial bundle.
### Vector Bundle
A fiber bundle whose fibers are vector spaces.
### Tangent Bundle
The tangent bundle to a manifold $M$ is a manifold $TM$ that is the disjoint union of the tangent spaces of $M$. The tangent bundle is the prototypical example of a vector bundle.
### Cotangent Bundle
The dual bundle of the Tangent Bundle, conistent of all of the cotangent spaces at every point in the manifold.
### Lie Derivative
The Lie derivative evaluates the change of a tensor field along the flow defined by another vector field.
#### Example
$\dot{V}=\frac{dV}{dx}\dot{x}$ represents the Lie derivative of the scalar field $V$ (Lyapunov function) along the flow defined by the vector field given by the dynamics of a system.

## Abstract Algebra
---
### Group
A group is a set equipped with a binary operation which satisfies the group axioms, given by
1. Closure
2. Associativity
3. Identity Element
4. Inverse Element

### Ring
A ring is a set equipped with two binary operations that generalize the arithmetic operations of addition and multiplication. More rigorously, a ring is a set $\mathbf{R}$ equipped with two binary operations $+$ and $\cdot$ satisfying the ring axioms, given by
1. $\mathbf{R}$ is an abelian group under addition
2. $\mathbf{R}$ is a monoid under multiplication
3. Multiplication is distributive with respect to addition

### [Module](https://en.wikipedia.org/wiki/Module_(mathematics))
A module over a ring is a generalization of the notion of a vector space over a fieds, wherein the corresponding scalars are the elemnts of a given ring, and multiplication is defined between elements of the ring and elements of the module.

### [Algebra over a Field (Algebra)](https://en.wikipedia.org/wiki/Algebra_over_a_field)
A vector space equipped with a bilinear product. Thus, an algebra is an algebraic structure, which consists of a set, together with operations of multiplication, addition, and scalar multiplication by elements of the underlying field, and satisfies the axioms implied by "vector space" and "bilinear".

## Still Fuzzy On
---
### Injection, Emersion, Submersion
### Riemannian Metrics
### Germs, sheafs
### Jets, Jet bundles
### One form, n-forms



