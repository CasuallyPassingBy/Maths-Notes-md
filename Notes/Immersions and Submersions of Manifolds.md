---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Functions on Smooth Manifolds]], [[Differentiability of Vector valued functions of Rn]]

**Def:** A $\mathcal C^\infty$ $F: N \to M$ is said to be an *immersion* at $p\in N$ if its differential $dF_p: T_pN \to T_{F(p)} M$ is injective, and a *submersion* at $p$ if $dF_p$ is surjective. We call $F$ an *immersion* if it is an immersion at every $p\in N$ and a *submersion* if it is a submersion at every $p\in N$. 

**Obs:** Suppose $N$ and $M$ are manifolds of dimension $n$ and $m$ respectively. then $\dim T_p N = n$ and $\dim T_{F(p)} M = m$. The injectivity of the differential $dF_p$  implies that $n \le m$. Similarly, the surjectivity of the differential $dF_p$ implies that $n \ge m$. Meaning, if $F: N \to M$ is a an immersion at a point or $N$, then $n \le m$ and if $F$ is a submersion at a point of $N$, then $n \ge m$. 

# Rank and Critical and Regular Points

**Def:** We consider a smooth map $F: N\to M$ of manifolds. Its *rank* at a point $p$ is $N$, denoted as $\text{rank } F(p)$, is defined as the rank of the differential $df_p : T_p N \to T_{F(p)} M$. Relative to the coordinate neighbourhoods $(U, x^1, \dots, x^n)$ and $(V, y^1, \dots, y^m)$ at $F(p)$, the differential is represented by the Jacobian matrix $\left[\dfrac{\partial F^i}{\partial x^j}(p)\right]$, so $$\text{rank } F(p) = \text{rank } \left[\dfrac{\partial F^i}{\partial x^j}(p)\right]$$
**Def:** A point $p$ in $N$ is a *critical point* of $F$ if the differential $dF_p: T_pN \to T_{F(p)} M$ fails to be surjective. it is a *regular point* of $F$ if the differential $dF_p$ is surjective, i.e., $F$ is a submersion at $p$. A point in $M$ is a *critical value* if it is the image of a critical point; otherwise it is a *regular value*.  ^071ac1

A point $c \in M$ is a critical value iff some point in the preimage $F^{-1}\{c\}$ is a critical point. A point $c$ in the image of $F$ is regular value iff *every* point in the preimage $F^{-1}\{c\}$ is a regular point. 

**Prop:** For a real-valued function $f:M \to \Bbb R$, a point $p\in M$ is critical point iff relative to some chart $(U, x^1, \dots, x^n)$ containing $p$, all the partial derivatives satisfy $$\frac{\partial f}{\partial x^j} (p) = 0, \qquad j\in \{1, \dots, n\}$$