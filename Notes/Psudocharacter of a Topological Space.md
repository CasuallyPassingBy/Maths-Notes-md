---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Bases, Subbases, and Local Basis for Topological Spaces]], [[Weight and Character of Topological Spaces]]

**Def:** Let $X$ be a $T_1$ space. The *pseudocharacter of a point $x\in X$* is defined as the smallest cardinal of the form $|\mathcal U|$, where $\mathcal U \subseteq \tau_X$ and $\bigcap \mathcal U = \{x\}$; this cardinal is denoted by $\psi(x, X)$. Additionally, the *pseudocharacter of $X$* is defined as $$
\psi(X) := \sup\{\psi(x, X) \mid x\in X\}.
$$
**Obs:** Let $X$ be $T_1$ space. Note that for every $x\in X$, then it is satisfied that $\psi(x, X) \le \chi(x, X)$, and $\psi(X) \le \chi(X)$.

**Prop:** If $X$ is a $T_0$ space, and has a $G_\delta$ diagonal, then $\psi(X) = \omega$. 

**Prop:** If $X$ is a $T_2$ compact space, then $\psi(x, X) = \chi(x, X)$ and $\psi(X) = \chi(X)$.