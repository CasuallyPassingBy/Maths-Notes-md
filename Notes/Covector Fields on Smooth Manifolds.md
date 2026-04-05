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

Given a local coframe $(\varepsilon^i)$ over an open subset $U\subseteq M$, every rough covector field $\omega$ on $U$ can be expressed in terms of the coframe as $\omega = \omega_i \varepsilon^i$ for some functions $\omega_1,\dots, \omega_n:U\to\Bbb R$, called the *component functions of $\omega$ with respect to the given coframe*. The component functions are determined by $\omega_i := \omega(E_i)$ where $(E_i)$ is the frame dual to $(\varepsilon^i)$. 

**Coframe Criterion for Smoothness of Covector Fields:** Let $M$ be a smooth manifold with or without boundary, and let $\omega$ be a rough covector field on $M$. If $(\varepsilon^i)$ is a smooth coframe on an open subset $U\subseteq M$, then $\omega$ is smooth on $U$ iff its component functions with respect to $(\varepsilon^i)$ are smooth. 

We denote the $\mathcal C^\infty$-module of all smooth covector fields on $M$ by ${\frak X}^*(M)$. 

## Differential of a Function

**Def:** Let $f$ be a smooth real-valued function on a smooth manifold $M$ with or without boundary. We define a covector field $df$, called the *differential of $f$*, by $$df_p(v) := vf, \qquad v\in T_p M. $$
**Prop:** The differential of a smooth function is a smooth covector field. 

Let $(x^i)$ be smooth coordinates on an open subset $U\subseteq M$, and let $(\lambda^i)$ be the correspinding coordinate frame on $U$, the corresponding coframe of $(\partial/\partial x^i)$. If we write $df_p = A_i(p)\lambda^i|_p$ for some functions $A_i:U\to \Bbb R$; then $$A_i(p) = df_p\left(\left.\frac{\partial}{\partial x^i}\right\rvert_p\right) = \frac{\partial f}{\partial x^i}(p).$$This means that$$df_p = \frac{\partial f}{\partial x^i} (p)\lambda^i|_p.$$If we apply this identity to the the special case in which $f$ is one of the coordinate functions $x^j: U\to\Bbb R$, we obtain that$$dx^j|_p = \frac{\partial  x^j}{\partial x^i}(p)\lambda^i|_p  = \delta^j_i \lambda^i|_p = \lambda^j|_p.$$In other words, the *coordinate covector field $\lambda^j$ is none other than the differential $dx^j$*, which explains the notation so far used, and a nice formula for the differential of a function in terms of local coordinates $$df = \frac{\partial f}{\partial x^i} dx^i.  $$
**Prop:** Suppose $M$ is a smooth $n$-manifold, $p\in M$, and $y^1,\dots, y^k$ are smooth real valued functions defined on a neighbourhood of $p\in M$.
- If $k = n$ and $(dy^1|_p,\dots, dy^n|_p)$ is a basis for $T_p^*M$, then $(y^1,\dots, y^n)$ are smooth coordinates for $M$ in some neighbourhood of $p$.
- If $(dy^1|_p, \dots, dy^k|_p)$ is a linearly independent $k$-tuple of covectors and $k<n$, then are some function $y^{k+1},\dots, y^n$ such that $(y^1,\dots,y^n)$ are smooth coordinates for $M$ in neighbourhoods of $p$.
- If $(dy^1|_p,\dots, dy^k|_p)$ span $T_p^*M$, there are indices $i_1,\dots, i_n$ such that $(y^{i_1},\dots, y^{i_n})$ are smooth coordinates for $M$ in a neighbourhood of $p$.

**Properties of the Differential:** Let $M$ be a smooth manifold with or without boundary, and let $f, g\in {\cal C}^\infty(M)$. 
- if $a$ and $b$ are constants, then $d(af+bg) = adf+ bdg$.
- $d(fg) = fdg + gdf$.
- $d(f/g) = (gdf - fdg)/g^2$ on the set where $g\neq 0$.
- If $J\subseteq \Bbb R$ is an interval containing the image of $f$, and $h: J \to\Bbb R$ is a smooth function, then $d(h\circ f) = (h' \circ f) df$.
- if $f$ is constant, then $df = 0$.

**Functions with Vanishing Differential:** If $f$ is a smooth real-valued function on a smooth manifold $M$ with or without boundary, then $df = 0$ iff $f$ is constant on each components of $M$.

**Derivative of a Function Along a Curve:** Suppose $M$ is a smooth manifold with or without boundary, $\gamma: J\to M$ is a smooth curve, and $f: M\to \Bbb R$ is a smooth function. Then the derivative of the real-valued function $f\circ \gamma: J \to\Bbb R$ is given by $$(f\circ \gamma)'(t) := df_{\gamma(t)}(\gamma'(t)).  $$

**Prop:** For a real-valued function $f: M \to\Bbb R$, we have that $p\in M$ is a critical point of $f$ iff $df_p = 0$. 

There might be a little bit of a problem since the differential for a smooth real-valued function $f: M \to\Bbb R$ is a little ambiguous. We can think of it as the linear transformation from $df_p : T_p M\to T_{f(p)} \Bbb R$ and the covector $df_p: T_p M \to \Bbb R$, but in reality they are the same. We only need to do the canonical identification of $T_{f(p)}\Bbb R$ with $\Bbb R$. 

**Def:** Let $M$ be a smooth manifold with or without boundary and $p\in M$. Let $\ell_p$ denote the subspace of ${\cal C}^\infty(M)$ consisting of smooth functions that vanish at $p$, and let $\ell_p^2$ be the subspace of $\ell_p$ spanned by functions of the form $fg$ for some $f, g\in\ell_p$.

**Prop:** $f\in \ell_p^2$ iff in any smooth local coordinates, its first first-order Taylor polynomial at $p$ is zero. Because of this we say that a function in $\ell_p^2$ is said to *vanish to second order*. 

**Prop:** The map $\Phi: \ell_p \to T^*_p M$ by setting $\Phi(f) := df_p$. We see that restriction $\Phi$ to $\ell_p^2$ is zero, and that $\Phi$ descends to a vector space isomorphism from $\ell_p/\ell_p^2$ to $T^*_p M$. 

In some treatments of smooth manifold theory, $T^*_p M$ is defined first in this way, and the then $T_p M$ is defined as the dual space $(\ell_p/\ell_p^2)^*$. 

**Lagrange Multipliers:** Let $M$ be a smooth manifold, and let $C\subseteq M$ be an embedded submanifold that admits a global defining function $\Phi: M \to \Bbb R^k$. Let $f\in  \mathcal C^\infty(M)$, and suppose $p\in C$ is a point at which $f$ attains its maximum or minimum value among points in $C$. Them there are real numbers $\lambda_1,\dots, \lambda_k$ (called *Lagrange multipliers*) such that $$df_p = \sum_{n = 1}^k\lambda_n d\Phi^n|_p.$$
The proof of this relies on the fact $\{d\Phi^1|_p,\dots, d\Phi^l|_p\}$ forms a basis for the [[Dual Vector Spaces#^500dc6|annihilator]] of $T_p C$. A critical point of $f|_C$ must have a vanishing differential, then $d(f|_C)_p$ must be an element of the annihilator of $T_p C$ when seen as subspace of $T_pM$.

# Pullback of Covector Fields

**Def:** Let $F: M\to N$ be a smooth map between smooth manifolds with or without boundary, and let $p\in M$ be arbitrary. The differential $dF_p: T_p M \to T_{F(p)} N$ yields a dual linear map $$dF_p^*: T_{F(p)}^* N \to T_p^*M,$$called the *pointwise pullback by $F$ at $p$,* or the *cotangent map of $F$.* We see that $dF_p^*$ is characterised by  $$dF_p^*(\omega)(v) := \omega(dF_p(v)), \qquad \text{for }\omega\in T^*_{F(p)} \text{ and } v\in T_p M.$$
We see that the assignments $(M, p)\mapsto T_p^*M$ and $F\mapsto dF_p^*$ yield a contravariant functor from the category of pointed smooth manifold to the category of real vector spaces. The convention of calling elements of $T^*M$ 'covariant vectors' is particularly unfortunate.

**Def:** Given a smooth map $F: M\to N$ and a covector field $\omega$ on $N$, we define the a rough covector field $F^*\omega$ on $M$, called the *pullback of $\omega$ by $F$*, by $$(F^*\omega)_p := dF^*_p(\omega_{F(p)}). $$It acts on a vector $v\in T_p M$ by $$(F^*\omega)_p(v) := \omega_{F(p)} (dF_p(v)). $$
**Prop:** Let $F: M\to N$ be a smooth map between smooth manifold with or without boundary. Suppose $u$ is a continuous real-valued function on $N$, and $\omega$ is a covector field on $N$. Then $$F^*(u\omega) = (u\circ F)(F^*\omega). $$If in addition $u$ is smooth, then $$F^*du= d(u\circ F). $$
**Cor:** Let $p\in M$, and choose smooth coordinates $(y^j)$ for $N$ in a neighbourhood $V$ of $F(p).$ Let $U:= F^{-1}[V]$, which is a neighbourhood of $p$. We can write a covector field $\omega$ in coordinates as $\omega = \omega_j dy^j$, then $$F^*\omega =F^*(\omega_j dy^j) = (\omega_j \circ F) F^*dy^j = (\omega_j\circ F) d(y^j \circ F) = (\omega_j\circ F)dF^j.$$

**Prop:** Suppose $F: M \to N$ is a smooth map between manifold with or boundary, and let $\omega$ be a covector field on $N$. Then $F^*\omega$ is a (continuous) covector field on $M$. If $\omega$ is smooth, then so is $F^*\omega$. 

**Prop:** Suppose $F: M \to N$ is a diffeomorphism, and let $dF^*: T^* N\to T^*M$ be the map whose restriction to each cotangent space $T_q^*N$ is equal to $dF_{F^{-1}(q)}^*$, then $dF^*$ is a smooth bundle homomorphism.

**Prop:** Let $\sf Diff_1$ be the category whose objects are smooth manifolds, but whose only morphisms are diffeomorphism; and let $\sf VB$ be the category whose objects are smooth vector bundles and whose morphisms are smooth vector bundle homomorphisms. Then, the assignment $M \mapsto T^*M$, $F\mapsto dF^*$ defined a contravariant functor from $\sf Diff_1$ to $\sf VB$ called the *cotangent functor.*

## Restricting Covector Fields on Submanifold

Suppose $M$ is a smooth manifold with or without boundary, $S\subseteq M$ is an immersed submanifold with or without manifold, and let $\iota: S \hookrightarrow M$ is the inclusion map. If $\omega$ is any smooth covector field on $M$, the pullback $\iota$ yields a smooth covector field $\iota^*\omega$ on $S$. Let $v\in T_p S$ be arbitrary, and compute $$(\iota^*\omega)_p(v) = \omega_p(d\iota_p(v)) = \omega_p(v), $$since $d\iota_p: T_pS\to T_p M$ is just the inclusion map. Thus, $\iota^*\omega$ is just the restriction of $\omega$ to vectors tangent to $S$. For this reason, $\iota^*\omega$ is often called the *restriction of $\omega$ of $S$*. We see that $\iota^*\omega$ might be zero at a given point of $S$, even though considered as a *covector gield on $M$*, $\omega$ might not vanish.

To distinguish the two ways in which we might interpret the statement '$\omega$ vanishes on $S$', one usually says that *$\omega$ vanishes along $S$* or *vanishes at points of $S$* if $\omega_p = 0$ for every point $p\in S$. The weaker condition that $\iota^*\omega = 0$ is expressed by saying the *restriction of $\omega$ to $S$ vanishes*, or the *pullback of $\omega$ to $S$ vanishes.*