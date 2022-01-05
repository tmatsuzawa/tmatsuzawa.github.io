---
layout: post
section-type: post
title: Calculus
category: personal
tags: [ 'personal', 'math']
---

These are notes on things that I tend to forget.

Saffman p.51 Sect.3.2. Eq.15
$$
\begin{aligned}
  \int_V \pmb{u} d\pmb{x} = \int_{\partial V} \pmb{x} (\pmb{u} \cdot \pmb{n}) dS
\end{aligned}
$$
This identity seems to hold only for incompressible fluids.

Proof:


<hr>
$$
\begin{aligned}
  \int \nabla^2 \pmb{u} dV = - \int (\hat{\pmb{n}} \cdot \nabla) \pmb{u} dS 
\end{aligned}
$$

<hr>
Saffman p.49 Sect.3.2. Eq.5:
$$
\begin{aligned}
  \int omega_i (\pmb{x}) d\pmb{x} &= \int \partial_j (x_i \omega_j) d\pmb{x} = \int (\partial_j x_i) \omega_i + x_i \partial_j \omega_i d\pmb{x}  = \int \delta_{ij} \omega_i + x_i \partial_j \omega_j d\pmb{x} \because  \partial_j \omega_j= \text{div curl} \pmb{u}=0\\
    &= \int_S x_i \pmb{\omega} \cdot \pmb{n} dS \because \text{Gauss's theorem}
\end{aligned}
$$