---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Cardinal Functions of Topological Spaces]]

**Def:** A family $\cal N$ of subsets of a topological space $X$ is a *network* for $X$ if for every point $x\in X$ and any $U \in\tau_X$ with $x\in U$ there exists an $M\in \cal N$ such that $x\in M \subseteq U$. 

Clearly, any base of $X$ is a network for $X$: it is a network of a special kind, namely, all members of which are open. The family of all one-point subsets of a space is another example of a network. 

**Def:** The *network weight* of a space $X$ is defined as the smallest cardinal number of the form $|\mathcal N|$, where $\cal N$ is a network for $X$; this cardinal number is denoted by $nw(X)$. Clearly, for every topological space $X$, we have $nw(X) \le w(X)$ and $nw(X) \le |X|$.

**Def:** Just as we can have a $\sigma$-locally finite base, a base that is the countable union of locally open families, we can generalise this to $\sigma$-locally finite network, meaning that it is a network that is the countable union of locally finite families. If a space has a $\sigma$-locally finite network it is called a *$\sigma$-space*. 

**Obs:** We see, by Nagata-Smirnov, that every metric space is $\sigma$-space. 

# Network Weight

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

# $k$-networks

**Def:** A collection $\scr P$ of closed subsets of a topological space $X$ is said to be a $k$-network for $X$ if, given any open set $U$ and any compact $K \subseteq U$, there is a finite subcollection ${\scr Q} \in [{\scr P}]^{<\omega}$ so that $K \subseteq \bigcup {\scr Q}\subseteq U$. We can also have the stronger version $\sigma$-locally finite $k$-network as a $k$-network that is the union of locally finite closed families.

