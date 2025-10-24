---
tags:
  - GroupTheory
  - RingTheory
---
Subjects: [[Group Theory]], [[Ring Theory]]
Links: [[Product and Coproduct of Rings]], [[Ring Homomorphisms]], [[Ring Ideals and Quotient Rings]], [[Orderings]], [[Direct Product of Groups]], [[Inverse Limits]]

In this section $(I, \le)$ is a partially ordered set, and $\{A_i \mid i\in I\}$ is a collection of abelian group.

Suppose for every pair of indices $i, j$ with $i \le j$ there is a map $\mu_{ji}: A_j \to A_i$ such that the following hold:
- $\mu_{ji} \circ \mu_{kj} = \mu_{ki}$ whenever $i \le j\le k$, and
- $\mu_{ii} = \text{id}_{A_i}$ for all $i\in I$. 

Let $P$ be the subset of elements $(a_i)_{i \in I}$ in the direct product $\prod_{i \in I} A_i$ such that $\mu_{ji}(a_j) = a_i$ whenever $i \le j$. The set $P$ is called the *inverse* or *projective limit* of the system $\{A_i \mid i\in I\}$ and is denoted $\varprojlim A_i$.

If all $\mu_{ji}$ are group homomorphisms, then $\varprojlim A_i$ is a subgroup of the direct product group. 

Let all $\mu_{ji}$ be group homomorphisms and $I = \Bbb N^+$ with the usual ordering, such that $\mu_i: \varprojlim A_i \to A_i$ be the projection of $\varprojlim A_i$ into its $i$th component. If each $\mu_{ji}$ is surjective, then so si $\mu_i$ for all $i\in I$. 

If all $A_i$ are commutative rings with $1$ and all $\mu_{ji}$ are ring homomorphisms that $1$ to $1$, then $\varprojlim A_i$ may likewise be given the structure of commutative ring with $1$ such that all $\mu_i$ are ring homomorphisms. 

The inverse limit has the following *universal property*: If $D$ is any group for each $i\in I$ there is a group homomorphism $\pi_i: D \to A_i$ with $\pi_i = \mu_{ji} \circ \pi_j$ whenever $i \le j$, then there is a unique homomorphism $\pi: D \to P$ such that $\mu_i \circ \pi = \pi$ for all $i$, meaning that the following diagram commutes: 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
&& A_j \arrow[dd, "\mu_{ji}"]\\
D \arrow[r, dashed, "\pi"]\arrow[rru, "\pi_j", bend left]\arrow[drr, "\pi_i",  bend right]& \varprojlim A_i\arrow[dr, "\mu_i"]\arrow[ur, "\mu_j"]& \\
&& A_i
\end{tikzcd}
\end{document}
```
