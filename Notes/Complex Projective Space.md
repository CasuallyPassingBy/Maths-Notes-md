---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Real Projective Space]], [[Homogeneous Spaces in the Case of Lie groups]]

**Def:** *Complex projective $n$-space*, denoted by $\Bbb{CP}^n$, is the set of $1$-dimensional complex linear subspaces of $\Bbb C^{n+1}$, with the quotient topology inherited from the natural projection $\pi: \Bbb C^{n+1}\setminus\{0\} \to \Bbb {CP}^n$.  

If we restrict the natural quotient map to $\Bbb S^{2n+1}$, then the quotient map $\pi: \Bbb S^{2n+1} \to \Bbb{CP}^n$ is known as the *Hopf map*. If we identify $\Bbb S^{2n+1}$ as subspace of $\Bbb C^{n+1}$. Additionally, we can see that $\Bbb S^{2n+1}/\Bbb S^1$ is diffeomorphic to $\Bbb{CP}^n$, where $\Bbb S^1$ is the set of unit complex numbers. This proves that $\Bbb{CP}^n$ is a $2n$-dimensional smooth compact manifold. 

**Prop:** We see that the natural action of $\text U(n+1)$ on $\Bbb C^{n+1}$, actually is transitive on $\Bbb S^{2n+1}$, thus it descends into a transitive action on $\Bbb{CP}^n$, so $\Bbb{CP}^n$ is a homogeneous $\text U(n+1)$-space. 

# As CW Complex

If we consider the the usual inclusion $\Bbb C^{k+1} \subseteq \Bbb C^{n+1}$ for $k<n$, this allows us to consider $\Bbb{CP}^k$ as a subspace of $\Bbb{CP}^n$. Then $\Bbb{CP}^n$ has a CW decomposition with one cell in each even dimension $0, \dots, 2n$ such that the $2k$-skeleton is $\Bbb{CP}^k$ for $0 < k < n$. 

**Homology:** Complex projective $n$-space $\Bbb{CP}^n$ has CW decomposition with one cell in each even dimension, $0,\dots, 2n$. It follows from [[Singular Homology of CW complexes#^cf2f30|this]] theorem that $H_{2k} (\Bbb {CP}^n) \cong \Bbb Z$ for $k = 0,\dots, n$, and the odd-dimensional homology groups vanish.
