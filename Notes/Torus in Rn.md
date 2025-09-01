---
tags:
  - DifferentialGeometry
  - Topology
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Topology]], [[Group Theory]]
Links: [[Lie Groups]], [[Lie Group Actions]], [[Spheres in Rn]]

Let $\Bbb S^1$ be the $1$-sphere. We can define the $n$-torus as $$\Bbb T^n :=  \left(\Bbb S^1\right)^n.$$This means that $1$-sphere is the $1$-torus.

We see that the discrete Lie group $\Bbb Z^n$ acts smoothly and freely on $\Bbb R^n$ by translation. We can check the action is proper since it satisfies that for any two points $p, q\in \Bbb R^n$ have neighbourhoods $U$ and $V$ such that the set $\{\varphi\in \Bbb Z^n\mid (\varphi + U) \cap V \neq \varnothing\}$ is finite. This is because we can just make small enough balls around $p$ and $q$. 

The quotient manifold $\Bbb R^n /\Bbb Z^n$ is homeomorphic to the $n$-torus $\Bbb T^n$, and [[Lie group Actions#^2c0355|this result]] says there is a unique smooth structure on $\Bbb T^n$ making the quotient map into a smooth covering map.

We would like to verify that this smooth structure is the same as $(\Bbb S^1)^n.$ To do this we just need to check that the covering map $\Bbb R^n \to \Bbb T^n$ given by $$(x^1, \dots, x^n) \mapsto (\exp(2\pi i x^1), \dots, \exp(2\pi i x^n))$$is a local diffeomorphism with respect to the product smooth structure on $\Bbb T^n$ and makes the same identifications as the quotient map $\Bbb R^n \to \Bbb R^n /\Bbb Z^n$; thus [[Submersions, Immersions and Embeddings of Manifolds#^a3a253|this other result]] makes sure that $\Bbb R^n /\Bbb Z^n$ is diffeomorphic to $\Bbb T^n$.