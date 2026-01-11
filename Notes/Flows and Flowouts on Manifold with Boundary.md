---
tags:
  - DifferentialGeometry
  - OrdinaryDifferentialEquations
---
Subjects: [[Differential Geometry]], [[Ordinary Differential Equations]]
Links: [[Integral Curves, Flows and Flowouts on Smooth Manifolds]], [[Existence and Uniqueness of Solutions to Systems of Differential Equations]], [[Vector Fields on Smooth Manifolds]], [[Tangent Space for Manifolds]], [[Homotopy]]

**Boundary Flowout Theorem:** Let $M$ be a smooth manifold with nonempty boundary, and let $N$ b a smooth vector field $M$ that is inward pointing at each point of $\partial M$. There exists a smooth function $\delta: \partial M \to \Bbb R^+$ and a smooth embedding $\Phi: {\cal P}_\delta\to M$, where $${\cal P}_\delta := \{(t, p) \mid p\in \partial M, 0 \le t < \delta(p)\} \subseteq \Bbb R\times \partial M,$$such that $\Phi[{\cal P}_\delta]$ is a neighbourhood of $\partial M$, and for each $p\in \partial M$ the map $t \mapsto \Phi(t, p)$ is an integral curve of $N$ a starting at $p$. 

**Def:** Let $M$ be a smooth manifold with boundary. A neighbourhood of $\partial M$ is called a *collar neighbourhood* if it is the image of a  smooth embedding $[0, 1) \times \partial M \to M$ that restricts to the obvious identification $\{0\} \times \partial M \to \partial M$. 

**Collar Neighbourhood Theorem:** If $M$ is a smooth manifold with nonempty boundary, then $\partial M$ has a collar neighbourhood. 

**Th:** Let $M$ be a smooth manifold with nonempty boundary, and let $\iota: \text{Int }M \hookrightarrow M$ denote the inclusion. There exists a proper smooth embedding $R: M \to \text{Int }M$ such that $\iota \circ R: M \to M$ and $R\circ \iota: \text{Int }M\to \text{Int }M$ are smoothly homotopic maps. Therefore, $\iota$ is a homotopy equivalence.

The theorem above gives us a generalisation of the [[The Whitney Approximation Theorem]]. 

**Whitney Approximation for Manifold with Boundary:** If $M$ and $N$ are smooth manifolds with boundary, then every continuous map from $M$ to $N$ is homotopic to a smooth map.

