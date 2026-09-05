---
layout: default
title: "Home"
permalink: /
---

<div class="hero">
<h1>SCOPA Lab</h1>
<p>Integrating <span class="hero-accent">data</span> with <span class="hero-accent">simulation</span> to enable data-driven discovery in the applied sciences.</p>
</div>

## Overview

The **Scientific Computing, Optimization, and Parallel Algorithms** (SCOPA) lab is part of the [Department of Mathematics](https://math.tufts.edu) at Tufts University.

Our goal is the design of principled and scalable algorithms at the interface of machine learning, optimization, and scientific computing that integrate *data* with *simulation* to enable data-driven discovery in the applied sciences. We are interested in methods that combine the interpretability and predictive power of mechanistic models with the flexibility of learning, and in the numerical analysis that makes them trustworthy --- stability, structure preservation, and a rigorous accounting of uncertainty. Our work is driven by applications in medical imaging and the life sciences, and much of it is released as open-source software for GPU and supercomputing platforms.

## Research Areas

- Scientific machine learning and data-driven modeling
- Inverse problems and PDE-constrained optimization
- Numerical optimization, including optimization for machine learning
- Tensor methods, model reduction, and surrogate models
- Uncertainty quantification and Bayesian inference
- Nonlinear optimal control
- Geometric methods and the analysis of shapes and manifold-valued data
- Scalable, parallel, and GPU-accelerated algorithms

## Research Themes

<div class="research-grid">
<div class="research-card">
<h3>Integrating models with data</h3>
<p>Much of our work concerns settings in which a mechanistic model &mdash; typically a system of differential equations &mdash; must be reconciled with observations. This leads to large-scale problems that are nonconvex, ill-posed, and expensive to solve. We are interested in formulations that respect the structure of the underlying problem, in fast solvers that make such problems tractable at realistic scale, and in Bayesian and randomized techniques that quantify the uncertainty of the resulting estimates.</p>
</div>
<div class="research-card">
<h3>Learning and numerics</h3>
<p>Mechanistic models are interpretable and extrapolate beyond the data, but they are costly; learned models are fast and flexible, but can be opaque and unreliable outside the regime they were trained on. A growing part of our work combines the two in a principled way, through continuous-time and dynamical-systems formulations of learning, structure- and stability-preserving discretizations, optimization methods for training, and surrogate and operator-learning frameworks. The guiding question is how to bring the standards of numerical analysis &mdash; stability, convergence, well-posedness &mdash; to methods that learn from data.</p>
</div>
<div class="research-card">
<h3>Reduction and scale</h3>
<p>Making these problems affordable is itself a mathematical question. Tensor-based reduced-order models and learned surrogates compress parametric models into forms cheap enough for many-query settings such as model calibration, uncertainty quantification, and digital twins. Complementing this, we design parallel and GPU-accelerated algorithms so that the resulting methods scale from a workstation to a supercomputer.</p>
</div>
<div class="research-card">
<h3>Geometry and applications</h3>
<p>Many of the objects we work with &mdash; images, shapes, deformations, and covariance structures &mdash; do not live in flat vector spaces, and respecting their geometry is often what makes an algorithm both meaningful and efficient. These methods are driven by applications in medical imaging and the life sciences, including computational anatomy, biophysical modeling of disease progression, cardiology, and systems biology.</p>
</div>
</div>

A more detailed description of our work is on the [research page]({{ '/research/' | relative_url }}); our [publications, talks, and posters]({{ '/publications/' | relative_url }}) and [lab members]({{ '/people/' | relative_url }}) are listed separately. Code is released at [github.com/scopagroup](https://github.com/scopagroup).
