---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Manifolds]], [[Vector Fields on Smooth Manifolds]]

We define $\Bbb S^n := \{x\in \Bbb R^{n+1} \mid \|x\| = 1\}$. 

Additionally, we can see that $\Bbb B^n := \{x\in \Bbb R^n \mid \|x\| < 1\}$ and $\bar{\Bbb B}^n := \{x\in \Bbb R^n \mid \|x\| \le 1\}$, then we get that $\partial \bar{\Bbb B}^n = \Bbb S^{n-1}$, and $\text{Fr}_{\Bbb R^n}(\Bbb B^n) = \Bbb S^{n-1}$. 

We can see that the [[Quotient Topology#Cones|cone]] $C\Bbb S^n  \cong \bar{\Bbb B}^{n+1}$

Let $N = (0, \dots, 0, 1)$ be the 'north pole' in $\Bbb S^n$, and let $S = -N$ be the 'south pole'. We define the *stereographic projection* $\sigma: \Bbb S^n\setminus\{N\} \to\Bbb R^n$ by $$\sigma (x^1, \dots, x^{n+1}) = \frac{(x^1, \dots, x^n)}{1-x^{n+1}}.$$And let $\tilde \sigma: \Bbb S^n\setminus\{S\}\to \Bbb R^n$ as $\tilde \sigma(x) = -\sigma(-x)$. 

For any $x\in \Bbb S^n \setminus \{N\}$, then $\sigma(x)$ is the point where the line through $N$ and $x$ intersects the linear subspace where $x^{n+1} = 0$, identified with $\Bbb R^{n}$. Similarly, $\tilde \sigma(x)$ is the point where the line through $S$ and $x$ intersects the same subspace. We call $\tilde \sigma$ the *stereographic from the south pole*.

We see that $\sigma$ is bijective, and $$\sigma^{-1}(u^1, \dots, u^n) = \frac{(2u^1, \dots, 2u^n, \|u\|^2-1)}{\|u\|^2+1}.$$
We see that the atlas consisting of two charts $(\Bbb S^n \setminus\{N\},\sigma)$ and $(\Bbb S^n\setminus\{S\}, \tilde \sigma)$ defines a smooth structure on $\Bbb S^n$. The coordinates defined by $\sigma$ or $\tilde \sigma$ are called *stereographic coordinates*. 

We can show that for $\Bbb S^{2n-1} \subseteq \Bbb R^{2n}$ we can define a smooth nowhere vanishing vector field. First, we need to consider a natural identification with $\Bbb C^n$. With this in mind, for every $z\in \Bbb S^{2n-1}$ we define the path $\gamma_z(t) := e^{it}z$. Now, we define the vector field $X_z := \gamma_z'(0)$. We can show it is smooth, and nowhere vanishing by considering $\Bbb S^{2n-1}$ as an embedded submanifold of $\Bbb C^n$. 

We can show that the unit [[Quaternions|quaternions]] are diffeomorphic to $\Bbb S^3$. 

# CW Complexes

- We will construct a regular cell decomposition of $\Bbb S^n$. Since $\Bbb S^0$ is a finite discrete space is already a regular $0$-dimensional cell complex with two cells. We will proceed by induction. Let us suppose that we have constructed a regular cell decomposition of $\Bbb S^n$ with two cells in each dimension. Now consider $\Bbb S^n$ as a subspace of $\Bbb S^{n+1}$ (the subset where $x_{n+2} = 0$), we can see that the open upper and lower hemispheres of $\Bbb S^{n+1}$ are regular $n$-cells whose boundaries lie in $\Bbb S^{n}$. We get the regular cell decomposition of $\Bbb S^n$ with exactly two cells in each dimension $0$ through $n$. Lastly, for $k\le n$, the $k$-skeleton of this complex of $\Bbb S^k$. 
- We can decompose $\Bbb S^n$ in another way, with only one $0$-cell and $n$-cell and no others. The $0$-cell is the north pole $N= (0,\dots, 0, 1)$, and the characteristic map for the $n$-cell is map $q:\bar {\Bbb B}^n\to \Bbb S^n$ which collapses $\partial \bar{\Bbb B}^n$. 

 We can continue the construction how we can obtain $\Bbb S^{n+1}$ from $\Bbb S^n$ by attaching two $(n+1)$-cells. If we continue this process inductively, we obtain a finite dimensional CW complex $\Bbb S^\infty = \bigcup_{n <\omega} \Bbb S^n$, with two cells of every dimension. It contains every $\Bbb S^n$ as a skeleton. 

 We can think of $\Bbb S^\infty$ as a [[Direct Limits|direct limit]] of all spheres. 