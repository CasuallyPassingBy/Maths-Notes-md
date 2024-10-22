---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]], [[Contour Integrals in C]], [[Contour Integration over Continuous Curves]], [[Homotopy in C]]
### Deformation Theorem
Suppose $f$ is an holomorphic function on an open set $G$ and that $\gamma_0$ and $\gamma_1$ are piecewise smooth curves in $G$.

- If $\gamma_0$ and $\gamma_1$ are paths from $z_0$ to $z_1$ and are homotopic in $G$ with fixed endpoints, then
    
    $$ \int_{\gamma_0} f = \int_{\gamma_1} f $$
    
- If $\gamma_0$ and $\gamma_1$ are closed curves which are homotopic as closed curves in $G$, then
    
    $$ \oint_{\gamma_0} f = \oint_{\gamma_1} f $$
    

### Homotopy Form of Cauchy’s Theorem
Let $f$ be holomorphic on $G$, an open connected set. Let $\gamma$ be a closed curve in $G$ which is homotopic to a point in $G$. Then

$$ \oint_\gamma f = 0 $$

A way to get the same results, without having to integrate over continuous curves. Is to use the [[Homology Cauchy's Theorem]], and the results that make it so that connect homotopy to homology, with [[Logarithms of curves#Connection to Homoogy|connection to homology]] with homotopy being a stronger condition. 