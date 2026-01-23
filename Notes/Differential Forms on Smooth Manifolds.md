---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Cotangent Bundle]], [[Covector Fields on Smooth Manifolds]], [[Local and Global Sections of Vector Bundles]], [[Exterior Algebra]], [[The Dual Functor and the Multicovector Functor]], [[The Tensor Bundles]], [[Derivations]]

**Def:** A section of ${\textstyle \bigwedge}^{ \!k} (T^* M)$ is called a *differential $k$-form*, or just a $k$-form; this is a continuous tensor field whose value at each point is an alternating tensor. The integer $k$ is called the *degree* of the form. We denote the space of Smooth $k$-forms by $$\Omega^k(M) := \Gamma\left({\textstyle \bigwedge}^{\! k}( T^* M)\right). $$
The wedge product of two differential forms is defined pointwise: $(\omega\wedge \eta)_p := \omega_p\wedge \eta_p$. Thus, the wedge product of a $k$-form with an $l$-form is a $(k+l)$-form. If $f$ is a $0$-form and $\eta$ is a $k$-form, we interpret the wedge product $f\wedge \eta$ to mean the ordinary product $f\eta$. If we define $$\Omega^*(M) := \bigoplus_{k = 0}^n\Omega^k(M),$$then the wedge product turns $\Omega^*(M)$ into an associative, anticommutative graded algebra. 

In any smooth chart, a $k$-form $\omega$ can be written locally as $$\omega = \omega_ I\; dx^{i_1}\wedge\dots \wedge dx^{i_k} = \omega_I \; dx^I,$$where the coefficients $\omega_I$ are continuous functions defined on the coordinate domain, and use $dx^I$ as the abbreviation for $dx^{i_1}\wedge\dots\wedge dx^{i_k}$. We are also extending Einstein's summation convention to differential forms, where it is is understood that we are summing over all increasing multi-indices.

**Obs:** A differential form $\omega$ is smooth on $U$ iff if the component functions $\omega_I$ are smooth. 

**Obs:** We can see that $dx^I$ are the elementary differential forms, and satisfy the following identity $$dx^{i_1}\wedge\dots \wedge dx^{i_k}\left(\frac{\partial}{\partial x^{j_1}}, \dots,\frac{\partial}{\partial x^{j_k}} \right) = \delta^I_J. $$Thus the component functions $\omega_I$ of $\omega$ are determined by  $$\omega_I = \omega \left(\frac{\partial}{\partial x^{i_1}}, \dots,\frac{\partial}{\partial x^{i_k}} \right)$$

**Def:** If $F: M \to N$ is a smooth map and $\omega$ is a differential form on $N$, the pullback $F^*\omega$ is a differential form on $M$, defined as for any covariant tensor field: $$(F^*\omega)_p(v_1,\dots, v_k) = \omega_{F(p)}(dF_p (v_1),\dots, dF_p(v_k)). $$

**Lemma:** Suppose $F: M \to N$ is smooth.
- $F^*: \Omega^k(N) \to \Omega^k(M)$ is linear over $\Bbb R$.
- $F^*(\omega\wedge \eta) = (F^*\omega)\wedge(F^*\eta)$.
- In any smooth chart, $$F^*(\omega_I \; dy^{i_1}\wedge\dots\wedge dy^{i_k}) = (\omega_I \circ F)\; d(y^{i_1}\circ F)\wedge \dots \wedge d(y^{i_1}\circ F).$$

**Pullback Formula for Top-Degree Forms:** Let $F: M \to N$ be a smooth map between $n$-manifolds with or without boundary. If $(x^i)$ and $(y^i)$ are smooth coordinates on open subsets $U\subseteq M$ and $V\subseteq N$, respectively, and $u$ is a continuous real-valued function on $V,$then the following golds on $U \cap F^{-1}[V]$: $$F^*(u\; dy^1\wedge\dots \wedge dy^n) = (u \circ F)\frac{\partial (F^1,\dots, F^n)}{\partial (x^1,\dots, x^n)}\; dx^1\wedge \dots \wedge dx^n.$$
**Cor:** If $(U, (x^i))$ and $(V, (y^i))% are overlapping smooth coordinate charts on $M$. then the following identity holds on $U\cap V$: $$dy^1\wedge \dots \wedge dy^n = \frac{\partial (y^1,\dots,y^n)}{\partial(x^1,\dots,x^n)}\; dx^1\wedge\dots \wedge dx^n.$$
**Def:** Interior multiplication also extends naturally to vector fields and differential forms, simply by letting it act pointwise: if $X\in {\frak X}(M)$ and $\omega\in \Omega^k(M)$, define a $(k-1)$-form $X \; \lrcorner \;\omega =i_X \omega$ by $$(X\; \lrcorner\; \omega)_p := X_p\;\lrcorner\; \omega_p. $$
**Properties of the Interior Product:** Let $X$ be a smooth vector field on $M$.
- If $\omega$ is a smooth differential form, the $i_X \omega$ is smooth.
- $i_X: \Omega^k (M) \to \Omega^{k-1}(M)$ is linear over $\mathcal C^\infty(M)$ and therefore corresponds to a [[Bundle Homomorphisms for Vector Bundles|smooth bundle homomorphism]] $i_X: {\textstyle \bigwedge}^{\!k}(T^*M) \to {\textstyle \bigwedge}^{\!k-1}(T^*M)$. 

An important operation to differential forms is the [[The Exterior Derivative on Smooth Manifolds|exterior derivative]]

**Prop:** Suppose $M$ is a smooth manifold and $X\in {\frak X}(M)$. Then the interior multiplication $i_X: \Omega^*(M) \to \Omega^*(M)$ is an antiderivation of degree $-1$ whose square is $0$. 

**Cartan's Lemma:** Let $M$ be a smooth $n$-manifold with or without boundary, and let $(\omega^1,\dots, \omega^k)$ be an ordered $k$-tuple of smooth $1$-forms on an open subset $U\subseteq M$ such that $(\omega^1|_p,\dots, \omega^k|_p)$ is linearly independent for each $p\in U$. Given smooth $1$-forms $\alpha^1,\dots, \alpha^k$ on $U$ such that $$\sum_{i = 1}^j \alpha^i \wedge \omega^i = 0,$$then each $\alpha^i$ can be written as a linear combination of $\omega^1,\dots, \omega^k$ with smooth coefficients. 

**Prop:** For each nonnegative integer $k$, there is a contravariant functor $\Omega^k: \sf Diff \to Vec_\Bbb R$, which to each smooth manifold $M$ assigns the vector space $\Omega^k(M)$ and to each smooth $F$ the pullback $F^*$. We see that the exterior derivative is a natural transformation from $\Omega^k$ to $\Omega^{k+1}$.