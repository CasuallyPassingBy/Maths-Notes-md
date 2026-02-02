---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Integration on Riemannian Manifolds]], [[Densities on Vector Spaces]], [[Local and Global Sections of Vector Bundles]], [[Orientations of Smooth Manifolds]], [[Integration on Riemannian Manifolds]], [[Riemannian Volume Form on Smooth Manifolds]], [[Divergence Theorem in R2]], [[Gauss's Theorem and Divergence in R3]], [[Scalar Line Integral]], [[Scalar Surface Integral]]

**Def:** Let $M$ be a smooth manifold with or without boundary. The set $$\mathcal DM := \coprod_{p\in M} \mathcal D(T_p M) $$is called the *density bundle of $M$*. Let $\pi: \mathcal D M \to M$ be the natural projection map taking each element fo ${\cal D}(T_p M)$ to $p$, $\mathcal D(T_p M)$ represents the vector spaces of densities of $T_p M.$

**Prop:** If $M$ is a smooth manifold with or without boundary, its density bundle is a smooth line bundle over $M$. 

**Def:** If $M$ is a smooth $n$-manifold with or without boundary, a section of ${\cal D}M$ is called a *density on $M$* We can also call such s a section a *density field* to distinguish it from a density on a vector space.

**Obs:** If $\mu$ is d density and $f$ is a continuous real-valued function, then $f\mu$ is again a density, which is smooth if both $f$ and $\mu$ are.

**Def:** A density on $M$ is said to be positive or negative if its value at each point has that property. Any nonvanishing $n$-form $\omega$ determines a positive density $|\omega|$, defined by $|\omega|_p = |\omega_p|$ for each $p\in M$. 

**Obs:** If $\omega$ is a nonvanishing $n$-form on an open subset $U\subseteq M$, then any denstity on $U$ can be written $\mu = f |\omega|$ for some real-valued function $f$.

**Prop:** If $M$ is a smooth manifold with or without boundary, there exists a smooth positive density on $M$.

Under smooth maps, densities pull back in the same ways as differential forms. 

**Def:** If $F: M \to N$ is a smooth map between $n$-manifolds with or without boundary and $\mu$ is a density on $N$, we define a density $F^*\mu$ on $M$ by $$(F^*\mu)_p(v_1,\dots, v_n) = \mu_{F(p)}(dF_p (v_1),\dots, dF_p(v_n)).$$
**Prop:** Let $G: P \to M$ an $F:M \to N$ be smooth maps between $n$-manifolds with or without a boundary, and let $\mu$ be a density on $N$.
- For any $f\in {\cal C}^\infty(N)$, $F^*(f\mu) = (f \circ F) F^*\mu$.
- If $\omega$ is a smooth $n$-form on $N$, then $F^*|\omega| = |F^*\omega|$.
- If $\mu$ is smooth, then $F^*\mu$ is a smooth density on $M$.
- $(F \circ G)^*\mu = G^*(F^*\mu)$. 

**Prop:** Suppose $F: M \to N$ is a smooth map between $n$-manifolds with or without boundary. If $(x^i)$ and $(y^i)$ are smooth coordinates on open subsets $U \subseteq M$ and $V\subseteq N$, respectively, and $u$ is a continuos real-valued function on $V$, then the following holds true on $U \cap F^{-1}[V]$: $$F^*(u\;|dy^1\wedge\dots \wedge dy^n|) = (u \circ F) \left|\det\left(\frac{\partial F_i}{\partial x^j}\right) \right| |dx^1\wedge\dots \wedge dx^n|. $$
**Cor:** If $(U, (x^i))$ and $(V, (y^i))$ are overlapping smooth coordinate charts on $M$. then the following identity holds on $U\cap V$: $$|dy^1\wedge \dots \wedge dy^n| = \left|\det\left(\frac{\partial y^i}{\partial x^j}\right)\right| \; |dx^1\wedge\dots \wedge dx^n|.$$
# Integration

**Def:** If $D\subseteq \Bbb R^n$ is a domain of integration and $\mu$ is a density on $\overline D$, we can write $\mu = f |dx^1\wedge \dots\wedge dx^n|$ for some uniquely determined continuous function $f: \overline D \to \Bbb R$. We define the *integral of $\mu$ over $D$* by $$\int_D \mu := \int_D f\; dV, $$or more suggestively, $$\int_D f \; |dx^1\wedge\dots\wedge dx^n| := \int_D f \; dx^1\cdots dx^n.  $$
Similarly, if $U$ is an open subset of $\Bbb R^n$ or $\Bbb H^n$ and $\mu$ is compactly supported in $U$, we define $$\int_U \mu := \int_D \mu, $$where $D$ is any domain of integration containing the support of $\mu$.

**Prop:** Suppose $U$ and $V$ are open subsets of $\Bbb R^n$ or $\Bbb H^n$, and $G: U \to V$ is a diffeomorphism. If $\mu$ is a compactly supported density on $V$, then$$\int_V \mu = \int_U G^* \mu. $$
**Def:** If $\mu$ is a density on $M$ whose support is contained in the domain of s single smooth chart $(U, \varphi)$, the *integral $\mu$ over $M$* is defined as$$\int_M \mu := \int_{\varphi^{-1}[U]} (\varphi^{-1})^* \mu.  $$This extend to arbitrary densities $\mu$ by setting $$\int_M \mu = \sum_i \int_M \psi_i \mu,  $$where $\{\psi_i\}$ is a smooth partition of unity subordinate to an open cover of $M$ by smooth charts. 

**Prop:** The definition of $\int_M \mu$ given above doesn't depend on the choice of open cover or partition of unity.

**Properties of Integral of Densities:** Suppose $M$ and $N$ are smooth $n$-manifolds with or without boundary, and $\mu$, $\nu$ are compactly supported densities on $M$.
- *Linearity:* If $a, b\in \Bbb R$, then $$\int_M a\mu + b\nu  = a \int_M \mu + b\int_M \nu. $$
- *Positivity:* If $\mu$ is a positive density, the $\int_M \mu > 0$.
- *Diffeomorphism Invariance:* If $F: N \to M$ is a diffeomorphism, then $$\int_M \mu  =\int_N F^*\omega.$$

**Cor:** Suppose $E$ and $M$ are smooth $n$-manifolds with or without boundary, and $\pi: E \to M$ is a smooth $k$-sheeted covering map or generalised covering map. We have that $$\int_E \pi^*\mu = k\int_M \mu  $$whenever $\mu$ is a compactly supported density on $M$.

**Remark:** A smooth density on a manifold defines an integral over compactly supported densities and over sufficiently regular domains. From the point of view of measure theory, this yields a finitely additive content on a class of “nice” sets. By extending this content via standard measure-theoretic constructions (e.g. Carathéodory’s extension theorem), one obtains a $σ$-additive Radon measure on the Borel σ-algebra of $M$.

In this text, we work exclusively at the level of densities and their integrals, and do not require this extension.

**Integrations Over Parametrizations:** Let $M$ be an smooth $n$-manifold with or without boundary, and let $\mu$ be a compactly supported density on $M$. Suppose $D_1, \dots, D_k$ are open domains of integration in $\Bbb R^n$, and for $i = 1,\dots, k$, we are given smooth maps $F_i: \overline D_i \to M$ satisfying:
- $F_i$ restricts to a diffeomorphism from $D_i$ onto an open subset $W_i \subseteq M$;
- $W_i \cap W_j = \varnothing$ when $i \neq  j$;
- $\text{supp }\mu \subseteq \bigcup_{i = 1}^k \overline W_i$. 
Then  $$\int_M \mu = \sum_{i = 1}^k \int_{D_i} F^*_i \mu. $$

## The Riemannian Density

**The Riemannian Density:** Let $(M, g)$ be a Riemannian manifold with or without boundary. There is a unique positive density $\mu_g$ on $M$, called the *Riemannian density*, with the property that $$\mu_g(E_1,\dots, E_n) = 1  $$for any local orthonormal frame $(E_i)$.

**Prop:** Let $(M, g)$ be an oriented Riemannian manifold with or without boundary and $\omega_g$ be its Riemannian volume form.
- The Riemannian density of $M$ is given by $\mu_g = |\omega_g|.$
- for any compactly supported continuous function $f: M \to \Bbb R$, then $$\int_M f\mu_g = \int_M f\omega_g.  $$

**Prop:** Suppose $(M, g)$ and $(\widetilde M, \widetilde g)$ are Riemannian manifolds with or without boundary, and $F: M \to \widetilde M$ is a local symmetry. Then $F^*\mu_{\widetilde g} = \mu_g$.

**Obs:** It is customary to denote the Riemannian density simply by $dV_g$, and to specify when necessary whether the notation refers to a density or a form. If $f: M \to \Bbb R$ is a compactly supported continuous function, the *integral of $f$ over $M$* is defined to be $$\int_M f\; dV_g.$$
**The Divergence Theorem in The Nonorientable Case:** Suppose $(M, g)$ is a nonorientable Riemannian manifold with boundary. For any compactly supported smooth vector field $X$ on $M$,  $$\int_M (\text{div }X)\; \mu_g = \int_{\partial M} \langle X, N \rangle_g \mu_{\widetilde g}, $$where $N$ is the outward-pointing unit normal vector field along $\partial M$, $\widetilde g$ is the induced Riemannian metric on $\partial M$, and $\mu_g$, $\mu_{\widetilde g}$ are the Riemannian densities of $g$ and $\widetilde g$, respectively.

**The Integration by Parts:** Let $(M, g)$ be a compact nonorientable Riemannian manifold with boundary, for any $f\in \mathcal C^\infty(M)$, $X\in {\frak X}(M)$  $$\int_M \langle \text{grad }f, X\rangle_g\; dV_g = \int_{\partial M} f\langle X, N \rangle \;dV_{\widetilde g} -\int_M (f \text{ div }X)\; dV_g.   $$where $N$ is the outward-pointing unit normal vector field along $\partial M$ and $\widetilde g$ is the induced Riemannian metric on $\partial M$. 