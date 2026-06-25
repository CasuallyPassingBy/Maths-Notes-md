---
tags:
  - FunctionalAnalysis
---
Subjects: [[Functional Analysis]]
Links: [[Dual Vector Spaces]], [[Bounded Linear Operators]], [[Normed Vector Spaces]]

**Def:** Let $V$ be a normed vector space. Let $V^* := \mathcal B(V, \Bbb F)$ be the space of bounded functionals from $V$ to its base field. We call $V^*$ the topological dual space of $V$, and its elements are called continuous functionals.

**Obs:** In the case where $V$ is finite dimensional then dual space $V'$ (also called the algebraic dual), and $V^*$ (the topological dual) are the same.

**Obs:** We see that $V^*$ is always a Banach space. 

**Obs:** If $H$ is a [[Hilbert Spaces|Hilbert space]], then we have a natural isometric isomorphism between $H$ and $H^*.$

**Def:** Let $V$ be a normed vector space, and let $v$ and $v_0, v_1, \dots$ belong to $V$. The sequence $(v_n)_{n<\omega}$ is said to *converge weakly* to $v$ if $\varphi(v) = \lim\limits_{n\to \infty} \varphi(v_n)$ holds for each $\varphi\in V^*$. 

**Obs:** Let $V$ be a normed vector space, and let $v$ and $v_0, v_1, \dots$ belong to $V$. If $(v_n)_{n<\omega}$ converges to $v$ in norm $\left(\lim\limits_{n\to\infty}\|v_n - v\| = 0\right)$, then $(v_n)_{n<\omega}$ converges weakly to $v$. 

**Def:** Let $V$ be a normed vector space, and let $\varphi$ and $\varphi_0, \varphi_1, \dots$ belong to $V^*$. The sequence $(\varphi_n)_{n<\omega}$ is said to *converges in the weak$^*$-topology* to $\varphi$ if $\varphi(v) = \lim\limits_{n\to \infty} \varphi_n(v)$ holds for each $v\in V$. That is, convergence in the point-wise sense. In this case, we write $\varphi_n \stackrel{w^*}{\longrightarrow}\varphi$ as $n \to \infty.$This definition also applies to nets not just sequences. 

**Example:** 
- Let $(X, {\scr A}, \mu)$ be a measure space, let $p$ satisfy $1 < p <\infty$, and $q$ be its harmonic conjugate. Then the dual of $L^p(X, {\scr A},\mu)$ is isometrically isomorphic to $L^q(X, {\scr A}, \mu)$.
	- Let $1 < p<\infty$ and $q$ its harmonic conjugate, then the dual of $\ell^p$ is isometrically isomorphic to $\ell^q$. 
- Let $X$ be a locally compact Hausdorff space. Then the map that takes finite signed, or complex, regular Borel measure $\mu$ to the functional $f\mapsto \int f\, d\mu$ is an isometric isomorphism of the Banach space $M_r(X, \Bbb R)$, or $M_r(X, \Bbb C)$, onto the dual of the Banach space $\mathcal C_0(X)$, or $\mathcal C_0(X, \Bbb C)$. 
- Let $X$ be a locally compact Hausdorff space, and let $\mu$ be a regular Borel measure on $X.$ For each $f\in \mathscr L^1(X, \mathcal B(X), \mu, \Bbb F)$ define a finite signed or complex measure $\nu_f$ on $(X, \mathcal B(X))$ by means of the formula $\nu_f(A) := \int_A f\, d\mu$. Then the map $f\mapsto \nu_f$ induces a linear isometry of $L^1(X, \mathcal B(X), \mu, \Bbb F)$ onto the subspace $M_r(X, \Bbb F)$ of those $\nu$ that are absolutely continuous with respect to $\mu$. 
- Let $X$ be a compact Hausdorff space, let $\mathcal B_0(X)$ be the Baire $\sigma$-algebra on $X$, and let $\mathcal C(X, \Bbb F)$ the space of all continuous real/complex-valued functions on $X$. We see that the map that assigns to a finite signed/complex measure $\mu$ on $(X, \mathcal B_0(X))$ the functional $f\mapsto \int f\,d\mu$ is an isometric isomorphism of $M(X, \mathcal B_0(X), \Bbb F)$ onto $\mathcal C(X, \Bbb F)$. 