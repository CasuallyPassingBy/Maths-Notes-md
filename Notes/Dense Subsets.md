---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Compactness in Metric Spaces]]

A subset of $A$ of $X$ is called *dense in* $X$ if $\overline A= X$, i.e. if for all $x\in X$ there's a sequence $(a_n)$ in $A$ such that $a_k \to x$ in $X$. 

We also have the following equivalences:
- $D$ is dense in $X$
- If $U \subseteq X$ is an nonempty open subset of $X$, then $U\cap D\ne \varnothing$
- The only closed subset of $X$, that contains $D$ is $X$ itself
- The difference $X\setminus D$ has an empty interior in $X$

Let $D$ be a dense subset of $X$, and $f:X\to Y$ being continuous and surjective, then $f[D]$ is dense in $Y$ (on metric spaces)

Let $X$ be topological space. Then if $Z \subseteq Y \subseteq X$ and $Z$ is dense in $X$ then $Y$ is dense in $X$

Let $D$ be a dense subset of $X$ and let $f, g:X\to Y$ be continuous functions such that they match on $D$, meaning ($f|_D = g|_D$), then $f=g$ (on metric spaces)

This actually tells us that the continuous real functions from the reals, are uniquely determined by their values on the rational functions

We add that if a topological space has dense subset that is also countable, then we call that space *separable*. The $\Bbb R^n$ are separable, since $\Bbb Q^n$ are dense and countable

We can also define something similar to $\Bbb Q$ of the reals to one of $\ell^p$ spaces, meaning let $\Bbb Q^\infty$ be defined as follows:
$$
\Bbb Q^\infty := \{q_\bullet \in \ell^\infty \mid  \text{Im }q_\bullet \subseteq \Bbb Q, \exists K \forall k \ge K \in \Bbb N[q_k= 0]\}
$$
This set is countable and dense in $\ell^p$ for $p \in [1,\infty)$, thus $\ell^p$ is separable for $p \in [1,\infty)$

A discrete topological spaces is separable iff it is countable

Every compact metric space is separable

