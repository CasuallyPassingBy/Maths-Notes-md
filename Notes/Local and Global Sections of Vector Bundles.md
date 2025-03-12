---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Differential 1-forms on Smooth Manifolds]], [[Differential 1-forms on Smooth Manifolds]], [[Vector Fields on Smooth Manifolds]]

**Def:** A *section* of a vector bundle $\pi: E \to M$ is a map $s: M \to E$ such that $\pi \circ s = \text{id}_M$. This condition means precisely that for each $p\in M$, $s(p) \in E_p$. A *local section* of $E$ is a section $s: U \to E$ defined only on some open subset $U \subset M$. To emphasise the distinction, a section defined on all of $M$ will sometimes be called a *global section*. 

We say that a section is *smooth* if it is smooth as a map from $M$ to $E$. Similarly, we say that a section is continuous if it is continuous in the sense as a map from $M$ to $E$. We define a *rough section* of $E$ over a set $U \subseteq M$ to be a map $s: U \to E$ (not necessarily continuous) such that $\pi \circ s = \text{id}_U$. 

**Example:** The *zero section* of $F$ is the global section $\zeta: M \to E$ defined by $\zeta(p) = 0 \in E_p$ for each $p \in M$. 

**Def:** We define the *support*of a section $s$ is the closure of the set $\{p \in M \mid s(p) \neq 0 \}$. 

**Prop:** Let $s$ and $t$ be $\mathcal C^\infty$ sections of a $\mathcal C^\infty$ vector bundle $\pi: E \to M$ and let $f$ be a smooth real-valued function on $M$. Then
- the sum $s+t: M \to E$ defined by $$(s+t)(p) = s(p) + t(p) \in E_p, \qquad p \in M$$is a smooth section of $E$. 
- The product $fs: M \to E$ defined by $$(fs)(p) = f(p) s(p) \in E_p, \qquad p\in M$$is a smooth section of $E$.

**Def:** Denote the set of all smooth sections of $E$ by $\Gamma(E)$. We see that $\Gamma(E)$ is a module over the ring $\mathcal C^\infty(M)$ of $\mathcal C^\infty$ functions on $M$. For any open subset $U\subseteq M$, one can also consider the vector space over $\Bbb R$ $\Gamma(U, E)$ of smooth sections of $E$ over $U$. Then $\Gamma(U, E)$ is a both a vector space over $\Bbb R$ and a $\mathcal C^\infty(U)$-module. To contrast with sections over a proper subset $U$, a section over the entire manifold $M$ is called a *global section*. 

**Extension Lemma for Vector Bundles:** Let $\pi: E \to M$ be a smooth vector bundle over a smooth manifold $M$, and suppose $s: A \to E$ is a smooth section of $E$ defined on a closed subset $A \subseteq M$ (in the sense that $s$ extends to a smooth section in a neighbourhood of each point). For any open set $U$ containing $A$, there exists a smooth section $\tilde s \in \Gamma(M)$ such that $\tilde s|_A = s$ and $\text{supp}\;\tilde s \subseteq U$. 

## Local and Global Frames

**Def:** Let $E \to M$ be a vector bundle. If $U \subseteq M$ is an open set, local, sections $s_1, \dots, s_k$ of $E$ over $U$ are said to be *independent* if their values $s_1(p), \dots, s_k(p)$ are linearly independent elements of $E_p$ for each $p\in U$. Similarly, they are said to *span* $E$ if their values span $E_p$ for each $p \in U$. 

A *local frame* for $E$ over $U$ is an ordered $k$-tuple $(s_1, \dots, s_k)$ of independent sections over $U$ that span $E$; thus $(s_1(p), \dots, s_k(p))$ is a basis for the fiber $E_p$ for each $p\in U$. If $U =M$ ir is called a *global frame*. A frame is said to be smooth if each section $s_i$ is smooth. 

**Example:** Let $M$ be a manifold and $e_1, \dots, e_r$ the standard basis for $\Bbb R^r$. Define $\bar e_i: M \to M \times \Bbb R^r$ by $\bar e_i(p) = (p, e_i)$. Then $\bar e_1, \dots, \bar e_r$ is a smooth frame for the product bundle $M \times \Bbb R^r \to M$. 

**Example (The frame of a trivialization):** Let $\pi: E \to M$ be a smooth vector bundle of rank $r$. If $\phi: E|_U\stackrel{\sim}{\to} U \times \Bbb R^r$ is a trivialisation of $E$ over an open set $U$, then $\phi^{-1}$ carries the smooth frame $\bar e_1, \dots, \bar e_r$ of the product bundle $U \times \Bbb R^r$ to a $\mathcal C^\infty$ frame $t_1, \dots, t_r$ for $E$ over $U$: $$t_i(p) = \phi^{-1}(\bar e_i(p)) = \phi^{-1}(p, e_i), \qquad p\in U$$We call $t_1, \dots, t_r$ the smooth frame over $U$ of the trivialisation $\phi$.

**Prop:** Every smooth local frame for a smooth vector bundle is associated with a smooth local trivialisation. 

**Cor:** A smooth vector bundle is trivial iff it admits a global frame.

**Cor:** Let $\pi: E \to M$ be a smooth vector bundle of rank $k$, let $(V, \phi)$ be a smooth chart on $M$, and suppose there exists a smooth local frame $(s_1, \dots, s_n)$ for $E$ over $V$. Then the map $\tilde \phi: \pi^{-1}[V] \to \phi[V] \times \Bbb R^k$ given by $$\tilde \phi(v^i \sigma_i(p) ) = (x^1(p), \dots, x^n(p), v^1, \dots, v^k)$$is a smooth coordinate map for $E$.

**Lemma:** Let $\phi: E|_U \to U \times \Bbb R^r$ be a trivialisation over an open set $U$ of a smooth vector bundle $E \to M$ and $t_1, \dots, t_r$ the smooth frame over $U$ of the trivialization. Then a section $s = \sum b^i t_i$ of $E$ over $U$ is smooth iff its coefficients $b^i$ relative to the frame $t_1, \dots, t_r$ are smooth.

**Prop (Characterisation of smooth sections):** Let $\pi: E \to M$ be a smooth vector bundle and $U$ an open subset of $M$. Suppose $s_1, \dots, s_r$ is a smooth frame for $E$ over $U$. Then a section $s = \sum c^j s_j$ of $E$ over $U$ is smooth iff the coefficients $c^j$ are smooth functions on $U$.

**Prop:** Let $\pi: E \to M$ be a smooth vector bundle and $s_1, \dots, s_r$ a smooth frame for $E$ over $U$ in $M$. Then every $e \in \pi^{-1}[U]$ can be written uniquely as a linear combination: $$e =  c^j(e) s_j(p), \quad p = \pi(e) \in U.$$ Then, $c^j: \pi^{-1}[U] \to \Bbb R$ is smooth for $j \in \{1, \dots, n\}$.
