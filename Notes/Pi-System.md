---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Link: [[Filters and Ideals]]

A $\pi$-system on a set $X$ is a collection $P$ of certain subsets of $C$ such that 
- $P$ is nonempty
- If $A, B\in P$, then $A\cap B \in P$

For any nonempty family $A$ of subsets of $X$, there's a unique $\pi$-system $\mathcal I_A$, called the $\pi$*-system generated by* $A$ that is the unique smallest $\pi$-system of $X$ containing every element of $A$. It is equal to the intersection of all $\pi$-system containing $A$, and can be explicitly described as the set of all possible nonempty finite intersections of elements of $A$: 
$$\pi (A) =\{E_1 \cap E_2 \cap \dots \cap E_n\mid n \in \Bbb N^+ \land E_1, \dots, E_n \in A\} $$
and $$ \pi (A) = \bigcap\{E \subseteq \mathcal P(X) \mid E\text{ a }\pi\text{-system}, A \subseteq E\}$$
A nonempty family of sets has the finite intersection property iff the $\pi$-system it generates does contain the empty set as an element. 