---
layout: post
section-type: post
title: LaTeX in Jekyll
category: documentation
tags: [ 'internal' ]
---
One can use $\LaTeX$ in Jekyll $\vec{\omega}=\nabla \times \vec{u}$.
Simply, use \$...\$ for inline and \$\$...\$\$ for block.

E.g.-
$
\begin{aligned}
  \phi(x,y) &= \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
                 = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j)  \\
            &= (x_1, \ldots, x_n) \left( \begin{array}{ccc}
              \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
              \vdots & \ddots & \vdots \\
              \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
              \end{array} \right)
            \left( \begin{array}{c}
              y_1 \\
              \vdots \\
              y_n
            \end{array} \right)
\end{aligned}
$

E.g. Maxwell's equations
$
\begin{align}
  \nabla\times\vec{\mathbf{B}}-\frac{1}{c}\frac{\partial\vec{\mathbf{E}}}{\partial t} &= \frac{4\pi}{c}\vec{\mathbf{j}} \\
  \nabla\cdot\vec{\mathbf{E}} &= 4\pi\rho \\
  \nabla\times\vec{\mathbf{E}}+\frac{1}{c}\frac{\partial\vec{\mathbf{B}}}{\partial t} &= \vec{\mathbf{0}} \\
  \nabla\cdot\vec{\mathbf{B}} &= 0
\end{align}
$

$$
\begin{align*}
  \dot{x} &= \sigma(y - x) \\
  \dot{y} &= \rho x - y - xz \\
  \dot{z} &= -\beta z + xy
\end{align*}
$$


<h4>Configuration</h4>
1. Add the following lines in `_includes/head.html`.

{% highlight py linenos %}
  <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
  </script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML" type="text/javascript"></script>
{% endhighlight %}


Sources:
[Add LaTeX support to your blog](https://hw311.me/en/jekyll/2019/01/23/support-latex-in-jekyll-blog/)

