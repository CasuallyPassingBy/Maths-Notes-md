---
tags:
  - Topology
---
Subject: [[Topology]]
Links : [[Generation of Topologies through Collection of Subsets]], [[Interior Points]], [[Limit Points and Closure]]

We can can construct a topology for a set, with a function from ${\cal P}(X)$ into itself. Then, we get the following definition

### Closure Operators

We say that the function $\eta:{\cal P}(X) \to {\cal P}(X)$ is a Kuratowski operator or a closure operator if it satisfies the following conditions, known as Kuratowski axioms:
- $\eta(\varnothing) = \varnothing$
- $\forall E\subseteq X$, we have that $E\subseteq \eta(E)$
- $\forall E\subseteq X$, we have that $\eta(\eta(E)) = \eta(E)$
- $\forall E, F\subseteq X$, we have that $\eta(E\cup F) = \eta(E) \cup \eta(F)$

If $\eta$ is a Kuratowski operator of a set $X$, then, for all $E, F \subseteq X$, then $E\subseteq F$, implies $\eta(E) \subseteq \eta(F)$

Let $X$ be a set. If $\eta:{\cal P}(X)\to {\cal P}(X)$ is a Kuratowski operator for $X$, then there's a unique topology $\tau$ on $X$ for which $\eta$ is the closure operator.

The way the proof goes, is to consider all the fixed points of the operator ${\cal F}= \{F \subseteq X \mid F = \eta(F)\}$, and we verify that this set behaves as the set of closed sets of a topology.

### Interior Operators

Let $X$ be a set. We say that the function $\eta:{\cal P}(X) \to {\cal P}(X)$ is an *interior operator* if
- $\eta(X) = X$
- $\forall E\subseteq X$ we have that $\eta(E) \subseteq E$
- $\forall E\subseteq X$ we have that $\eta(\eta(E)) = \eta(E)$
- $\forall A, B\subseteq X$ we have that $\eta(A\cap B) = \eta(A) \cap \eta(B)$

Let $\eta:{\cal P}(X) \to {\cal P}(X)$ is an interior operator defined on the set $X$. Then $A\subseteq B \subseteq X$ implies $\eta(A) \subseteq \eta(B)$

Let $X$ be a set and $\eta:{\cal P}(X) \to {\cal P}(X)$ be an interior operator over $X$. Then there's exists a unique topology $\tau$ on $X$ for which $\eta$ is an interior operator.

The way we prove this is by, is by constructing the operator $\kappa:{\cal P}(X) \to {\cal P}(X)$, defined as $\kappa(A) = X\setminus \eta(A)$, and this is Kuratowski operator, then we get the new topology


