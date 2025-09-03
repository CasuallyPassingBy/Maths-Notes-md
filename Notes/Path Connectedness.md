---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Connectedness]], [[Continuous Functions and Homeomorphims]]

**Def:** Let $X$ be a topological space and $p,q \in X$. A *path in $X$ from $p$ to $q$* is a continuous function $f: I \to X$ such that $f(0) = p$ and $f(1) =q$, where $I = [0,  1]$. We say that $X$ is *path-connected* if every $p,q\in X$, there is a path in $X$ from $p$ to $q$. 

**Properties of Path-Connected Spaces:**
- Every continuous image of a path-connected space is path-connected
- Let $X$ be a space, and let $\{B_\alpha \mid \alpha  <\kappa\}$ be a collection of path-connected subspace of $X$ with a point in common. Then $\bigcup_{\alpha <\kappa} B_\alpha$ is path-connected.
- Every product of finitely many path-connected spaces is path-connected.
- Every quotient space of a path-connected space is path-connected.

**Th:** Path-connectedness implies connectedness.

## Components

**Def:** If $X$ is a topological space, define a *path component of $X$* to be a maximal nonempty path-connected subset

**Properties of Path Components:** Let $X$ be any space.
- The path components of $X$ form a partition of $X$.
- Each path component is contained in a single connected component, and each component is a disjoint union of path components.
- Any nonempty path-connected subset of $X$ is contained in a single path component. 

Since path-connectedness is a global property we can also [[Local Path Connectedness]]