---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Differential forms on Smooth Manifolds]], [[Symplectic Vector Spaces]], [[The Exterior Derivative on Manifolds]]

**Def:** A *symplect form* on a smooth manifold $M$ is a smooth, closed, nondegenerate $2$-form. In other words, a smooth $2$-form is symplectic iff it is closed and $\omega_p$ is a symplectic tensor. A smooth manifold endowed with a specific choice a symplectic form is called a *symplectic manifold*. A choice of symplectic form is also sometimes called a *symplectic structure* on $M$. 

We know that a symplectic manifold must be even-dimensional. 

**Def:** If $(M, \omega)$ and $(\widetilde M, \widetilde \omega)$ are symplectic manifolds, a diffeomorphism $F: M \to \widetilde  M$ satisfying $F^*\widetilde \omega = \omega$ is called a *symplectomorphism*. 

The study of properties of symplectic manifold that are invariant under symplectomorphisms is known as *symplectic geometry*. 

**Examples:**
- If we denote the standard coordinates on $\Bbb R^{2n}$ by $(x^1,y^1\dots, x^n, y^n)$, the $2$-form$$\omega = \sum_{i = 1}^n dx^i \wedge dy^i $$is symplectic. This is called the *standard symplectic form* on $\Bbb R^{2n}$. 
- Suppose $\Sigma$ is any smooth $2$-manifold and $\Omega$ is any nonvanishing $2$-form on $\Sigma$. Then $\omega$ is closed because $d\Omega$ is a $3$-form, and every $3$-form on a $2$-manifold is zero. Moreover, every nonvanishing $2$-form is nondegenerate, so $(\Sigma, \Omega)$ is a symplectic manifold.

**Def:** Suppose $(M,\omega)$ is a symplecti manifold. An (immersed or embedded) submanifold $N\subseteq M$ is said to be symplectic, isotropic, coisotropic, or Lagrangian if $T_p N$, as a subspace of $T_p M$, has this property at each point $p\in N$. more generally, an immersion (or embedding) $F: N \to M$ is said to have one these properties if the subspace $F_*[T_p  N] \subseteq T_{F(p)} M$ has the corresponding property for every $p\in N$. Thus a manifold is symplectic, isotropic, coisotropic or Lagrangian iff its inclusion map has the same property. 