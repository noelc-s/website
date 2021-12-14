---
display_to_feed: true
layout:     post
title:      Supporting Hyperplane Theorem
author:     Noel Csomay-Shanklin
tags: 		  School 
subtitle:  	Mathematical Optimization
category:   school
---
## Table of Contents
* TOC
{:toc}

## Projection onto Convex Sets Theorem
Let $\mathcal{C}\subset\mathbb{R}^n$ be a closed, convex set. For any $x\in\mathbb{R}^n$, consider the following optimisation problem
\\[
\inf_{z\in\mathbb{R}^n}\\|x-z\\|_2\quad\text{s.t.}\ z\in\mathcal{C}\notag.
\\]
The optimal point is attained uniquely at a point in $\mathcal{C}$.
### *Proof*
Fix any $y\in\mathcal{C}$. Then we have that 
\\[
\inf_{z\in\mathbb{R}^n}\\|x-z\\|\quad\text{s.t.}\ z\in\mathcal{C}
\\]
is equivalent to
\\[
\inf_{z\in\mathbb{R}^n}\\|x-z\\|\quad\text{s.t.}\ z\in\mathcal{C}\cap B(x,\\|x-y\\|)
\\]
Because the intersection of two closed, convex sets is similary closed and convex, the set $\mathcal{C}\cap B(x,\\|x-y\\|)$ is closed and convex. Further, $\mathcal{C}\cap B(x,\\|x-y\\|)\subseteq B(x,\\|x-y\\|)$ and therefore $\mathcal{C}\cap B(x,\\|x-y\\|)$ is bounded. As the function $\\|x-z\\|$ is continuous in $z$, we have that the optimal value is attained. concerning the question of uniqueness, supose for the sake of contradiction that there exists $z_1\ne z_2 \in\mathcal{C}$ such that both $z_1$ and $z_2$ are optimal solutions. Consider the point $\frac{z_1+z_2}{2}\in\mathcal{C}$ (due to the convexity of $\mathcal{C}$). We have that
\\[
\begin{align}
\left\\|\frac{z_1+z_2}{2}-x\right\\|^2 &= \left\\|\frac{z_1 -x}{2}+\frac{z_2-x}{2}\right\\|^2 \notag\\\
&= \frac{1}{2}\\|z_1-x\\|^2+\frac{1}{2}\\|z_2-x\\|^2-\left\\|\frac{z_1-x}{2}-\frac{z_2-x}{2}\right\\|^2\notag\\\
&= \frac{1}{2}\\|z_1-x\\|^2+\frac{1}{2}\\|z_2-x\\|^2-\left\\|\frac{z_1-z_2}{2}\right\\|^2\notag
\end{align}
\\]
This gives us the desired contradiction, as 
\\[
\left\\|\frac{z_1+z_2}{2}-x\right\\|<\\|z_1-x\\|
\\]
unless $z_1=z_2$
$$\tag*{$\blacksquare$}$$

## Inner Product in Convex Set Lemma
Let $\mathcal{C}\subset\mathbb{R}^n$ be a convex set and let $x\in\mathbb{R}^n$ be any point. Further, let $z^* \in\text{cl}(\mathcal{C})$ be the closest point to $x$ in cl($\mathcal{C}$). Then we have that
\\[
(x-z^* )^\top (z-z^* )\le 0\ \forall\ z\in\mathcal{C}
\\]
### *Proof*
\\[
\begin{align}
\\|x-z^* \\|^2 &\le \\|x-z\\|^2\ \forall\ z\in\mathcal{C}\notag\\\
&=\\|(x-z^* )+(z^* -z)\\|^2\notag\\\
&=\\|x-z^* \\|^2+\\|z-z^* \\|^2+2\langle x-z^* ,z^* -z \rangle\notag.
\end{align}
\\]
Therefore,
\\[
\begin{align}
2(x-z^* )^\top (z^* -z) &\ge -\\|z-z^* \\|^2 \notag\\\
2(x-z^* )^\top (z-z^* ) &\le \\|z-z^* \\|^2 \notag\\\
(x-z^* )^\top (z-z^* )& \le 0\notag.
\end{align}
\\]
$$\tag*{$\square$}$$
### Remark
The last step holds due to the following logic from analysis. Suppose that $z=z^* $. Then we are done. Suppose now that $z\ne z^* $. Then the inequality
\\[
2(x-z^* )^\top (z-z^* ) \le \\|z-z^* \\|^2
\\]
can be rewritten as
\\[
2(x-z^* )^\top \frac{(z-z^* )}{ \\|z-z^* \\| } \le \\|z-z^* \\|.
\\]
Note that as $z\to z^* $, the right hand side tends to zero while the left hand side doesn't change. Therefore, we have that 
\\[
\begin{align}
2(x-z^* )^\top \frac{(z-z^* )}{ \\|z-z^* \\| } \le 0 \notag\\\
2(x-z^* )^\top (z-z^* ) \le 0.\notag
\end{align}
\\]
## Supporting Hyperplane Theorem
Let $\mathcal{C}\subset\mathbb{R}^n$ be a convex set and let $w\notin\text{relint}(\mathcal{C})\in\mathbb{R}^n$ be a point. Then there exists $a\in\mathbb{R}^n\backslash\\{0\\}$ and $b\in\mathbb{R}$ such that 
\\[
\begin{align}
a^\top w &= b\notag\\\
\inf_{x\in\mathcal{C}}a^\top x &\ge b \notag
\end{align}
\\]
### *Proof*
Consider the sequence $\\{w_k\\}\to w$; we know from the fact that $w\notin\text{relint}(\mathcal{C})$ that $w_k\notin\text{cl}(\mathcal{C})$. 
For each $k$, let $a_k=\frac{z_k^* - w_k}{\\|z_k^* - w_k\\|}$ where $z_k^* $ is the closest point to $w_k$ in cl($\mathcal{C}$) (the existence and uniqueness of which is garuneed by the Projection onto Convex Sets Theorem from before). As $w_k\notin\text{cl}(\mathcal{C})$, we have that $\\|z_k^* - w_k\\|\ne 0$.
Because the sequence $\\{a_k\\}$ is bounded, from the Bolzano-Weierstrass theorem we know that there exists a convergent subsequence $\\{a_i\\}_{i\in I}$ with $a_i\to a^* $.
For each $i\in I$, we have from the Inner Product in Convex Sets Lemma that 
\\[
(w_i-z_i^* )^\top (z-z_i^* )\le 0\ \forall\ z\in\mathcal{C}.
\\]
Substituting values, we have that
\\[
\begin{align}
-a_i^\top (z-z_i^* )&\le 0\ \forall\ z\in\mathcal{C} \notag \\\
a_i^\top z_i^* &= a_i^\top (z_i^* -w ) + a_i^\top w_i \notag
\end{align}
\\]
which implies that 
\\[
a_i^\top w_i < a_i^\top z_i^*
\\]
as $a_i^\top (z_i^* - w_i) > 0$. Hence, we have that 
\\[
a_i^\top z > a_i^\top w_i\ \forall\ z\in\mathcal{C}.
\\]
Letting $a_i\to a^* $ and $w_i \to w$, we have that 
\\[
a^{* \top} z > a^{* \top} w\ \forall\ z\in\mathcal{C}.
\\]
We have that $a^* \ne 0$ as it is the limit of a sequence of unit vectors. Setting $b=a^{* \top} w$, we are done.
$$\tag*{$\blacksquare$}$$
