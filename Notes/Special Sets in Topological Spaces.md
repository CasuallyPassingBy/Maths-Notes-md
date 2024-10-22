---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Interior Points]], [[Limit Points and Closure]], [[Dense Subsets]]

We can look at special sets. Let $(X, \tau)$ be a topological space:
- A set $E\subseteq X$ is *dense* in $X$, if $\text{cl}(E) =X$
- A set $E\subseteq X$ is *dense-in-itself* if for any point of $E$ is a limit point of $E$, meaning, $E \subseteq \text{Lim}(E)$
- A set $E\subseteq X$ is perfect, if $E$ is *closed* and *dense-in-itself*
- A set $E\subseteq X$ has an empty interior, meaning $\text{int}(E) = \varnothing$ 
- A set $E\subseteq X$ *nowhere dense* if $\text{int}(\text{cl}(E))= \varnothing$ 

Let $(X, \tau)$ be a topological space:
- $E\subseteq X$ is dense in $X$ iff for each $A \in \tau^+$ satisfies $A\cap E\ne \varnothing$
- The following are equivalent
	- $E\subseteq X$ has an empty interior
	- each $A\in \tau^+$ contains points of $X\setminus E$
	- $X\setminus E$ is dense in $X$
- The following are equivalent
	- $E\subseteq X$ is nowhere dense
	- $X\setminus \text{cl}(E)$ is dense in $X$
	- for any $A\in \tau^+$, there's a $\varnothing \ne B\subseteq A$ open such that $B\cap E= \varnothing$
- $E$ is perfect iff $E = \text{Lim}(E)$
- Every nowhere dense set has empty interior, and every closed set with empty interior is nowhere dense

Let $(X, \tau)$ be a topological space, that is dense-in-itself, then we have that $\text{int}\{x\} = \varnothing$, for all $x\in X$. 

For a topological space $X$ it follows that
- The union of sets that have empty interior of $X$, not necessarily have empty interior
- If $A\subseteq X$ have an empty interior, and $B\subseteq X$ is nowhere dense, then $A\cup B$ has an empty interior
- The finite union of nowhere dense subsets of $X$ is also a nowhere dense set

Let $D$ be a dense subset of the space $(X, \tau)$, and $A \in \tau$. Then $\text{cl}(A) = \text{cl}(A \cap D)$