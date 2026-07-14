---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

<!-- TODO: Replace the placeholder text below with your own words. -->

I am a PhD candidate in Mechanical Engineering working on the **aeroelastic
design optimization of wind turbines**. My work sits at the intersection of
large-scale gradient-based optimization and machine learning, with the goal of
designing turbines that are more cost-effective.

## Aeroelastic design optimization of wind turbines
With the increase in energy requirements throughout the world, there is a need for higher energy generation. There are many different avenues to meet this need and it seems prudent to pursue as many viable options as possible, including renewable sources such as wind energy. To competitively meet the energy demand, wind energy must become more cost-effective. 

Wind turbines are an interesting design problem because of their multi-disciplinary nature. The complex interaction of the physics of aerodynamics and the physics of the structure creates a coupled problem that requires analyzing both simultaneously. Many have done great work incorporating static analysis of both aerodynamics and structures into design optimization, but far fewer have included unsteady analysis, including the effects of fatigue. Unsteady analysis is difficult to accurately conduct and even more difficult to include into a design optimization. One reason it is so difficult to include into an optimization is the amount of time required for each analysis. In a design optimization you often need hundreds, if not thousands of evaluations of your analysis. If an analysis is long, then a design optimization quickly becomes intractable. My work focuses on creating efficient unsteady aerostructural analysis software designed for design optimization. 

## Gradient computation
Wind turbines require a large number of *design variables* to mathematically describe the design. Gradient-based design optimization is typically a more efficient approach to solving a design problem with many design variables. It comes at the added cost of computing derivatives. In my work, I show how using efficient gradient computation methods such as automatic differentiation, implicit differentiation, and adjoint methods allow for high-dimensional design optimizations that include unsteady effects. 

## Deep-learning surrogates

_Describe your surrogate-modeling work — what quantities you emulate, the
architectures you use, and how the surrogates plug into the optimization loop._

---

**Selected publications** appear on the [Publications]({{ base_path }}/publications/)
page; software and tools are on the [Projects]({{ base_path }}/portfolio/) page.
