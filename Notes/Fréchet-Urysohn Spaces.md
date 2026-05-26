---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Sequential Spaces]], [[Continuous Functions and Homeomorphims]], [[Separable, First and Second Countable Spaces]], [[Standard, Analytic, Lusin, and Souslin Spaces]]

**Def:** A topological space $X$ is a *Fréchet-Uryshon space* if for each $A \subseteq X$, and every $x \in \text{cl}(A)$, there's a sequence $(x_n)_{n \in \Bbb N}$ in $A$, that converges to $x$. 

**Obs:** We see that every first countable space is a Fréchet-Uryshon space. 

**Obs:** Every Fréchet-Uryshon space is sequential. 

**Obs:** This property is hereditary.

We have an equivalent, characterisation of being Fréchet-Uryshon. For any subset $S\subseteq X$ is not closed iff for every $x \in (\text{cl}_X\, S)\setminus S$, there's a sequence in $S$ that converges to $x$.

**Prop:** If $X$ is a Fréchet-Urysohn and $f:X \to Y$ is a continuous pseudo-open function, then $Y$ is also a Fréchet-Urysohn space.

**Prop:** The product of two Fréchet-Urysohn may not be Fréchet-Urysohn again. 

**Th:** A space $X$ is a Fréchet-Urysohn space iff every subspace of $X$ is a sequential space. 

**Prop:** Every quotient space of a Fréchet-Urysohn space is a sequential space.

**Obs:** We know there are spaces that are Fréchet-Urysohn that aren't sequential. 

# Arens' Space

**Def:** The Arens' space is the set $X = [0,\omega] \cup (\omega\times \omega)$ with the open neighbourhoods defined according to the following conditions:
- the points in $\omega\times\omega$ are isolated;
- The neighbourhoods at each $n<\omega$ are of the form $$B_{n, m} := \{n\} \cup \{(n ,j) \in \omega\times\omega\mid j \ge m\}$$for some $m <\omega$;
- The neighbourhoods at $\infty$ are obtained by removing $X$ finitely many $B_{n, 1}$ and by removing finitely many isolated points in each of the remaining $B_{n, 1}$ 

The Arens' space is also known as $S_2$.

**Prop:** $S_2$ is the canonical example of a sequential space that is not a Fréchet-Urysohn space.

**Th:** Let $X$ be a sequential space. Then $X$ is a Fréchet-Urysohn space iff $X$ doesn't contain a copy of $S_2$. Meaning, that if $X$ is a sequential space that is not a Fréchet-Urysohn space, then $X$ contains a copy of $S_2$. 

**Obs:** Let $C$ be a convergence sequence along with the limit point. We consider $C$ as a subspace of the real line. The sequential fan $S(\omega)$ is the quotient space obtained by the topological sum of countably many and infinitely many copies of $C$ with the limits points identified as one point called $\infty$. The convergent sequence $C$, is a compact metric space, in particular, it is a Fréchet-Urysohn space. The sequential fan $S(\omega)$, being a closed image of a metric space, is a Lašnev space, in particular, a Fréchet-Urysohn space. It is well known that $C\times S(\omega)$ is not a Fréchet-Urysohn space. We do this by finding a subspace that is homeomorphic to the Arens' space. 

**Prop:** The product of first countable space and a Fréchet-Urysohn space can fail to be a $k_1$-space, thus not even sequential. 