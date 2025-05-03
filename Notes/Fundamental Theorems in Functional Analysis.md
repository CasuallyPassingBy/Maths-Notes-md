---
tags:
  - FunctionalAnalysis
---
Subjects: [[Functional Analysis]]
Links: [[Normed Vector Spaces]], [[Bounded Linear Operators]], [[Continuous Functions and Homeomorphims#^7182de|Open Functions]]

**Def:** A *seminorm* or *prenorm* on a vector space $X$ is real valued function $p:X \to \Bbb R$ such that the following conditions are satisfies by all $x, y \in X$ and $\alpha \in \Bbb F$.
- $p(\alpha x) = |\alpha| p(x).$
- $p(x+y) \le p(x) + p(y)$.
From this definition we get that $p(0) = 0$ and $p(x) \ge 0$ for all $x\in X$.

**Def:** A function $f: X \to \Bbb R^{\ge 0}$ is *countably subadditive* if $f(\sum x_n) \le \sum f(x_n)$ for every convergent series $\sum x_n$ in $X$.

**Zabreĭko's Lemma**: Every countable subadditive seminorm on a Banach space is continuous.

**Open Mapping Theorem:** Every surjective bounded linear operator from a Banach space is an open mapping.

**Cor:** Every bijective bounded linear operator from a Banach space into a Banach space is an isomorphism.

**Def:** Two norms on the same vector space are equivalent if they induce the same topology.

**Cor:** Suppose $\|\cdot \|_1$ and $\|\cdot \|_2$ are two Banach norms on a vector space $X$ and that the identity from $(X, \|\cdot \|_1)$ to $(X,\|\cdot \|_2)$ is continuous, then the two norms are equivalent.

**Def:** A family of $\mathcal F$ of linear operator from a normed space $X$ into a normed space $Y$ is said to be *pointwise bounded* if, for each element of $x\in X$, the set $\{Tx \mid T \in \mathcal F\}$ is bounded, and is said to be *uniformly bounded*, if for each bounded set $B\subseteq X$, the set $\bigcup\{T[B] \mid T\in \mathcal F\}$ is bounded. 

**The Uniform Boundedness Principle:** Let $\mathcal F \subseteq\mathcal B(X, Y)$, where $X$ is a Banach spaces and $Y$ a normed space. If $\sup\{\|Tx \| \mid T\in \mathcal F\}$ is finite for each $x\in X$, then $\sup\{\|T\| \mid T \in \mathcal F\}$ is finite. 

**Cor:** Let $(T_n)$ be a sequence of bounded linear operators from a Banach space $X$ into a normed space $Y$ such that $\lim T_n X$ exists for each $x\in X$. Define $T: X \to Y$ by the formula $Tx := \lim T_n x$. Then $T$ is a bounded linear operator from $X$ into $Y$.

**The Closed Graph Theorem:** Let $T$ be a linear operator from a Banach space $X$ into a Banach space $Y$. Suppose that whenever a sequence $(x_n)_{n <\omega}$ in $X$ converges to some $x\in X$ and $(Tx_n)_{n<\omega}$ converges to some $y\in Y$, it follows that $Tx = y$. Then $T$ is bounded.