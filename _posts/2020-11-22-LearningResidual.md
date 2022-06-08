---
display_to_feed: true
layout:     post
title:      Model Uncertainty and Machine Learning
author:     Noel Csomay-Shanklin
tags: 		  Research
subtitle:  	With Control Barrier Functions
category:   research
---

The following discussion is meant to be a more intuitive example of the methodology employed in the paper: [Episodic Learning for Safe Bipedal Locomotion with
Control Barrier Functions and Projection-to-State Safety](https://arxiv.org/pdf/2105.01697.pdf)

### Table of Contents
{: .no_toc}
* TOC
{:toc}

# Introduction
Consider the following equations of motion for a control-affine system:
\\[
\dot{x} = f(x) + g(x)u.
\\]
Because this is simply a mathematical model of a physical system, there is guaranteed to be some level of uncertainty in the model, i.e. the model does not perfectly capture the evolution of the system. 
In the current setting we will assume that we have perfect knowledge of the state of the system, but uncertainty arises in our knowledge of its time evolution. Treating the above equation as the true equations, as in the unknown equations that govern the motion of the system, we can represent the equations that come from our model as 
\\[
\hat{x} = \hat{f}(x)+\hat{g}(x)\hat{u}(x)
\\]
where $\hat{u}$ is the controller which depends on the model. We can then write the true evolution of the system as 
\\begin{align}
 \dot{x} &= f(x) + g(x)u\notag \\\\ \notag
 &= \hat{f}(x) + \hat{g}(x)u + \overbrace{\underbrace{(f(x)-\hat{f}(x))}\_{b(x)}+\underbrace{(g(x)-\hat{g}(x))}\_{A(x)}u}^{d(x,u)}.
\\end{align}
We use the notion of Control Barrier Functions to ensure safety. To begin, consider a set $\mathcal{C}$ as the superlevel set of a continuously differentiable function $h:\mathbb{R}^n\to \mathbb{R}$. We can define a projected disturbance as 
\\[
\delta \triangleq \dot{h}(x,k(x)) - \hat{\dot{h}}(x,k(x)) = b(x) + a(x)^\top k(x).
\\]
Enforcing the following inequality
\\[
\dot{h}(x,k(x)) \ge -\alpha(h(x)) - \delta(x)
\\]
enforces safety for the system; however the true $\delta(x)$ is unknown. Based on data collected from the evolution of the system, we can try to learn $\hat{\delta}(x)$, an approximation of the true uncertainty in our model. If we learn the uncertainty perfectly, safety for the true system can be enforced through the following quadratic program:
\\begin{align}
    k'(x) =  \\,\\,\underset{u \in \mathbb{R}^m}{\text{argmin}}  &  \quad \frac{1}{2} \| u-k_d(x) \|_2^2  \notag\\\\ \notag
    \mathrm{s.t.} \quad & \quad \widehat{\dot{h}}(x, u) - \hat{\delta}
    \geq -\alpha(h(x)). \nonumber
\\end{align}
In practice, we likely will not be able to learn $\hat{\delta}(x)$ perfectly, but this methodology can be shown to have improved performance when compared to just utilizing the original model.
# Example
This discussion uses the [pendulum]({{ site.baseurl }}{% post_url 2020-07-08-Pendulum%}) as the motivating example, whose dynamics are given by
\\[
\dot{x} = \underbrace{\begin{bmatrix}\dot{\theta}\\\\ -\frac{g}{l}\sin\theta-\frac{b}{ml^2}\dot{\theta}\end{bmatrix}}_{f(x)} +  \underbrace{\begin{bmatrix}0\\\\ \frac{1}{ml^2}\end{bmatrix}}\_{g(x)}u
\\]

Consider a true model with $g=9.81\ m/s^2$, $l=1\ m$, $m=1\ kg$, and $b=0\ Nms^{-1}$, and a perturbed model where the damping term was incorrectly determined to be $b=10\ Nms^{-1}$. Additionally, we use the barrier function 
\\[ h(x) = \dot{\theta}_\max - \dot{\theta}.\\]
In the first episode, the system is allowed to evolve under the above quadratic program with  $\hat{\delta}\equiv 0$. Data is collected and a residual term between the gradient of the measured $h$ and the estimated $\hat{\dot{h}}$ is formed. A model $\hat{\delta}(x)$ is then fit to this residual, shown below. Because uncertainty was added to the damping which affects the dynamics in a linear fashion, a linear model is almost perfectly able to capture the residual term, as shown in the plot below. The residual is plotted in red as a function of state, and the surface represents $\hat{\delta}$.
<img class="center"  style="margin-top:20px;margin-bottom:20px" src="https://noelc-s.github.io/website/img/ResidualFit.svg?sanitize=true">
Now using this estimate of the model uncertainty as it shows up in the barrier function, another episode is run. As compared to episode 0 (blue), episode 1 (orange) is able to ensure safety because all model uncertainty was captured.
<img class="center"  style="margin-top:20px;margin-bottom:20px" src="https://noelc-s.github.io/website/img/ResidualFit2.svg?sanitize=true">
Because uncertainty was injected in a very structured and known way, it was able to be perfectly captured by our chosen model. In a more general setting, and especially on hardware systems, the uncertainty can arise from a number of unknown sources, creating a need for more complicated models, like neural networks.