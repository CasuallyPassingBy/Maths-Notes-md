---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Continuous Functions and Homeomorphims]], [[Product Topology]], [[Separation Axioms]]

**Def:** We say that the space $X$ is *universal* for all space having a topological property $P$ if $X$ has the property $P$ and every space that has property $P$ is embeddable in $X$.

**Def:** The Tychonoff cube of weight $\kappa\ge\aleph_0$ is the space $I^\kappa$, where $I := [0, 1]$. The Tychonoff cube $I^{\aleph_0}$ is called the *Hilbert cube*. Let us note that if $\tau\le \kappa$, the the cube $I^\tau$ is embeddable in $I^\kappa$. 

**Th:** Let $\kappa \ge  \aleph_0$ be a cardinal number. The Tychonoff cube $I^\kappa$ is universal for all Tychonoff spaces of weight $\kappa$. 

**Th (van der Slot):** If a topological property $P$ is hereditary to both open and closed subsets and open subsets and is multiplicative, then if the closed interval $I$ has $P$, then all Tychonoff spaces have $P$. 

**Def:** Let $\kappa \ge  \aleph_0$ be a cardinal number. The *Cantor cube of weight* $\kappa$ is the space $2^\kappa$. The Cantor cube $2^\omega$ or $2^{\aleph_0}$ is called the *Cantor set*. 

**Th:** Let $\kappa \ge  \aleph_0$ be a cardinal number. For every $x\in 2^\kappa$, we have $\chi(x, 2^\kappa) = \kappa$. 

**Cor:** Let $\kappa \ge  \aleph_0$ be a cardinal number. For every $x\in I^\kappa$, we have $\chi(x, I^\kappa) = \kappa$. 

**Def:** Let $\kappa \ge  \aleph_0$ be a cardinal number. Let $F$ be the topological space consisting of the set $X := \{0, 1\} = 2$ and with topology $\tau := \{\varnothing, \{0\}, X\} = \{0, 1, 2\}$. We call $F$ the *Sierpiński space*. The *Alexandroff cube of weight $\kappa$* is the space $F^\kappa$. 

**Th:** Let $\kappa \ge  \aleph_0$ be a cardinal number. The Alexandroff cube $F^\kappa$ is universal for all $T_0$-spaces of weight $\kappa$. 

**Prop:** Let $E$ be the topological space, $E := \{0, 1, 2\}$ with topology $\tau = \{\varnothing, \{0\}, E\}$. If $\kappa \ge \aleph_0$ is a cardinal number, then the space $E^\kappa$ is universal for all topological spaces of weight $\kappa$ and cardinality at most $2^\kappa$. We see that every topological space is homeomorphic to a subspace of a power of $E$. 

**Th:** The product space $(J(\kappa))^\omega$ of the hedgehog $J(\kappa)$ is universal for all $T_3$ spaces of weight $\kappa \ge \omega$ and with a $\sigma$-locally finite base.

**Kowalsky's Metrization Theorem:** The product space $(J(\kappa))^\omega$ of the hedgehog $J(\kappa)$ is universal for all metrizable spaces of weight $\kappa \ge \omega$.

**Th:** The Hilbert cube $[0,1]^\omega$ is universal for all compact metrizable spaces and for all separable metrizable spaces.
