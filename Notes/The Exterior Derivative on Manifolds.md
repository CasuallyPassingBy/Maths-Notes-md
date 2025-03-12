---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Exterior Derivative on Rn]], [[Differential k-forms on Smooth Manifolds]], [[Derivations]]

**Def:** An *exterior derivative* on a manifold $M$ is an $\Bbb R$-linar map $D: \Omega^*(M) \to \Omega^*(M)$ such that:
- $D$ is an antiderivation of degree $1$
- $D\circ D =0$
- If $f$ is a smooth function and $X$ a smooth vector field on $M$, then $(Df)(X) = Xf$. 

We see that if an exterior derivative must agree with the differential $df$ of a function $f$. 

**Prop:** If $(U, x^1, \dots, x^n)$ a coordinate chart on a manifold $M$. The if an exterior derivative on $U$, the  it is uniquely defined. 

# Local Operators

**Def:** An operator $D: \Omega^*(M) \to \Omega^*(M)$ is said to be *local* if for all $k \ge 0$, whenever a $k$-form $\omega\in \Omega^k(M)$ restricts to $0$ on an open set $U$ in $M$, then $D\omega = 0$ on $U$.

An equivalent criterion for an operator $D$ to be local is that for all $k\ge 0$, whenever two $k$-forms $\omega, \tau  \in \Omega^k(M)$ agree on an open set $U$, then $D\omega = D\tau$ on $U$.

**Prop:** Any antiderivation $D$ on $\Omega^*(M)$ is a local operator.

**Def:** An operator $L: \Omega^*(M) \to \Omega^*(M)$ is a *support-decreasing* if $\text{supp} (L\omega) \subseteq \text{supp}(\omega)$ for every $\omega \in \Omega^*(M)$.

**Prop:** An operator on $\Omega^*(M)$ is local iff it is support decreasing. 

# Existence and Uniqueness of the Exterior Derivative on a Manifold

Choose a chart $(U, x^1, \dots, x^n)$ about $p$. Suppose $\omega = \sum a_I dx^I$ on $U$. There's an exterior derivative $d_U$ on $U$ with the property: $$d_U \omega = \sum da_I \wedge dx^I.$$We define $(d\omega)_p := (d_U \omega)_p$. If $(V, y^1, \dots, y^n)$ is another chart about $p$ and $\omega = \sum b_J dy^J$ on $V$ then on $U \cap V$, $$\sum a_I dx^I = \sum b_J dy^J$$there exists a unique exterior derivative $d_{U \cap V}: \Omega^*(U \cap V) \to \Omega^*(U \cap V)$. By the properties of the exterior derivative, $U\cap V$ $$d_{U\cap V}\left( a_I dx^I\right) = d_{U \cap V}\left( b_J dy^J\right)$$or $$ da_I \wedge dx^I = db_J \wedge dy^J$$thus $(d\omega)_p = (d_U \omega)_p$ is well defined, independently of the chart.

**Th:** On any manifold $M$ there exists a unique exterior derivative $d: \Omega^*(M) \to \Omega^*(M)$. Defined by if $\omega \in \Omega^k(M)$, then $\omega = \sum a_I dx^I$, $$d\omega := da_I \wedge dx^I.$$
# Pullbacks

**Commutation of the pullback with $d$:** Let $F: N \to M$ be a smooth map of manifolds. If $\omega \in \Omega^k(M)$, then $dF^*\omega = F^*d\omega$. 

**Cor:** If $U$ is an open set of a manifold $M$ and $\omega \in \Omega^k(M)$, then $(d\omega)|_U = d(\omega|_U)$.

**Prop:** If $F: N \to M$ is a smooth map of manifolds and $\omega$ is a smooth $k$-form on $M$, then $F^*\omega$ is a smooth $k$-form on $N$. 