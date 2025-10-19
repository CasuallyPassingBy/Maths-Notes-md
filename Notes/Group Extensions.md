---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]], [[Normal Subgroups and Quotient Groups]], [[Group Homomorphisms and Isomorphisms]]

**Def:** A group $G$ is said to be the extension of the group $N$ by a group $M$ if $G$ has a normal subgroup $H \trianglelefteq G$ isomorphic it $N$ such that the quotient $G/H$ is isomorphic to $M$. It is common to use this notation: 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
     1\arrow[r] & H\arrow[r, hook]\arrow[d, "\simeq"] & G\arrow[r]& G/H\arrow[r]\arrow[d, "\simeq"] & 1 \\
     & N && M &
   \end{tikzcd}
\end{document}
```

This means that the class $\sf Sol$ of solvable groups is closed under subgroups, quotients and extensions, but $\sf Ab$ is closed under subgroups and quotients, but not extensions, since $S_3$ has as a normal subgroup $A_3$ which is cyclic, and $S_3/A_3$ is of order $2$, so it is abelian, but $S_3$ is not abelian. 