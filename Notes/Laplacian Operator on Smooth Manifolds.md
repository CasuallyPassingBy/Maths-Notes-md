---
tags:
  - DifferentialGeometry
  - PartialDifferentialEquations
---
Subjects: [[Differential Geometry]], [[Partial Differential Equations]]
Links: [[Integration on Riemannian Manifolds]], [[Densities on Smooth Manifolds]], [[Harmonic Functions]]

**The Integration by Parts:** Let $(M, g)$ be a compact Riemannian manifold with boundary, for any $f\in \mathcal C^\infty(M)$, $X\in {\frak X}(M)$  $$\int_M \langle \text{grad }f, X\rangle_g\; dV_g = \int_{\partial M} f\langle X, N \rangle \;dV_{\widetilde g} -\int_M (f \text{ div }X)\; dV_g.   $$where $N$ is the outward-pointing unit normal vector field along $\partial M$ and $\widetilde g$ is the induced Riemannian metric on $\partial M$. 

**Def:** Let $(M,g)$ be a Riemannian manifold with or without boundary. The linear operator $\Delta: \mathcal C^\infty(M) \to \mathcal C^\infty(M)$ defined by $$\Delta u := -\text{div}(\text{grad }u)$$is called the *geometric Laplacian*. There is no general agreement about the sign convention for the Laplacian on a Riemannian manifold, and many authors define $\Delta$ to be the negative of the operator we have defined. Although the geometric Laplacian defined is the opposite of the traditional Laplacian on $\Bbb R^n$, it has two distinct advantages: our Laplacian has nonnegative eigenvalues, and it agrees with the Laplace-Beltrami operator on differential forms. When reading anything that mentions the Laplacian, we have to be careful to determine which sign convention the author is using. 

**Prop:** Let $(M,g )$ be a Riemannian manifold with or without boundary. In any smooth local coordinates $(x^i)$, then $$\Delta u = -\frac{1}{\sqrt{\det g}} \frac{\partial}{\partial x^i} \left(g^{ij} \sqrt{\det g} \frac{\partial u}{\partial u^i}\right),$$where $\det g= \det(g_{kl})$ is the determinant of the component matrix of $g$ in these coordinates.

**Def:** Let $(M, g)$ be a Riemannian manifold with or without boundary. A function $u\in\mathcal C^\infty(M)$ is said to be *[[Harmonic Functions|harmonic]]* if $\Delta u = 0$. 

**Green's Identities:** Suppose $(M, g)$ is a compact Riemannian manifold.$$\begin{align*}
\int_M u \Delta v \; dV_g &= \int_M \langle \text{grad }u, \text{grad }v\rangle_g\; dV_g- \int_{\partial M} u N v\; dV_g \\
\int_M (u \Delta v - v \Delta u) \; dV_g &= \int_{\partial M} (vNu- u Nv)\; dV_{\widetilde g},
\end{align*}   $$where $N$ is the outward-pointing unit normal vector field along $\partial M$ and $\widetilde g$ is the induced Riemannian metric on $\partial M$. Note that in the case where $\partial M = \varnothing$, this identities simplify to $$\begin{align*}
\int_M u \Delta v \; dV_g &= \int_M \langle \text{grad }u, \text{grad }v\rangle_g\; dV_g = \int_M v \Delta u \; dV_g\\
&\int_M (u \Delta v - v \Delta u) \; dV_g = 0
\end{align*} $$
**Prop:** Suppose $(M, g)$ is a compact, connected Riemannian manifold.
- If $\partial M = \varnothing$, the only harmonic functions on $M$ are the constants.
- If $\partial M \neq \varnothing$, and $u, v$ are harmonic functions on $M$ whose restriction to $\partial M$ agree, then $u = v$.

**Def:** Let $(M, g)$ be a compact connected Riemannian manifold without boundary, and let $\Delta$ be the geometric Laplacian. A real number $\lambda$ is called an *eigenvalue of $\Delta$* if there exists a smooth real-valued function $u$ on $M$, not identically zero, such that $\Delta u = \lambda u$. In this case, $u$ is called an *eigenfunction* corresponding to $\lambda$.

**Prop:** Let $(M, g)$ be a compact connected Riemannian manifold without boundary.
- $0$ is an eigenvalue of $\Delta$, and all other eigenvalues are strictly positive.
- If $u$ and $v$ eigenfunctions corresponding to distinct eigenvalues, then $\int_M uv \; dV_g = 0$. 

Note that on the space $\mathcal C^\infty(M)$, we can consider the natural inner product to be $f,g\in \mathcal C^\infty(M)$ to be$$\langle f, g\rangle := \int_M fg\; dV_g.$$With this definition in mind, we see that the eigenfunctions of $\Delta$ that have different eigenfunctions are orthogonal. We most likely we can extend this to $L^2(M)$, with the induced metric on $M$ by the density $dV_g$. We get that the Laplacian operator is self-adjoint since $$\langle\Delta u, v\rangle = \int_M v \Delta u\; dV_g = \int_M u\Delta v\; dV_g = \langle u, \Delta v\rangle. $$
**Def:** Let $M$ be a compact connected Riemannian $n$-manifold with nonempty boundary. A number $\lambda\in \Bbb R$ is called a *Dirichlet eigenvalue for $M$* if there exists a smooth real-valued function $u$ on $M$, not identically zero, such that $\Delta u = \lambda u$ and $u|_{\partial M} = 0$. Similarly, $\lambda$ is called a *Neumann eigenvalue* if there exists such a $u$ satisfying $\Delta u = \lambda u$ and $Nu|_{\partial M} = 0$, where $N$ is the outward unit normal.

**Prop:** Let $M$ be a compact connected Riemannian $n$-manifold with nonempty boundary.
- Every Dirichlet eigenvalue is strictly positive.
- $0$ is a Neumann eigenvalue, and all other Neumann eigenvalues are strictly positive.

**Dirichlet's Principle:** Suppose $M$ is a compact connected Riemannian manifold with nonempty boundary. A function $u\in \mathcal C^\infty(M)$ is harmonic iff it minimises $$\int_M |\text{grad }u|_g^2\; dV_g  $$among all smooth function with the same boundary values. 