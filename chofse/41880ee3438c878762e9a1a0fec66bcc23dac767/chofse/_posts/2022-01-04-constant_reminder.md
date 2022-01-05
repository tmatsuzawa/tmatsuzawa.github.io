---
layout: post
section-type: post
title: Calculus
category: personal
tags: [ 'personal', 'math']
---

These are notes on things that I tend to forget.

Saffman p.51 Sect.3.2. Eq.15:
<br>
<br>
$$
\begin{align}
  \int_V \pmb{u} d\pmb{x} = \int_{\partial V} \pmb{x} (\pmb{u} \cdot \pmb{n}) dS \label{eq:SaffmanSect3-2-15}
\end{align}
$$
<br>
This identity seems to hold only for incompressible fluids.
<br>
Proof:<br>
We begin with a corollary on the divergence theorem.
$$
\int_V [\pmb{u} \cdot (\nabla g) + g(\nabla \cdot \pmb{u})] dV = \int_{\partial V} g (\pmb{u} \cdot \pmb{n}) dS
$$<br>
Setting $g=x_i$ yields<br>
$$
\int_V [\pmb{u} + \pmb{x} (\nabla \cdot \pmb{u})] dV = \int_{\partial V} \pmb{x}  (\pmb{u} \cdot \pmb{n}) dS
$$<br>
Therefore, \eqref{eq:SaffmanSect3-2-15} seems to hold only if $\nabla \cdot \pmb{u}=0$. He is not explicit about this.

<hr>
$$
\begin{align}
  \int \nabla^2 \pmb{u} dV = - \int (\hat{\pmb{n}} \cdot \nabla) \pmb{u} dS 
\end{align}
$$

<hr>
Saffman p.49 Sect.3.2. Eq.5:
$$
\begin{align}
  \int \omega_i (\pmb{x}) d\pmb{x} &= \int \partial_j (x_i \omega_j) d\pmb{x} = \int (\partial_j x_i) \omega_j + x_i \partial_j \omega_i d\pmb{x}  = \int \delta_{ij} \omega_i + x_i \partial_j \omega_j d\pmb{x} \because  \partial_j \omega_j= \text{div curl} \pmb{u}=0\\
    &= \int_S x_i (\pmb{\omega} \cdot \pmb{n}) dS \because \text{Gauss's theorem}
\end{align}
$$