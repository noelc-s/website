---
layout:     post
title:      Model Uncertainty and Machine Learning
author:     Noel Csomay-Shanklin
tags: 		  Reading 
subtitle:  	With Control Barrier Functions
show: false
category:   reading
---

### Table of Contents
* TOC
{:toc}

# Introduction
In this setting, we are considering systems subject to Control Barrier Functions to ensure safety. To begin, consider a set $\mathcal{C}$ as the superlevel set of a continuously differentiable function $h:\mathbb{R}^n\to \mathbb{R}$. For the pendulum, the equations of motion can we written as 
\\[
\dot{x} = f(x) + g(x)u
\\]
Because this is simply a mathematical model of a physical system, there is guaranteed to be some level of uncertainty in the model, i.e. the model does not perfectly capture the evolution of the system. 
In the current setting we will assume that we have perfect knowledge of the state of the system, but uncertainty arises in our knowledge of its time evolution. Treating the above equation as the true equations, as in the unknown equations that govern the motion of the system, we car represent the equations that come from our model as 
\\[
\hat{x} = \hat{f}(x)+\hat{g}(x)\hat{u}(x)
\\]
where $\hat{u}$ is the controller which depends on the model. We can then write the true evolution of the system as 
\\begin{align}
 \dot{x} &= f(x) + g(x)u\notag \\\\ \notag
 &= \hat{f}(x) + \hat{g}(x)u + \overbrace{\underbrace{(f(x)-\hat{f}(x))}\_{b(x)}+\underbrace{(g(x)-\hat{g}(x))}\_{A(x)}u}^{d(x,u)}.
\\end{align}
Given the CBF $h$, we can define a projected disturbance as 
\\[
\delta \triangleq \dot{h}(x,k(x)) - \hat{\dot{h}}(x,k(x)) = b(x) + a(x)^\top k(x).
\\]
This leads to 
\\[
\dot{h}(x,k(x)) \ge -\alpha(h(x)) - \delta(x).
\\]
Based on data collected from the evolution of the system, we can try to learn $\hat{\delta}(x)$, an approximation of the true uncertainty in our model. If we learn the uncertainty perfectly, safety for the true system can be enforced through the following quadratic program:
\\begin{align}
    k'(x) =  \\,\\,\underset{u \in \mathbb{R}^m}{\text{argmin}}  &  \quad \frac{1}{2} \| u-k_d(x) \|_2^2  \notag\\\\ \notag
    \mathrm{s.t.} \quad & \quad \widehat{\dot{h}}(x, u) - \hat{\delta}
    \geq -\alpha(h(x)). \nonumber
\\end{align}
In practice, we likely will not be able to learn $\hat{\delta}(x)$ perfectly, but this methodology can be shown to have improved performance when compared to just utilizing the original model.
# Example
This discussion uses the [pendulum]({{ site.baseurl }}{% post_url 2020-03-08-Pendulum%}) as the motivating example, whose dynamics are given by
\\[
\dot{x} = \underbrace{\begin{bmatrix}\dot{\theta}\\\\ -\frac{mgl}{J}\sin\theta-b\dot{\theta}\end{bmatrix}}_{f(x)} +  \underbrace{\begin{bmatrix}0\\\\ 1\end{bmatrix}}\_{g(x)}u
\\]

Consider a true model with $g=9.81\ m/s^2$, $l=1\ m$, $m=1\ kg$, and $b=0\ Nms^{-1}$, and a perturbed model where the damping term was incorrectly determined to be $b=10\ Nms^{-1}$. Additionally, we use the barrier function 
\\[ h(x) = \dot{\theta}_\max - \dot{\theta}\\]
The basic CBF-QP would result in the following behavior

# Conclusion
The above discussion has been a simpler example of the methodology employed in the paper
