---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Covector Fields on Smooth Manifolds]], [[Covector Fields on Smooth Manifolds]], [[Vector Fields on Smooth Manifolds]]

**Def:** Let $\pi: E\to M$ be a vector bundle. A *section of $E$*, sometimes called a *cross section* is a section of the map $\pi$, namely, a continuous map $\sigma: M \to E$ satisfying $\pi \circ \sigma = \text{id}_M$. This means that $\sigma(p)$ is an element of the fibre $E_p$ for each $p\in M$.

A *local section of* $E$ is a continuous map $\sigma: U \to E$ defined on some subset $U \subseteq M$ satisfying $\pi \circ \sigma = \text{id}_U$. To emphasise the distinction, a section defined on all of $M$ is sometimes called a *global section*. If $M$ is a smooth manifold with or without boundary and $E$ is smooth vector bundle, a *smooth, local or global, section of $E$* is one that is a smooth map from its domain to $E$. 

We also define a *rough, local or global, section of $E$* over a set $U\subseteq M$ to be a map $\sigma: U \to E$ such that $\pi\circ \sigma = \text{id}_U$. 

The *zero section of $E$* is the global section $\zeta: M \to E$ defined by $$\zeta(p) := 0\in E_p \qquad \text{for each }p\in M. $$As in the case for vector fields, the *support* of a section $\sigma$ is the closure of the set $\{p\in M \mid \sigma(p) \neq 0\in E_p\}.$ 

**Def:** Given an immersed submanifold $S\subseteq M$ with or without boundary, a section of the ambient tangent bundle $TM|_S\to S$ is called a *vector field along $S$*. 

**Prop:** Let $s$ and $t$ be $\mathcal C^\infty$ sections of a $\mathcal C^\infty$ vector bundle $\pi: E \to M$ and let $f$ be a smooth real-valued function on $M$. Then
- the sum $s+t: M \to E$ defined by $$(s+t)(p) = s(p) + t(p) \in E_p, \qquad p \in M$$is a smooth section of $E$. 
- The product $fs: M \to E$ defined by $$(fs)(p) = f(p) s(p) \in E_p, \qquad p\in M$$is a smooth section of $E$.

**Prop:** Suppose $M$ is a compact smooth manifold and $E\to M$ is a smooth vector bundle of rank $k$. $E$ admits a smooth section $\sigma$ with the following property:
- If $k >\dim M$, then $\sigma$ is nowhere vanishing
- If $k \le \dim M$, then the set of points where $\sigma$ vanishes is a smooth compact codimension-$k$ submanifold of $M$.
The proof of this fact uses [[Transversailty Theorems for Smooth Manifolds|transversality]]. 

**Cor:** If $M$ is a compact smooth manifold, then $M$ admits a smooth vector field with only finitely many singular points.

**Def:** Denote the set of all smooth sections of $E$ by $\Gamma(E)$. We see that $\Gamma(E)$ is a module over the ring $\mathcal C^\infty(M)$ of $\mathcal C^\infty$ functions on $M$. For any open subset $U\subseteq M$, one can also consider the vector space over $\Bbb R$ $\Gamma(U, E)$ of smooth sections of $E$ over $U$. Then $\Gamma(U, E)$ is a both a vector space over $\Bbb R$ and a $\mathcal C^\infty(U)$-module. To contrast with sections over a proper subset $U$, a section over the entire manifold $M$ is called a *global section*. 

**Extension Lemma for Vector Bundles:** Let $\pi: E \to M$ be a smooth vector bundle over a smooth manifold $M$ with or without boundary. Suppose $A$ is a closed subset of $M$, and $\sigma: A \to E$ is a section of $E|_A$ that is smooth in the sense that $\sigma$ extends to a smooth local section to $E$ in a neighbourhood of each point. For each open subset $U\subseteq M$ containing $A,$ there exists a global smooth section $\tilde\sigma\in \Gamma(E)$ such that $\tilde \sigma|_A = \sigma$ and $\text{supp }\tilde \sigma \subseteq U$. 

**Extension Lemma for Sections of Restricted Bundles:** Suppose $M$ is a smooth manifold, $E\to M$ is a smooth vector bundle, and $S\subseteq M$ is an embedded submanifold with or without boundary. For any smooth section $\sigma$ of the restricted bundle $E|_S \to S$, there exists a neighbourhood $U$ of $S$ in $M$ and a smooth section $\tilde\sigma$ of $E|_U$ such that $\sigma = \tilde\sigma|_S$ If $E$ has a positive rank, then every smooth section of $E|_S$ extends smoothly to all of $M$ iff $S$ si properly embedded.

## Local and Global Frames

**Def:** Let $E \to M$ be a vector bundle. If $U \subseteq M$ is an open set, a $k$-tuple of local sections $(\sigma_1, \dots, \sigma_k)$ of $E$ over $U$ are said to be *linearly independent* if their values $(\sigma_1(p), \dots, \sigma_k(p))$ are linearly independent elements of $E_p$ for each $p\in U$. Similarly, they are said to *span* $E$ if their values span $E_p$ for each $p \in U$. 

A *local frame* for $E$ over $U$ is an ordered $k$-tuple $(\sigma_1, \dots, \sigma_k)$ of linearly independent sections over $U$ that span $E$; thus $(\sigma_1(p), \dots, \sigma_k(p))$ is a basis for the fiber $E_p$ for each $p\in U$. It is called a *global frame* if $U= M$. If $E \to M$ is a smooth vector bundle, a local or global frame is *smooth frame* if each $\sigma_i$ is smooth section. We often denote a frame $(\sigma_1,\dots, \sigma_k)$ by $(\sigma_i)$. 

**Completion of Local Frames for Vector Bundles:** Suppose $\pi: E \to M$ is a smooth vector bundle or rank $k$.
- If $(\sigma_1,\dots, \sigma_m)$ is a linearly independent $m$-tuple of smooth local section of $E$ over an open subset $U\subseteq M$, with $1\le m < k$, the for each $p\in U$ there exist smooth sections $\sigma_{m+1},\dots, \sigma_k$ is defined on some neighbourhood $V$ of $p$ such that $(\sigma_1,\dots, \sigma_k)$ is a smooth local frame for $E$ over $U \cap V$.
- If $(v_1,\dots, v_m)$ is a linearly independent $m$-tuple of elements of $E_p$ for some $p\in M$, with $1\le m <k$, then there exists a smooth frame $(\sigma_i)$ for $E$ over some neighbourhood of $p$ such that $\sigma_i(p) = v_i$ for $i = 1,\dots, m$.
- If $A\subseteq M$ is a closed subset and $(\tau_1,\dots, \tau_k)$ is a linearly independent $k$-tuple of sections of $E|_A$ that are smooth in the sense that each $\tau_i$ extendos to a smooth local section of $E$ in a neighbourhood of point, then there exists a smooth local frame $(\sigma_,\dots, \sigma_k)$ for $E$ over some neighbourhood of $A$ such that $\sigma_i|_A = \tau_i$ for $i = 1,\dots, k$. 

**Example:** Let $M$ be a manifold and $e_1, \dots, e_r$ the standard basis for $\Bbb R^r$. Define $\bar e_i: M \to M \times \Bbb R^r$ by $\bar e_i(p) = (p, e_i)$. Then $\bar e_1, \dots, \bar e_r$ is a smooth frame for the product bundle $M \times \Bbb R^r \to M$. 

**Example (The frame of a trivialization):** Let $\pi: E \to M$ be a smooth vector bundle of rank $r$. If $\phi: E|_U\stackrel{\sim}{\to} U \times \Bbb R^r$ is a trivialisation of $E$ over an open set $U$, then $\phi^{-1}$ carries the smooth frame $\bar e_1, \dots, \bar e_r$ of the product bundle $U \times \Bbb R^r$ to a $\mathcal C^\infty$ frame $t_1, \dots, t_r$ for $E$ over $U$: $$t_i(p) = \phi^{-1}(\bar e_i(p)) = \phi^{-1}(p, e_i), \qquad p\in U$$We call $t_1, \dots, t_r$ the smooth frame over $U$ of the trivialisation $\phi$.

**Prop:** Every smooth local frame for a smooth vector bundle is associated with a smooth local trivialisation. 

**Cor:** A smooth vector bundle is smoothly trivial iff it admits a smooth global frame.

**Cor:** Let $\pi: E \to M$ be a smooth vector bundle of rank $k$, let $(V, \phi)$ be a smooth chart on $M$, and suppose there exists a smooth local frame $(s_1, \dots, s_n)$ for $E$ over $V$. If we define the map $\tilde \varphi: \pi^{-1}[V] \to \phi[V] \times \Bbb R^k$ given by $$\tilde \varphi(v^i \sigma_i(p) ) = (x^1(p), \dots, x^n(p), v^1, \dots, v^k),$$then $(\pi^{-1}[V],\tilde\varphi)$ 

**Def:** Suppose $(\sigma_i)$ is a smooth local frame for $E$ over some open subset $U\subseteq M$. If $\tau: M \to E$ is a rough section, the value of $\tau$ at an arbitrary point $p\in U$ can be written $\tau(p) = \tau^i(p)\sigma_i(p)$ for some uniquely determined numbers $(\tau^1(p), \dots, \tau^k(p))$. This defined $k$ function $\tau^i:U \to \Bbb R$, called the *component functions of $\tau$* with respect the local frame.

**Local Frame Criterion for Smoothness:** Let $\pi: E \to M$ be a smooth vector bundle, and let $\tau: M \to E$ be a rough section. If $(\sigma_i)$ is a smooth local frame for $E$ over an open subset $U\subseteq M$, then $\tau$ is a smooth on $U$ iff its components functions with respect to $(\sigma_i)$ are smooth. 

**Uniqueness of a Sooth Structure of $TM$:** Let $M$ be a smooth $n$-manifold with or without boundary. The topology and smooth structure on $TM$ constructed in [[The Tangent Bundle]] are the unique ones with respect to which $\pi: TM \to M$ is a smooth vector bundle with a given vector space structure on the fibres, and such that all the coordinate vector fields are smooth local sections.  

**Def:** Let $\pi: E \to M$ be a smooth vector bundle and $U$ an open subset of $M$. Suppose $s_1, \dots, s_r$ is a frame for $E$ over $U$. We can define the dual coframe $\psi^1,\dots, \psi^r$ as the sections $\phi^k: M \to E^*$ such that $\phi^i(s_j) = \delta^i_j$. This is an analogue to a dual basis. 

**Prop:** Let $\pi: E \to M$ be a smooth vector bundle and $U$ an open subset of $M$. Suppose $s_1, \dots, s_r$ is a smooth frame for $E$ over $U$, then the corresponding dual coframe $\psi^1,\dots, \psi^r$ is also smooth. 