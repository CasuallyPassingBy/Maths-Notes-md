---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Countable Tightness]]

**Def:** Let $X$ be a topological space, and let $x\in X$. The *tightness* of $X$ at $x$, denoted as $t(x, X)$, is the smallest cardinal number $\kappa$ such that whenever $x$ is in the closure of a subset $A\subseteq X$, there exists a subset $B\subseteq A$ with cardinality $|B|\le \kappa$ such that $x\in B$. The tightness of the entire space $X$, denoted as $t(X)$, is the supremum of the tightness of all of its points: $$t(X) := \sup\{t(x,X)\mid x\in X\}. $$
**Def:** We see that a countably tight space $X$ is really just $t(X) = \omega$. Note that every sequential space is countably tight.
