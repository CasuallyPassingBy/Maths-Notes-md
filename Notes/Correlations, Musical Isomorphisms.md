---
tags:
  - CliffordAlgebra
---
Subjects: [[Clifford Algebra]]
Links: [[Bilinear Forms]], [[Quadratic Forms]]

**Def:** Let $V$ be a finite dimensional $K$-vector space, and $V'$ represents its dual. If $\tau: V \to V'$ is a linear function, then we call $\tau$ a *correlation*. A correlation $\tau$ naturally defines a bilinear functional $B: V \times V \to K$ by the equation $$B(v, u) := \tau(v) u \qquad \forall u, v\in V.$$If $\ker \tau = \{0\}$, the correlation is said to be *non-degenerate*. In this case the vector space $V$ and the bilinear form associated with $\tau$ are also said to be non-degenerate. 

**Prop:** Let $\tau$ be a correlation, and $B$ the associated bilinear form. $B$ is non-degenerate iff for each $v\in V\setminus\{0\}$ there's a $u\in V\setminus\{0\}$ such that $B(v, u) \neq 0$.

Since $\dim V = \dim V'$, then if a correlation $\tau$ is non-degenerate, then $\tau$ is an isomorphism between $V$ and $V'$.

# Quadratic and Symplectic Spaces

**Def:** A bilinear form, in this case denoted by $g$, is said to be *symmetric* if $$g(v, u) = g(u, v) \qquad \forall u,v\in V.$$The correlation $\tau$ associated with $g$ and defined by $\tau(v)(u) = g(v, u)$ satisfies $\tau(v)(u) = \tau(u)(v)$. A vector space endowed with a non-degenerate symmetric bilinear form is said to be a *quadratic space*.

**Def:** A bilinear form, in this case denoted by $\sigma$, is said to be *antisymmetric* if $$\sigma(v, u) = -\sigma(u, v) \qquad \forall u,v\in V.$$The correlation $\tau$ associated with $\sigma$ satisfies $\tau(v)(u) = -\tau(u)(v)$. A vector space endowed with a non-degenerate antisymmetric bilinear form is said to be a *symplectic space*.

**Def:** If $g(v, u) =0$, the vectors $v$ and $u$ are said to be *orthogonal* with respect to $g$, when $g$ is non-degenerate. A non-trivial vector $v$ can be orthogonal to itself, namely, $g(v, v) = 0$, and such vectors are called *isotropic*. 

We see that in symplectic space every vector is isotropic.

# Musical Isomorphisms

We will only consider quadratic spaces with respect to the symmetric correlations $\tau: V \to V'$, and $\tau^{-1}: V' \to V$. Here, we shall use a notation which is much more convenient than the one we have used so far: we shall denote these correlations respectively by $$\flat: V \to V', \quad \sharp: V' \to V,$$where $\flat = \sharp^{-1}$ and $\sharp = \flat^{-1}$. Such isomorphisms are called *musical isomorphisms*. In general, the expression $$v_\flat := \flat(v)\, \qquad \alpha^\sharp := \sharp(\alpha)$$ will be used. 