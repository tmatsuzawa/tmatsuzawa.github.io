---
layout: post
section-type: post
title: Notes on angular momentum in fluids
category: professional
published: false
tags: [ 'tech']
---
Check out the notebook [here](https://mybinder.org/v2/gh/tmatsuzawa/neko/HEAD).


I deal with 3D data on daily basis. 
Imagine a MRI data organized in a 3D array. 
Cross-sectional movies are required to inspect the patients' brain.
<br>
<br>
If the data were organized well, visualizing a cross-section is not a difficult job; however,
it becomes challenging if you'd like to visualize some arbitrary cross-section.  
That was the problem I faced the other day. 
<br>
<br>
**Q. Consider a 3D scalar field with domain $\Omega \subset \mathbb{R}^3$.
How do you extract an arbitrary cross-section of the field?**

<br>
**A.**<br>
When a plane intersects with a cuboid, there is a variety of shapes
that a cross-section could be. Check out this
[link](https://ckrao.wordpress.com/2015/02/27/cross-sections-of-a-cube/).

Let $(x_0, y_0, z_0)$ be a point on the plane. The plane is given by
<br>
$$
\begin{aligned}
  ax + by + cz = ax_0 + by_0 + c z_0 \equiv.
\end{aligned}
$$
<br>
The normal of the plane is given by $(a, b, c)$. Normalize the vector as you wish.
<br>
<br>
With this equation of the plane and the eight edges, one can solve for the intersecting points. 


