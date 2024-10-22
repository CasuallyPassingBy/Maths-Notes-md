---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Bases, Subbases, and Local Basis for Topological Spaces]], [[Topological Subspaces]]

When we have a topological space $(X, \tau)$ and $E \subseteq X$, we can define the points that sticked to $E$, as
- A point $x \in X$ is a limit point of $E$ if for every neighbourhood $N$ of $x$ on $(X, \tau)$ has a different point of $E$ from $x$. Meaning, $x$ is a limit point of $E$, if $(E \cap N)\setminus\{x\} \ne \varnothing$ for all $N \in {\cal N}(x)$. 
- The set of all limit points of $E$ is usually denoted as $E'$ or $\text{Lim}(E)$.
- A point $x\in E$ is an isolated point of $E$, if $x \in E\setminus \text{Lim}(E)$ 

For subsets $A, B$ of the topological space $(X, \tau)$, then the following are true:
- $\text{Lim}(\varnothing) = \varnothing$
- If $A \subseteq B$, then $\text{Lim}(A) \subseteq \text{Lim}(B)$ 
- If $x \in \text{Lim}(A)$, then $x \in \text{Lim}(A\setminus\{x\})$ 
- $\text{Lim}(A \cup B) = \text{Lim}(A) \cup \text{Lim}(B)$

A subset $E$ of a topological space $(X, \tau)$ is closed iff $\text{Lim}(E)\subseteq E$

### Closure of a Set

The closure of a subset $E$ of a topological space $(X, \tau)$, is the subset $\text{cl}(E):= E \cup \text{Lim}(E)$, sometimes it is denoted as $\overline E$, but means the same thing

Let $(X, \tau)$ is a topological space, and $E, F \subseteq X$. Then the following is true:
- $x \in \text{cl}(E)$ iff for every neighborhood of $x$, $N$, then $N \cap E \ne \varnothing$
- $\text{cl}(E)$ is closed
- If $F\subseteq X$ is a closed set that contains $E$, then $\text{cl}(E)\subseteq F$
- $E$ is closed iff $E = \text{cl}(E)$
- $\text{cl}(E) = \bigcap\{F \subseteq X \mid F \text{ closed }\land E \subseteq F\}$ 
- $\text{cl}(E\cup F) = \text{cl}(E)\cup\text{cl}(F)$ 
- $\text{cl}(E \cap F) \subseteq \text{cl}(E)\cap \text{cl}(F)$

Let $\tau_1$ and $\tau_2$ be topologies of $X$, and let $A$ be a subset of $X$. If $\tau_1 \subseteq \tau_2$, then
- $\text{Lim}_{\tau_2}(A) \subseteq \text{Lim}_{\tau_1}(A)$
- $\text{cl}_{\tau_2}(A) \subseteq \text{cl}_{\tau_1}(A)$ 

Let $Y$ be a subspace of $X$. For any $E\subseteq Y$ we have that
- $\text{Lim}_Y(E) = \text{Lim}_X(E)\cap Y$ 
- $\text{cl}_Y(E) = \text{cl}_X(E) \cap Y$ 