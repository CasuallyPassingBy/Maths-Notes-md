---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Topological Manifolds]]

Unless, stated I consider $k \in \{0, \dots, \infty, \omega\}$ 

**Def:** We shall say that $(U, \varphi)$ and $(V, \psi)$ are $\mathcal C^k$-compatible if $U \cap V\neq \varnothing$  implies that the transition maps $\varphi\circ \psi^{-1}$ and $\psi \circ \varphi^{-1}$ are $\mathcal C^k$ functions. 

**Def:** A $\mathcal C^k$ *atlas* is a collection of charts $\{(U_\alpha, \varphi_\alpha) \mid \alpha<\kappa\}$ such that $\{U_\alpha\mid \alpha < \kappa\}$ is an open cover of  $M$, and such that for all $\alpha, \beta <\kappa$, the $(U_\alpha, \varphi_\alpha)$ and $(U_\beta, \varphi_\beta)$ are $\mathcal C^k$-compatible.

**Def:** A *differentiable* of $\mathcal C^k$ (smooth) *structure* on a topological manifold $M$ is a a family $\mathscr U = \{U_\alpha, \varphi_\alpha\}$  of coordinate neighbourhoods such that
- $\{U_\alpha\}$ is an open cover of $M$
- for any $\alpha$ and $\beta$ the neighbourhoods $U_\alpha, \varphi_\alpha$ and $U_\beta, \beta$ are $\mathcal C^\infty$- compatible
- any coordinate neighbourhood $V, \psi$ compatible with every $U_\alpha, \varphi_\alpha \in \mathscr U$ satisfies $V, \psi \in \mathscr U$.
A $\mathcal C^k$ structure is a maximal $\mathcal C^k$ atlas. 

A $\mathcal C^\infty$ manifold is a topological manifold together with a $\mathcal C^\infty$-differentiable structure. Similarly, we can define for $0 \le k < \infty$ $\mathcal C^k$ manifolds, and $\mathcal C^\omega$ manifolds . On the special case that $k = 0$, $\mathcal C^0$ manifold is a topological manifold.

**Th:** Let $M$ be a second countable Hausdorff space. If $\{V_\beta, \psi_\beta\}$ is a covering of $M$ by $\mathcal C^k$-compatible neighbourhoods, then there is a unique $\mathcal C^k$ structure on $M$ containing these neighbourhoods. The unique $\mathcal C^k$ structure is the set of all topological neighbourhoods $U, \varphi$ which are $\mathcal C^k$-compatible with every $V_\beta, \psi_\beta$. 

**Obs:** A $\mathcal C^k$ atlas determines a $\mathcal C^k$ structure on $M$

**Obs:** An open set $U$ of a $\mathcal C^k$ manifold $M$ is itself a $\mathcal C^k$ manifold, which is called an *open submanifold* of $M$. 

**Th:** Let $M$ and $N$ be $\mathcal C^k$ manifolds of dimension $m$ and $n$, respectively. Then $M\times N$ is a $\mathcal C^k$ manifold of dimension $m+n$ with $\mathcal C^k$ structured determined by coordinate neighbourhoods of the form $\{U \times V, \varphi \times \psi\}$, where $U, \varphi$ and $V, \psi$ are coordinate neighbourhoods of $M$ and $N$, respectively, and $(\varphi \times \psi)(p, q) = (\varphi (p), \psi(q))$ in $\Bbb R^{n+m} = \Bbb R^n \times \Bbb R^m$. 

