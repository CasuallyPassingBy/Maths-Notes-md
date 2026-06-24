---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Laplacian Operator on Riemannian Manifolds]], [[Differential Forms on Smooth Manifolds]], [[The Exterior Derivative on Smooth Manifolds]], [[Integration on Riemannian Manifolds]]

**Def:** Let $(M, g)$ be an oriented compact Riemannian $n$-manifold. For each $0\le p\le n$, the *Laplace-Beltrami operator* or *Laplace-de Rham operator* $\Delta: \Omega^p(M) \to \Omega^p(M)$ is the linear map defined by $$\Delta \omega = d d^*\omega+ d^*d\omega,$$where $d^*$ is the codifferential. A smooth form $\omega\in \Omega^p(M)$ is said to be *harmonic* if $\Delta \omega = 0.$

**Prop:** The following statements are equivalent for any $\omega\in \Omega^p(M)$.
- $\omega$ is harmonic.
- $d\omega = 0$ and $\delta\omega= 0$, which we can call that $\omega$ is closed and co-closed
- $d\omega = 0$ and $\omega$ is the unique smooth $p$-form in its [[The de Rham Cohomology Groups|de Rham cohomology]] class with minimum norm $\|\omega\| = \langle\!\langle \omega,\omega \rangle\!\rangle^{1/2}$. 

**Prop:** Let $(M, g)$ be an oriented Riemannian manifold, and let $\Delta = dd^*+ d^*d$ be Laplace-Beltrami operator on $p$-forms. When $p = 0$, we see that $\Delta$ agree with the geometric Laplacian $\Delta u = -\text{div}(\text{grad }u)$.