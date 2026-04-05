---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Real Projective Space]], [[The Rank of a Matrix and Matrix Inverses]], [[Continuous Actions of Groups]], [[Multi-index notation]], [[Lie Group Actions]], [[General Linear Group]]

**Def:** Let $V$ be an $n$-dimensional real vector space. For any integer $0 \le k \le n$, we let $\text G_k(V)$ denote the set of all $k$-dimensional linear subspaces of $V$. We will show that $\text G_k(V)$ can be naturally given the structure of a smooth manifold of dimension $k(n-k)$. 

Let $\text G_k(\Bbb R^n)$ denote the Grassmanian of $k$-dimensional subspaces of $\Bbb R^n$. The general linear group acts transitively on $\text G_k(\Bbb R^n)$: Given two subspaces $A$ and $B$, choose bases for both subspaces and extend them to bases for $\Bbb R^n$, and then linear transformation taking the first basis to the second also takes $A$ to $B$. Now we would like to calculate the stabiliser of the subspace $\Bbb R^k \subset \Bbb R^n$. We get that $$\text{Stab}(\Bbb R ^k) = \left\{\left.\begin{pmatrix} A & B \\ 0 & D \end{pmatrix}\; \right\rvert \; A \in \text{GL}(k, \Bbb R), D \in \text{GL}(n-k.\Bbb R), B \in \mathcal M_{k \times (n-k)}(\Bbb R)\right\},$$which is easily seen to be a closed Lie group of $\text{GL}(n, \Bbb R)$. Therefore $\text G_k (\Bbb R^n)$ has a unique smooth manifold structure making the natural $\text{GL}(n, \Bbb R)$ action smooth.

With the proof above, we see that for any $V$ an $n$-dimensional real vector space and $0\le k \le n$, then $\text G_k(V)$ is a has a unique smooth structure. The smooth manifold $\text G_k(V)$ is called the *Grassmanian manifold* of $k$-planes in $V$, or simply a *Grassmanian*. In the special case $V= \Bbb R^n$, the Grassmanian $\text G_k(\Bbb R^n)$ is often denoted by the simpler notation $\text G_{k, n}$ or $\text G(k, n)$. We get that $\text G_1(\Bbb R^{n+1})$ is exactly the $n$-dimensional projective space $\Bbb {RP}^n$. 

**Prop:** Let $V$ be a finite dimensional real vector space, then the Grassmanian $\text G_k(V)$ is a compact for each $k$. This is because we can do a very similar trick as above, but instead of $\text{GL}(n,\Bbb R)$ acting transitively and smooth smoothly we consider $\text O(n)$. 

**Prop:** The set of $k$-dimensional complex linear subspaces of $\Bbb C^n$ is denoted by $\text G_k(\Bbb C^n)$. We get that $\text G_k(\Bbb C^n)$ is a compact smooth manifold making it into a compact homogeneous $\text U(n)$-space, and its dimension is $k(n-k)$. 

**Def:** Let $\Lambda_{2n}\subseteq \text{G}_{n}(\Bbb R^{2n})$ denote the set of [[Symplectic Vector Spaces|Lagrangian]] subspaces of $\Bbb R ^{2n}$. 

**Prop:** 
- We see that $\text{Sp}(2n, \Bbb R)$ acts transitively in $\Lambda_{2n}$.