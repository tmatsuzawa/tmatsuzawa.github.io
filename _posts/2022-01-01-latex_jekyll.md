---
layout: post
section-type: post
title: LaTeX in Jekyll
category: documentation
tags: [ 'internal' ]
---
One can use LaTeX in Jekyll $\vec{\omega}=\nabla \times \vec{u}$.

$$
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
$$  

\\( 1/x^{2} \\)
$\( 1/x^{2} \)$
$$\( 1/x^{2} \)$$
vs


\[ \frac{1}{n^{2}} \]
$\[ \frac{1}{n^{2}} \]$
$$\[ \frac{1}{n^{2}} \]$$

\\[ \frac{1}{n^{2}} \\]

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

2. Add the following lines in `_config.yml`

{% highlight py linenos %}
kramdown:
  # Enable LaTeX via MathJax
  mathjax: true
{% endhighlight %}