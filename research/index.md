---
layout: default
title: "Research"
permalink: /research/
---

# Research

Below, you can find a description of several areas of research the SCOPA lab has contributed to. Code related to our research is deployed at [https://github.com/scopagroup](https://github.com/scopagroup).

## Machine Learning

We develop mathematical frameworks that combine neural networks with physical models for parameter estimation and uncertainty quantification in inverse problems. A key focus is on Bayesian inverse problems governed by systems of nonlinear ordinary differential equations. We have shown that neural networks can overcome challenges posed by strong nonlinearities and sharp gradients by learning reconstruction maps from observational data. Our approach enables simultaneous estimation of model parameters, noise parameters (including autocorrelated additive noise and noise modeled via stochastic differential equations), and the covariance matrix of the posterior distribution -- all from a single forward network evaluation.

We have worked on lifted training methods for deep neural networks, which reformulate the nested optimization into higher-dimensional constrained optimization problems amenable to block-coordinate descent with accelerated and stochastic variants. This framework supports non-differentiable proximal activations, improved conditioning, and extends naturally to inverse problems in imaging.

We have proposed efficient clustering on Riemannian manifolds. We have developed a novel approach based on Fréchet maps that embeds high-dimensional, non-Euclidean manifold data (such as symmetric positive definite matrices) into lower-dimensional Euclidean spaces, enabling standard k-means clustering with runtime reductions of up to two orders of magnitude compared to intrinsic manifold-based approaches.


## Optimization Problems Governed by Complex Dynamical Systems

We develop fast iterative methods for large-scale PDE-constrained optimization problems. Our work includes the design and analysis of efficient solvers for optimal control problems governed by hyperbolic transport equations, with applications in image registration, shape matching, and biophysical modeling. We study preconditioned Newton--Krylov methods, operator-splitting schemes, and novel acceleration techniques (including nonlinear GMRES variants) that exploit the structure of the underlying PDE constraints. We have developed fast methods for evaluating forward and adjoint operators in transport dominated problems. We also develop and studied tensorial reduced-order models for parametric coupled reaction-diffusion systems.


## Diffeomorphic Image Registration

We develop scalable, GPU-accelerated algorithms for diffeomorphic image registration. Image registration is a nonlinear inverse problem: given two images of the same object or scene, we seek a spatial mapping that brings one image into alignment with the other. In diffeomorphic image registration, the admissible transformations are restricted to maps that are smooth, one-to-one, and have a smooth inverse. We formulate this as a variational problem governed by transport equations and solve it using an inexact, globalized Gauss--Newton--Krylov method.

Our software tool **CLAIRE** (*Constrained Large Deformation Diffeomorphic Image Registration*) implements these algorithms. CLAIRE features mixed-precision, hardware-accelerated computational kernels for optimal throughput on multi-node, multi-GPU architectures (default) as well as multi-core CPU systems. It can solve clinically relevant registration problems in under four seconds on a single GPU and scales to large-scale 3D imaging problems with billions of voxels. We have designed a novel alternating nonlinear GMRES acceleration method that achieves runtimes up to 5x faster than state-of-the-art Newton--Krylov methods while relying solely on first-order derivatives. We are also exploring novel formulations based on variational principle grid generation methods that construct non-folding grids with prescribed Jacobian determinants and provide accurate inverse transformations within the diffeomorphism group.

CLAIRE is released under the GNU General Public License and is available at [github.com/andreasmang/claire](https://github.com/andreasmang/claire). The deployment page is [andreasmang.github.io/claire](https://andreasmang.github.io/claire).


## Diffeomorphic Shape Matching and Shape Analysis

We develop numerical algorithms for studying the variability of shapes and shape deformations through the lens of geodesic flows of diffeomorphisms. We formulate diffeomorphic shape matching as an ODE-constrained optimization problem, where the ODE constraint models the flow of diffeomorphisms and the velocity is modeled in a reproducing kernel Hilbert space. We use operator-splitting methods (Douglas--Rachford) for numerical optimization. Our algorithms enable rotation-invariant automatic classification of 3D surfaces using registration-based feature vectors, with data augmentation via diffeomorphic interpolation and random flows of smooth diffeomorphisms.

## Parallel and High-Performance Computing

Our algorithms are designed to run efficiently on modern high-performance computing architectures. CLAIRE uses MPI for distributed-memory parallelism and CUDA for GPU acceleration, and has been demonstrated to scale on several supercomputing platforms including multi-node, multi-GPU systems. We have been awarded allocations on the Neocortex supercomputer at the Pittsburgh Supercomputing Center to explore Cerebras-accelerated deep neural networks for scientific computing applications.


## Support
* 2025: NSF CBMS ([DMS-2430460](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2430460))
* 2025: UH DOR GEAR Award
* since 2022: NSF CAREER Award (Computational Mathematics) ([DMS-2145845](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2145845))
* 2023: Allocation on the Neocortex Supercomputer at the Pittsburgh Supercomputing Center
* 2020--2023: NSF Applied Mathematics ([DMS-2009923](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2009923))
* 2020--2023: NSF Computational Mathematics ([DMS-2012825](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2012825))
* 2019--2022: NSF CDS&E-MSS ([DMS-1854853](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1854853))
* 2019: NVIDIA Corporation GPU Grant Program (Accelerated Data Science Call)
* 2018: SIMONS Foundation Collaboration Grants for Mathematicians (Award 586055)

Talks and posters given by lab members are listed on the [publications page]({{ site.baseurl }}/publications/).
