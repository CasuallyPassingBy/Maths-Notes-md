---
tags:
  - FunctionalAnalysis
---
Links: [[Vector Spaces]], [[Inner Products and Norms]], [[Complete Metric Spaces]], [[Lp spaces]], [[ellp spaces]], [[Bounded Linear Operators]]

**Def:** Let $(V, \langle \cdot, \cdot \rangle)$ be an inner product space, we say that the inner product is strictly positive definite if $\|v\| = 0$ iff $v = 0$.

**Def:** An inner product space where the inner product is strictly positive-definite, and is complete with the induced norm is a *Hilbert space*. If either of the conditions fail, the space is a called a *pre-Hilbert space*

We see that $\Bbb R^n$ and $\Bbb C^n$ are examples of finite dimensional Hilbert spaces.  While $\ell^2(\Bbb Z)$ and $\ell^2(\Bbb N)$ are examples of infinite dimensional Hilbert spaces. An extremely important example are the $L^2[a,b]$ spaces.

**Prop:** If $H$ is a Hilbert space and if $C$ is a nonempty closed convex subset of $C$, then there is a unique point $y\in C$ that satisfies $$\|y\| = \inf\{\|z\|\mid z\in C\}. $$
**Prop:** Let $H$ be a Hilbert space, and let $H_0$ be a closed linear subspace of $H$.If $x\in H$, then there is a unique point $y\in H_0$ such that $$\|x-y\| = \inf\{\|x-z\| \mid z\in H\},$$and for each $z\in H_0$, we know that $\langle x-y, z\rangle = 0$. 

**Prop:** Let $V$ be an inner product space, and for each $y\in V$ define $F_y:= V \to \Bbb R$ and $F_y(x) := \langle x, y\rangle$. We know that $F_y\in V^*$, $\|F_y\| = \|y\|$, and if $y\neq y'$, then $F_y \neq F_{y'}$. In addition, if $V$ is a Hilbert space and $F\in V^*$, then there is a unique element $y\in V$ such that $F = F_y$.