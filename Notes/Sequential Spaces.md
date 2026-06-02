---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Topological Spaces]], [[Convergence of Sequences]], [[Separable, First and Second Countable Spaces]], [[Continuous Functions and Homeomorphims]], [[Fréchet-Urysohn Spaces]], [[Metric Spaces]]

We say that a topological space $X$ is *sequential*  if for every $A \subseteq X$, $A$ is not closed iff there's $x \notin A$ and a sequence $(x_n)_{n \in \Bbb N}$ contained in $A$, that converges to $x$. 

A function $f: X\to Y$, with $X$ and $Y$ topological spaces. We say that $f$ is *sequentially continuous*, if for every $(x_n)_{n\in \Bbb N}$ that converges to $x$, then $(f(x_n))_{n \in \Bbb N}$ converges to $f(x)$. 

Every continuous function is sequentially continuous.

A closed subspace of a sequential space is sequential. 

If $X$ is a sequential space, and $E\subseteq X$, then $x\in \text{cl}(E)$ iff there's a sequence on $E$ that converges to $x$

Let $f:X\to Y$ be a function between spaces $X$ and $Y$. If $X$ is sequential and $x\in X$, then $f$ is continuous on $x$ iff for every sequence $(x_n)_{n \in \Bbb N}$  on $X$ that converges to $x$ we have that $f(x_n) \to f(x)$. Meaning that in sequential spaces, sequential continuity is enough for continuity. 

A mapping $f$ of a sequential space $X$ to a topological space $Y$ is continuous if $f[\lim x_n] \subseteq \lim f[x_n]$.

**Th:** A space $X$ is a [[Fréchet-Urysohn Spaces|Fréchet-Urysohn]] space iff every subspace of $X$ is a sequential space. 

**Th:** Every quotient space of a sequential space is always sequential.

**Cor:** Every quotient space of a first countable space is a sequential space. Every quotient space of a Fréchet-Urysohn space is a sequential space.

**Def:** For any space $X$, $A\subseteq X$ is sequentially closed in $X$ if whenever $(x_n)_{n<\omega}$ is a sequence of points of $A$ and $x_n\to x$, then $x\in A$. In other words, $A$ contains all sequential limits of convergent sequences of points of $A$. 

**Obs:** A topological space $X$ is sequential if every sequentially closed subset is closed.

**Def:** Given a topological space $(X, \tau)$. Let us consider the topology $$\tau_\text{seq} := \{U \subseteq X \mid X \setminus U \text{ is sequentially closed in }X\}. $$We see that $\tau_s$ is a topology on $X$, and that it is finer that the original topology, $\tau\subseteq \tau_\text{seq}$.

**Obs:** A topological space $(X, \tau)$ is sequential iff $\tau = \tau_\text{seq}$. 

**Th:** For any space $X$, the following statements are equivalent.
- $X$ is a sequential space. 
- $X$ is a quotient of a metric space.
- $X$ is a quotient of a first countable space. 

**Prop:** The uncountable products of first countable spaces cannot be sequential. In particular, $2^{\omega_1}$ is not sequential. 

**Prop:** The product of first countable space and a Fréchet-Urysohn space can fail to be a $k_1$-space, thus not even sequential. 

**Th:** Let $X$ be a Hausdorff space in which every point is a $G_\delta$-set in $X$, meaning every singleton $\{x\}$ is a $G_\delta$-set. Then if $X$ is a $k_1$-space, then $X$ is a sequential space. 

**Prop:** Each of the following implies that $X$ is sequential.
- $X$ is a Fréchet-Urysohn space.
- $X$ is the quotient of a first countable space.
- $X$ is a $k$-space in which every point is a $G_\delta$.
- $X$ is a CW-complex.
