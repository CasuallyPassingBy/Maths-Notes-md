---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Networks]], [[Weight and Character of Topological Spaces]], [[Density of a Topological Space]]

**Def:** Let $(X, \tau)$ be a topological space. We define the *network weight* of $(X, \tau)$ as$$
nw(X) = nw(X, \tau) :=\min \{|\mathcal N| \mid \mathcal N \text{ is  network for }(X, \tau) \}.
$$
**Obs:** We see that every base for $(X, \tau)$ is a network and the set $\{\{x\} \mid x\in X\}$ is also a network, then $$d(X, \tau) \le nw(X, \tau) \le \min\{w(X, \tau), |X|\}.$$
**Th:** For every [[Kolmogorov Spaces|Kolmogorov space]] we have $|X| \le 2^{nw(X)}$.   

**Prop:** If $X$ is a $T_2$ space, then there are $Y$ a $T_2$ space and $f:X \to Y$ be a continuous bijective function such that $w(Y) \le nw(X)$.

**Prop:** If $X$ is a $T_2$ compact space, then $nw(X) = w(X)$. 

**Cor:** If $X$ is a $T_2$ compact space and a has a cover $\{A_\alpha \mid \alpha <\kappa\}$ such that $nw(A_\alpha) \le \lambda \ge \omega$ for $\alpha <\kappa$ and $\kappa \le \lambda$, then $nw(X) \le \lambda$.

**Th:** For every $T_2$ compact space $X$ we have $w(X) \le |X|$

**Th:** Let $X$ and $Y$ be $T_2$ spaces. If there's a continuous surjective function $f:X \to Y$, and $Y$ is compact, then $w(Y) \le nw(X)$. 