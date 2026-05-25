---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Sequential Spaces]], [[Continuous Functions and Homeomorphims]], [[Separable, First and Second Countable Spaces]]

**Def:** A topological space $X$ is a *Fréchet-Uryshon space* if for each $A \subseteq X$, and every $x \in \text{cl}(A)$, there's a sequence $(x_n)_{n \in \Bbb N}$ in $A$, that converges to $x$. 

**Obs:** We see that every first countable space is a Fréchet-Uryshon space. 

**Obs:** Every Fréchet-Uryshon space is sequential. 

This property is hereditary.

We have an equivalent, characterisation of being Fréchet-Uryshon. For any subset $S\subseteq X$ is not closed iff for every $x \in (\text{cl}_X\, S)\setminus S$, there's a sequence in $S$ that converges to $x$.

**Prop:** If $X$ is a Fréchet-Urysohn and $f:X \to Y$ is a continuous pseudo-open function, then $Y$ is also a Fréchet-Urysohn space.