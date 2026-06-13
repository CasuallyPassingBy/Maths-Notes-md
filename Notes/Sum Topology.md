---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Strong Topology]], [[Product Topology]], [[Categorical Product and Coproduct]], [[Cardinal Functions of Topological Spaces]]

**Def:** Suppose we are given a family $\{X_s\mid s\in S\}$ of pairwise disjoint topological spaces; consider the set $X = \bigcup_{s\in S} X_s$ and the inclusion maps $\iota_s: X_s \to X$. We define the sum topology on $X$ to be the strong/final topology induced by the family $\{\iota_s: X_s \to X\mid s\in S\}$.  We denote the topological sum topology of $X$ as $$\bigoplus_{s\in S} X_s = \coprod_{s\in S} X_s.  $$
**Obs:** Note that we can we can consider the family $\{X_s\times \{s\}\mid s\in S\}$ of topological spaces where $X_s\times \{s\} \cong X_s$, so we can suppose the spaces to be pairwise disjoint without loss of generality.

**Prop:** A mapping $f$ of the sum $\bigoplus_{s\in S} X_s$ to a topological space $Y$ is continuous iff the composition $f\circ \iota_s$ is continuous for every $s\in S$. 

**Prop:** Let $\{X_s\mid s\in S\}$ be a family of topological spaces. We see that $U$ is an open set of $\bigoplus_{s\in S} X_s$ iff $U\cap X_s$ is open for every $s\in S$.

**Prop:** A set $A\subseteq \bigoplus_{s\in S} X_s$ is closed iff the intersection $A\cap X_s$ is closed in $X_s$ for every $s\in S$. 

**Cor:** All sets $X_s$ are clopen in $\bigoplus_{s\in S} X_s$.

**Prop:** If $\{X_s\}$ is a family of pairwise disjoint topological spaces and $A_s$ is a subspace of $X_s$ for every $s\in S$, then two topologies defined on the set $\bigcup_{s\in S} A_s$, i.e., the topology of the sum of subspaces $\{A_s\mid s\in S\}$ and the topology of the subspace of the sum $\bigoplus_{s\in S} X_s$, coincide. 

**Prop:** If a topological space $X$ can be represented as the union of a family $\{X_s\mid s\in S\}$ of pairwise disjoint open subsets, then $X := \bigoplus_{s\in S} X_s$.

**Cor:** Let $\{X_s\}$ be a family of pairwise disjoint topological spaces. If $S = \bigcup_{t\in T} S_t$, where $S_t \cap S_r = \varnothing$ for $r\neq t$, then $$\bigoplus_{s\in S} X_s = \bigoplus_{t\in T}\left(\bigoplus_{s\in S_t} X_s\right),  $$i.e., the sum of spaces is associative. 

**Def:** We say that a topological property $P$ is *additive* if for any family $\{X_s\mid s\in S\}$ of spaces with property $P$, the sum $\bigoplus_{s\in S}X_s$ also has the property $P$. Similarly, we say that a property is $\kappa$-*additive* if we add the condition that $|S|<\kappa$, and *finitely additive* if $|S| <\aleph_0$. 

**Th:** Any sum of $T_i$-spaces is a $T_i$-space for $i \le 6$. Similarly, we see that regularity and normality are additive.

**Prop:** For $X = \bigoplus_{s\in S} X_s$ we see that $w(X) = |S| \cdot \sup\{w(X_s) \mid s\in S\}$, $d(X) = |S| \cdot \sup\{d(X_s) \mid s\in S\}$, $\chi(x, X) = \chi(x, X_s)$ for some $s\in S$ such that $x\in X_s$, and $\chi(X) = \sup\{\chi(X_s) \mid s\in S\}$. 

**Obs:** We see that $w(X) \le \kappa$ and $d(X)\le \kappa$ are $\kappa$-additive, but $\chi(X) \le \kappa$ is additive.

**Obs:** Let $\kappa$ be a cardinal number. We see that the discrete space $D(\kappa)$ is homeomorphic to $\bigoplus_{\alpha<\kappa} \{\alpha\}$. 

**Def:** Suppose we are given two families $\{X_s\mid s\in S\}$ and $\{Y_s\mid s\in S\}$ of pairwise disjoint topological spaces and a family of continuous mappings $\{f_s: X_s\to Y_s \mid s\in S\}$. Letting $f(x) = f_s(x)$ for $x\in X_s$, we define a mapping $f$ of the sum $\bigoplus_{s\in S} X_s$ to the sum $\bigoplus_{s\in S}Y_s$ which is called the *sum of the mappings* $\{f_s\mid s\in S\}$ and is denoted by $\bigoplus_{s\in S} f_s$.

**Prop:** Suppose we are given two families $\{X_s\mid s\in S\}$ and $\{Y_s\mid s\in S\}$ of pairwise disjoint topological spaces and a family of continuous mappings $\{f_s: X_s\to Y_s \mid s\in S\}$. We see that $\bigoplus_{s\in S} f_s$ is closed iff all the functions $f_s$ are closed. Similarly, we see that $\bigoplus_{s\in S} f_s$ is open iff all the functions $f_s$ are open. Lastly, $\bigoplus_{s\in S} f_s$ is a homeomorphic embedding iff all of the functions $f_s$ are homeomorphic embeddings. 

**Universal Property of the Sum Topology:** Suppose we are given a family $\{X_s\mid s\in S\}$ of pairwise disjoint topological spaces and a family of continuous mappings $\{f_s: X_s \to Y\mid s\in S\}$. Then there is a unique continuous function $f: \bigoplus_{s\in S} X_s \to Y$ such that the following diagram commutes for every $s\in S$: 

```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X_s \arrow[d,hook, "\iota_s"] \arrow[dr, "f_s"] \\ 
\bigoplus_{s\in S}X_s \arrow[r, dashed, "f"] & Y

\end{tikzcd}
\end{document}
```
We see that $f = \bigcup_{s\in S} f_s$. Additionally, we see that $f$ is closed iff every every function $f_s$ is closed, and $f$ is open iff every function $f_s$ is open.

We see that the topological sum is just the [[Categorical Product and Coproduct|coproduct]] in the category $\sf Top$. 

**Prop:** We see that the space $X$ is homeomorphic to the sum $\bigoplus_{s\in S}X_s$ iff there's a family of continuous mappings $\{\iota_s: X_s\to X\mid s\in S\}$ satisfying the following conditions:
- For every space $Y$ and a pair $f, g$ of continuous functions of $X$ to $Y$, if $f\circ \iota_s = g\circ\iota_s$ for every $s\in S$, then $f= g$.
- For every space $Y$ and a family of continuous mappings $\{f_s:X_s\to Y\mid s\in S\}$ there exists a continuous mapping $f:X \to Y$ such that $f\circ \iota_s = f_s$ for every $s\in S$. 