---
tags:
  - RingTheory
  - GroupTheory
---
Subjects: [[Ring Theory]], [[Group Theory]]
Links: [[Product and Coproduct of Rings]], [[Ring Homomorphisms]], [[Ring Ideals and Quotient Rings]], [[Directed Sets]], [[Direct Product of Groups]], [[Direct Limits]]

For this section $(I, \le)$ is a directed set. Let $\{A_i \mid i \in I\}$ be a collection abelian groups. 

Suppose for every pair of indices $i, j$ with $i \le j$ there is a map $\rho_{ij}: A_i \to A_j$ such that the following hold:
- $\rho_{jk}\circ \rho_{ij} = \rho_{ik}$ whenever $i\le j\le k$, and
- $\rho_ii = \text{id}_{A_i}$ for all $i\in I$.

Let $B$ be the disjoint union of all $A_i$. We define the relation $\sim$ on $B$ by $a\sim b$ iff there exists $k$ with $i, j\le k$ and $\rho_{ik}(a) = \rho_{jk}(b)$, for $a\in A_i$ and $b\in A_j$. 

Note that $\sim$ is an equivalence relation on $B$. The set of the equivalence classes is called the *direct* or *inductive limit* of the directed system $\{A_i\mid i \in I\}$, and is denoted by $\varinjlim A_i$ 

Let $\overline x$ denote the class of $x$ in $A$ and define $\rho_i: A_i \to \varinjlim A_i$ by $\rho_i(a) = \overline a$. If each $\rho_{ij}$ is injective, then so is $\rho_i$ for all $i$. 

If we assume that all $\rho_{ij}$ are group homomorphisms, For $a\in A_i$, $b\in A_j$ then the operation $$\overline a +\overline b := \overline{\rho_{ik}(a) + \rho_{jk}(b)}$$where $k$ is any index with $i, j \le k$, is well defined and makes  $\varinjlim A_i$ into an abelian group. Then $\rho_i$ are group homomorphism form $A_i$ to $\varinjlim A_i$. 

If all $A_i$ are commutative rings with $1$ and all $\rho_{ij}$ are ring homomorphisms that send $1$ to $1,$ then $\varinjlim A_i$ may likewise be given the structure of a commutative ring with $1$ such that all $\rho_i$ are ring homomorphisms. 

The direct limit has the following *universal property:* If $C$ is any abelian group such that for each $i\in I$ there is a homomorphism $\varphi_i: A_i \to C$ with $\varphi_i = \varphi_j \circ \rho_{ij}$ whenever $i\le j$, then there is a unique homomorphism $\varphi: \varinjlim A_i \to C$ such that $\varphi \circ \rho_i = \varphi_i$ for all $i\in I$. this means the the following diagram commutes for every $i, j$ such that $i \le j$:

```tikz
\usepackage{tikz-cd} 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
A_i \arrow[dd, "\rho_{ij}"']\arrow[dr, "\rho_i"']\arrow[rrd, "\varphi_i", bend left]&& \\
& \varinjlim A_i \arrow[r, dashed, "\varphi"]& C \\
A_j\arrow[ur, "\rho_j"] \arrow[rru, "\varphi_j", bend right]&&
\end{tikzcd}
\end{document}
```

