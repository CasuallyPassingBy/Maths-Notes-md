---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Tangent Distributions and Involutivity on Smooth Manifolds]]

**Def:** Let $M$ be a smooth $n$-manifold, and let $\cal F$ be any collection of $k$-dimensional submanifolds of $M$. A smooth chart $(U, \varphi)$ for $M$ is said to be *flat for $\cal F$* if $\varphi[U]$ is a cube in $\Bbb R^n$, and each submanifold in $\cal F$ intersects $U$ in either the empty set or a countable union of $k$-dimensional slices of the form $x^{k+1} = c^{k+1}, \dots, x^n= c^n$. We define a *foliation of dimension $k$ on $M$* to be a collection $\cal F$ of disjoint, connected, nonempty, immersed $k$-dimensional submanifolds of $M$, called the *leaves of the foliation*, whose union is $M$, and such that in a neighbourhood of each point $p\in M$ there exists a flat chart for $M$. 

**Prop:** Let $\cal F$ be a foliation on a smooth manifold $M$. The collection of tangent spaces to the leaves of $\cal F$ forms an involutive distribution on $M$.

**Lemma:** Suppose $D\subseteq TM$ is an involutive distribution, and let $\{N_\alpha\}_{\alpha\in A}$ be any collection of connected integral domains of $D$ with a point in common. Then $N = \bigcup_{\alpha} N_\alpha$ has a unique smooth manifold structure making it into a connected integral manifold of $D.$ 
**Global Frobenius Theorem:** Let $D$ be an involutive distribution on a smooth manifold $M$. The collection of all maximal connected integral manifolds of $D$ forms a foliation of $M$.

**Def:** Suppose $M$ is a smooth manifold and $\Phi: M \to M$ is a diffeomorphism. A distribution $\Phi$ on $M$ is said to be *$\Phi$-invariant* if $d\Phi[D] = D$; or more precisely, if for each $x\in M$, $d\Phi_x[D_x] = D_{\Phi(x)}$. Similarly, a foliation $\cal F$ on $M$ is said to be *$\Phi$-invariant* if for each leaf $L$ of $\cal F$, the submanifold $\Phi[L]$ is also a lead on $\cal F$.

**Prop:** Let $M$ be a smooth manifold and $\Phi: M \to M$ be a diffeomorphism. Suppose $D$ is an involutive distribution on $M$ and $\cal F$ is the foliation it determines. Then $D$ is $\Phi$-invariant iff $\cal F$ is $\Phi$-invariant. 