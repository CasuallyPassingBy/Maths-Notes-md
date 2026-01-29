---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Singular Homology]], [[The Seifert-Van Kampen Theorem]]

We are given a space $X$ and two open subsets $U, V\subseteq X$ whose union is $X$. There are four inclusion maps 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}
& U\arrow[dr, "k"] & \\
U \cap V\arrow[ur, "i"]\arrow[dr, "j"] && X \\
&V\arrow[ur,"\ell"']&
\end{tikzcd}
\end{document}
```

**Mayer-Vietoris Theorem:** Let  be a topological space, and let $U, V$ be open subsets of  whose union is $X$. Then for each $p$ there is a homomorphism $\partial_*: H_p(X) \to H_{o-1}(U \cap V)$ such that the following sequence is exact:  $$H_p(U \cap V) \stackrel{i_* \oplus j_*}{\longrightarrow} H_p(U) \oplus H_p(V)\stackrel{k_*- l_*}{\longrightarrow}H_p(X)\stackrel{\partial_*}{\longrightarrow} H_{p-1}(U\cap V)$$
