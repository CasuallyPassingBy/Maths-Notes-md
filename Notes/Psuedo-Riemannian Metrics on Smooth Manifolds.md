---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Riemannian Metrics on Smooth Manifolds]]

A symmetric $2$-tensor $g$ on a vector space $V$ is said to be *nondegenerate* if the linear map $\hat g: V \to V^*$ defined by $\hat g(v)(w) = g(v, w)$ is an isomorphism, or equivalently, if for every nonzero $v\in V$ there exists $w\in V$ such that $g(v, w) \neq 0$.

Just as any inner product can be transformed to the Euclidean one by switching to an orthonormal basis, every nondegenerate symmetric $2$-tensor can be transfromed by a change of basis to one whose matrix is diagonal with all entries equal to $\pm 1$. The number $r$ and $s$ of positive and negative diagonal entries, respectively, are independent of the choice of basis, a fact known as [[Bilinear Forms#Sylvester’s Law of Inertia|Sylvester's law of intertia]]. The ordered pair $(r,s)$, called the *signature of $g$*, is an invariant of $g$.

**Def:** A *psuedo-Riemannian metric* on a smooth manifold $M$ is a smooth symmetric $2$-tensor field whose value is nondegenerate at each point, with the same signature everywhere on $M$. Psuedo-Riemannian metrics with signature $(n-1, 1)$, or $(1, n-1)$ depending on the convention used, are called *Lorentz metrics*.

