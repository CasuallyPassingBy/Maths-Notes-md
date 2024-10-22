---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Topological Spaces]], [[Convergence of Sequences]], [[Separable, First and Second Countable Spaces]], [[Continuous Functions and Homeomorphims]]

We say that a topological space $X$ is *sequential*  if for every $A \subseteq X$, $A$ is not closed iff there's $x \notin A$ and a sequence $(x_n)_{n \in \Bbb N}$ contained in $A$, that converges to $x$. 

A function $f: X\to Y$, with $X$ and $Y$ topological spaces. We say that $f$ is *sequentially continuous*, if for every $(x_n)_{n\in \Bbb N}$ that converges to $x$, then $(f(x_n))_{n \in \Bbb N}$ converges to $f(x)$. 

Every continuous function is sequentially continuous.

A closed subspace of a sequential space is sequential. 

If $X$ is a sequential space, and $E\subseteq X$, then $x\in \text{cl}(E)$ iff there's a sequence on $E$ that converges to $x$

Let $f:X\to Y$ be a function between spaces $X$ and $Y$. If $X$ is sequential and $x\in X$, then $f$ is continuous on $x$ iff for every sequence $(x_n)_{n \in \Bbb N}$  on $X$ that converges to $x$ we have that $f(x_n) \to f(x)$. Meaning that in sequential spaces, sequential continuity is enough for continuity. 

# Fréchet-Uryshon Spaces

A topological space $X$ is a *Fréchet-Uryshon space* if for each $A \subseteq X$, and every $x \in \text{cl}(A)$, there's a sequence $(x_n)_{n \in \Bbb N}$ in $A$, that converges to $x$. 

We see that every first countable space is a Fréchet-Uryshon space. 

This property is hereditary.

We have an equivalent, characterization of being Fréchet-Uryshon. For any subset $S\subseteq X$ is not closed iff for every $x \in (\text{cl}_X\, S)\setminus S$, there's a sequence in $S$ that converges to $x$.

Every Fréchet-Uryshon space is sequential. 