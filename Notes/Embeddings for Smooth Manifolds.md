---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Submersions, Immersions and Local Diffeomorphism of Smooth Manifolds]], [[Rank and Local Normal Forms of Smooth Manifolds]], [[Continuous Functions and Homeomorphims]]

**Def:** If $M$ and $N$ are smooth manifolds with or without boundary, a *smooth embedding of $M$ into $N$* is a smooth immersion $F: M \to N$ that is also a topological embedding, i.e., a homeomorphism onto its image $F[M] \subseteq N$ in the subspace topology. Note that a smooth embedding is not just a topological embedding that happens to be smooth.

Just to emphasise, but $\text{embedding} \implies \text{immersion}$, but we can find examples of immersed manifolds that are not embedded manifolds.

**Prop:** Suppose $M$ and $N$ are smooth manifolds with or without boundary, and $F: M \to N$ is an injective smooth immersion. If any of the following holds, then $F$ is a smooth embedding.
- $M$ is compact.
- $F$ is a proper map. 
- $F$ is open or closed
- $M$ has empty boundary and $\dim M = \dim N$. 

**Local Embedding Theorem:** Suppose $M$ and $N$ are smooth manifolds with or without boundary, and $F: M \to N$ is a smooth map. Then $F$ is a smooth immersion iff every point in $M$ has a neighbourhood $U\subseteq M$ such that $F|_U: U \to N$ is a smooth embedding. 
