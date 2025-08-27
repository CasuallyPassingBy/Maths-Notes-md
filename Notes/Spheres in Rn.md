---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth or Differentiable Manifolds]]

We define $\Bbb S^n := \{x\in \Bbb R^{n+1} \mid \|x\| = 1\}$. 

Let $N = (0, \dots, 0, 1)$ be the 'north pole' in $\Bbb S^n$, and let $S = -N$ be the 'south pole'. We define the *stereographic projection* $\sigma: \Bbb S^n\setminus\{N\} \to\Bbb R^n$ by $$\sigma (x^1, \dots, x^{n+1}) = \frac{(x^1, \dots, x^n)}{1-x^{n+1}}.$$And let $\tilde \sigma: \Bbb S^n\setminus\{S\}\to \Bbb R^n$ as $\tilde \sigma(x) = -\sigma(-x)$. 

For any $x\in \Bbb S^n \setminus \{N\}$, then $\sigma(x)$ is the point where the line through $N$ and $x$ intersects the linear subspace where $x^{n+1} = 0$, identified with $\Bbb R^{n}$. Similarly, $\tilde \sigma(x)$ is the point where the line through $S$ and $x$ intersects the same subspace. We call $\tilde \sigma$ the *stereographic from the south pole*.

