---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Cotangent Bundle]], [[Vector Fields on Smooth Manifolds]], [[Tangent Space for Manifolds]], [[Dual Vector Spaces]], [[Local and Global Sections of Vector Bundles]]

**Def:** A (local or global) section of $T^*M$ is called a *covector field* or *differential $1$-form*. Like sections of other bundles, covector fields without further qualifications are assumed to be merely continuous; when we make different assumptions, we use *rough vector field* and *smooth vector field*. In any smooth local coordinates on an open subset $U\subseteq M$, a rough covector field $\omega$ can be written in terms of the coordinate covector fields $(dx^i)$ as $\omega = \omega_i dx^i$ for $n$ functions $\omega_i: U\to\Bbb R$ called the *component functions of $\omega$*. They are characterised by $$\omega_i(p) := \omega_p\left(\left.\frac{\partial}{\partial x^i}\right\rvert_p\right).$$
If $\omega$ is a rough covector field and $X$ is a vector field on $M$, then we can form a function $\omega(X):M \to \Bbb R$ by $$\omega(X)(p) := \omega_p(X_p),\qquad p\in M. $$If we write $\omega =\omega_i dx^i$ and $X  = X^j \partial/\partial x^j$ in terms of local coordinates, then $\omega(X) = \omega_i X^i$.

**Smoothness Criteria for Covector Fields:** Let $M$ be a smooth manifold with or without boundary, and let $\omega: M \to T^*M$ be a rough covector field. The following are equivalent:
- $\omega$ is smooth.
- In every smooth coordinate chart, the component functions are smooth.
- Each point of $M$ is contained in some coordinate chart in which $\omega$ has smooth component functions.
- For every smooth vector field $X\in{\frak X}(M)$, the function $\omega(X)$ is smooth on $M$.
- For every open subset $U\subseteq M$ and every vector field $X$ on $U$, the function $\omega(X):U\to \Bbb R$ is smooth on $U$.

# Coframes

**Def:** Let $M$ be a smooth manifold with or without boundary, and let $U\subseteq M$ be an open subset. A *local coframe for $M$ over  $U$* is an ordered $n$-tiple of covector fields $(\varepsilon^1,\dots, \varepsilon^n)$ defined on $U$ such that $(\varepsilon^i|_p)$ forms a basis for $T^*_p M$ at each $p\in M$. If $U = M$, it is called a *global coframe*. 

For any smooth chart $(U, (x^i))$, the coordinate covector fields $(dx^i)$ constitute a local coframe over $U$, called a *coordinate coframe.*

**Def:** Given a local frame $(E_1,\dots, E_n)$ for $TM$ over an open subset $U$, there is a uniquely determined (rough) local coframe $(\varepsilon^1,\dots, \varepsilon^n)$ over $U$ such that $(\varepsilon^i|_p)$ is the dual basis to $(E_i|_p)$ for each $p\in U$, or equivalently $\varepsilon^i(E_j) = \delta^i_j$. This coframe is called the *coframe dual of $(E_i)$*. Conversely, if we start with the local coframe $(\varepsilon^i)$ over an open subset $U\subseteq M$, there is a uniquely determined local coframe $(E_i)$, called the *frame dual to $(\varepsilon^i)$*, determined by $\varepsilon^i(E_j) =\delta^i_j$. 

**Lemma:** Let $M$ be a smooth manifold with or without boundary. If $(E_i)$ is a rough local frame over an open subset $U\subseteq M$ and $(\varepsilon^i)$ is its dual coframe, then $(E_i)$ is smooth iff $(\varepsilon^i)$ is smooth. 

Given a local coframe $(\varepsilon^i)$ over an open subset $U\subseteq M$, every rough covector field $\omega$ on $U$ can be expressed in terms of the coframe as $\omeg