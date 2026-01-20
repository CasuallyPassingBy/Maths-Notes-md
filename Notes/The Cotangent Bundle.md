---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Tangent Bundle]], [[Dual Vector Spaces]], [[Vector Bundles on Smooth Manifolds]], [[Tangent Space for Manifolds]], [[Exterior Algebra]], [[Vector Bundles on Smooth Manifolds]]

**Def:** Let $M$ be a smooth manifold and a $p$ a point in $M$. The *cotangent space* of $M$ at $p$, denoted by $T_p^* M$ or $T_*(M)$, is defined to be the dual space of the tangent space $T_p M$. $$ T_p ^*M := (T_p M)' = \text{Hom}(T_p M, \Bbb R) = \mathcal L(T_p M, \Bbb R).$$An element of the cotangent space $T_p^*M$ is called a *covector at $p$*. Thus a covector $\omega_p$ at $p$ is a linear function $\omega_p: T_p M \to \Bbb R$. 

**Def:** The underlying set of the *cotangent bundle* $T^*M$ of a manifold $M$ is the union of the cotangent space at all points in $M$: $$T^*M := \coprod_{p \in M} T_p^*M.$$It has a natural projection $\pi: T^*M \to M$ sending $\omega\in T^*_p M$ to $p\in M$. Given any smooth local coordinates $(x^i)$ on an open subset $U\subseteq M$, for each $p\in U$ we denote the basis for $T^*_p M$ dual to $(\partial/\partial x^i|_p)$ by $(dx^i)$. This defined $n$ maps $dx^1, \dots, dx^n: U \to T^* M$ called *coordinate covector fields.*

**The Cotangent Bundle as a Vector Bundle:** Let $M$ be a smooth $n$-manifold with or without boundary. With this standard projection map and the natural vector space structure on each fibre, the cotangent bundle $T^*M$ has a unique topology and smooth structure making it into a smooth rank-$n$ vector bundle over $M$ for which all coordinate covector fields are smooth local sections.

If $(x^i)$ are smooth coordinates on an open subset $U\subseteq M$, we have that the map from $\pi^{-1}[U]$ to $\Bbb R^{2n}$ given by $$\xi_i dx^i|_p \mapsto (x^1(p),\dots, x^n(p),\xi_1,\dots, \xi_n) $$is a smooth coordinate chart for $T^*M$. We called $(x^i, dx^i)$ the *natural coordinates for $T^*M$* associated with $(x^i)$. 

**Prop:** For any smooth manifold $M$, then $T^*M$ is a trivial vector bundle iff $TM$ is trivial.

**Prop:** Suppose $F: M \to N$ is a diffeomorphism, and let $dF^*: T^* N\to T^*M$ be the map whose restriction to each cotangent space $T_q^*N$ is equal to $dF_{F^{-1}(q)}^*$, then $dF^*$ is a smooth bundle homomorphism.

**Prop:** Let $\sf Diff_1$ be the category whose objects are smooth manifolds, but whose only morphisms are diffeomorphism; and let $\sf VB$ be the category whose objects are smooth vector bundles and whose morphisms are smooth vector bundle homomorphisms. Then, the assignment $M \mapsto T^*M$, $F\mapsto dF^*$ defined a contravariant functor from $\sf Diff_1$ to $\sf VB$ called the *cotangent functor.*


# Exterior Powers

**Def:** Let $M$ be a manifold of dimension $n$. We mimic the construction of the tangent and the cotangent bundles and form the set $${\textstyle\bigwedge}^{\!k} (T^*M) := \coprod_{p \in M} {\textstyle\bigwedge}^{\!k} (T_p^*M)$$of all alternating $k$-tensors at all points in the manifold $M$. This set is called the $k$th *exterior power* of the cotangent bundle. There is a projection $\pi: {\textstyle\bigwedge}^{\!k} (T^*M)\to M$ by $\pi (\alpha) = p$ if ${\textstyle\bigwedge}^{\!k} (T_p^*M)$. 

If $(U, \phi)$ is a coordinate chart on $M$, then there's a bijection $$
\begin{align*}
{\textstyle\bigwedge}^{\!k} (T^*U) = &\coprod_{p \in U} {\textstyle\bigwedge}^{\!k} (T_p^*U) \simeq \phi[U] \times \Bbb R^{n \choose k} \\
& \alpha \in {\textstyle\bigwedge}^{\!k} (T_p^*U)\mapsto (\phi(p), \{c_I(\alpha)\}_I),
\end{align*}
$$where $\alpha = \sum c_I(\alpha) dx^I\rvert_p \in {\textstyle\bigwedge}^{\!k} (T_p^*U)$ and $I \in \mathcal I_{k, n}$. In this way we can give ${\textstyle\bigwedge}^{\!k} (T^*U)$ and hence ${\textstyle\bigwedge}^{\!k} (T^*M)$ a topology and even a differentiable structure. The projection map $\pi: {\textstyle\bigwedge}^{\!k} (T^*M) \to M$ is a smooth vector bundle of rank ${n \choose k}$. 