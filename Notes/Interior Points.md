---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Limit Points and Closure]], [[Bases, Subbases, and Local Basis for Topological Spaces]], [[Topological Subspaces]]

Let $E$ be a subset of a topological space $(X, \tau)$. The interior of $E$, denoted as $\text{int}(E)$; is the union of all open subsets contained in $E$; $\text{int}(E):=\bigcup\{U \in \tau \mid U \subseteq E\}$. The points in $\text{int}(E)$ are called the interior points of $E$.

For any subset $E$ of a topological space $(X, \tau)$, then
- $\text{int}(E)$ is an open subset of $X$
- $\text{int}(E)$ is the biggest open subset contained in $E$; i.e., if $A$ is open and $A \subseteq E$, then $A \subseteq \text{int}(E) \subseteq E$.
- If $A \subseteq B \subseteq X$, then $\text{int}(A) \subseteq \text{int}(B)$
- $E \in \tau$ iff $\text{int}(E) = E$

Let $(X, \tau)$ be a topological space, and $A, B$ and $E$ are subsets of $X$. Then
- $\text{int}(X) = X$
- $\text{int}(E) \subseteq E$
- $\text{int}(\text{int}(E)) = \text{int}(E)$ 
- $\text{int}(A\cap B) = \text{int}(A) \cap \text{int}(B)$ 
- $\text{int}(A)\cup \text{int}(B) \subseteq \text{int}(A\cup B)$ 

For any subset $E$ of a topological space $(X, \tau)$, $\text{int}(E) = X \setminus \text{cl}(X\setminus E)$; which is equivalent to $\text{cl}(E) = X\setminus \text{int}(X\setminus E)$ 

Let $(X, \tau)$ be a topological space $E$ and $E\subseteq X$. 
- The *exterior* of $E$, denoted by $\text{ext}(E)$, is the set of the interior points of $X\setminus E$. Meaning we get that $\text{ext}(E) = \text{int}(X\setminus E)$ .
- A point $x \in X$ is a *boundary point of* $E$ if for any neighbourhood $N$ of $x$, satisfies $V\cap E \ne \varnothing$ and $V\setminus E \ne \varnothing$ 
- The *boundary* of $E$, can be denoted as $\partial E$, $\text{bd}(E)$ or $\text{fr}(E)$, is the set of all boundary points. In analysis it is often used $\partial E$, while in general topology maybe it is used the notations $\text{bd}(E)$ or $\text{fr}(E)$

We get the following properties about the exterior of sets, in the topological space $(X, \tau)$:
- $\text{ext}(\varnothing) = X$
- $\text{ext}(E) \subseteq X\setminus E$
- $\text{ext}(E) = \text{ext}(X\setminus \text{ext}(E))$
- $\text{ext}(A\cup B )= \text{ext}(A) \cap \text{ext}(B)$ 

We get a couple properties of the boundary of sets, in the topological space $(X, \tau)$:
- $\text{bd}(\varnothing) = \varnothing$
- $\text{bd}(E) = \text{bd}(X\setminus E)$
- $\text{bd}(\text{bd}(E)) \subseteq \text{bd}(E)$ 
- $\text{bd}(A \cap B) \subseteq [\text{cl}(A) \cap \text{fr}(B)] \cup [\text{fr}(A) \cap \text{cl}(B)]$ 

For a subset $E$ of the topological space $(X, \tau)$, then the following are true:
- $\text{ext}(E) = X \setminus \text{cl}(E)$
- $\text{cl}(E) = X \setminus \text{ext}(E)$ 
- $\text{ext}(E) \cap \text{int}(E) = \text{ext}(E) \cap \text{bd}(E) = \text{int}(E) \cap \text{bd}(E) = \text{int}(E) \cap \text{cl}(X\setminus E) =$$\text{cl}(E) \cap \text{ext}(E) = \varnothing$   
- $\text{cl}(E) \cap \text{bd}(E) = \text{cl}(X\setminus E) \cap \text{bd}(E) = [X \setminus \text{int}(E)]\cap [X\setminus \text{ext}(E)] = \text{bd}(E)$ 
- $\text{cl}(E) = E \cup \text{bd}(E)$
- $\text{int}(E) = E \setminus \text{bd}(E)$ 
- $\text{int}(E) \cup \text{bd}(E) = \text{ext}(E) = X$

Let $\tau_1$ and $\tau_2$ be topologies of $X$, and let $A$ be a subset of $X$. If $\tau_1 \subseteq \tau_2$, then
- $\text{int}_{\tau_2}(A)\supseteq \text{int}_{\tau_1}(A)$ 
- $\text{ext}_{\tau_2}(A)\supseteq \text{ext}_{\tau_1}(A)$ 
- $\text{bd}_{\tau_2}(A) \subseteq \text{bd}_{\tau_1}(A)$ 

Let $Y$ be a subspace of $X$. For any $E\subseteq Y$ we have that
- $\text{int}_X(E) \cap Y \subseteq \text{int}_Y(E)$
- $\text{bd}_Y(E) \subseteq \text{bd}_X(E) \cap Y$ 
