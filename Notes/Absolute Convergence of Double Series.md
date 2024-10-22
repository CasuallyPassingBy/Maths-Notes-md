---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Double Series]], [[Absolute Convergence Test and Properties]]

_**Definition:**_ The _double series $\sum_{n,m = 1}^\infty z_{n,m}$_ is said to be _absolutely convergent_ if $\sum_{n,m = 1}^\infty |z_{n,m}|$ converges. The _iterated series_ $\sum_{m=1}^\infty\left(\sum_{n=1}^\infty z_{n,m}\right)$ is said to be _absolutely convergent_ if $\sum_{m=1}^\infty\left|\sum_{n=1}^\infty z_{n,m}\right|$ converges.

_**Theorem:**_ Every absolutely convergent double series is convergent.

_**Theorem:**_ $\forall n, m\in\mathbb{N}(z_{n,m} \in\mathbb{C} )$, and $\phi:\mathbb{N} \to \mathbb{N}^2$ be a bijection. If any of the following three sums:

$\sum_{n= 1}^\infty\sum_{m=1}^\infty |z_{n,m}|$, $\sum_{m= 1}^\infty\sum_{n=1}^\infty |z_{n,m}|$, $\sum_{k= 1}^\infty |z_{\phi(k)}|$ is finite, then all of the following series:

1. $\sum_{n=1}^\infty z_{n,m}$, for $m\in\mathbb{N}$
2. $\sum_{m=1}^\infty z_{n,m}$, for $n\in\mathbb{N}$
3. $\sum_{n = 1}^\infty \sum_{m=1}^\infty z_{n,m}$, $\sum_{m = 1}^\infty \sum_{n=1}^\infty z_{n,m}$, $\sum_{k=1}^\infty z_{\phi(k)}$

are absolutely convergent and the three series in $(3)$ have the same sum

_**Theorem:**_ $\forall n,m\in\mathbb{N}(z_{n,m} \in\mathbb{C})$, and let $\phi :\mathbb{N}\to\mathbb{N}^2$ be a bijection. Then,

1. $\sum_{k=1}^\infty z_{\phi(k)}$ converges absolutely iff $\sum_{n,m=1}^\infty z_{n,m}$ converges absolutely.
2. If $\sum_{n,m = 1}^\infty z_{n,m}$ converges absolutely to the sum $s$, then $\sum_{k=1}^\infty z_{\phi(k)}= s$.

_**Theorem:**_ $\forall n, m\in\mathbb{N}(z_{n,m} \in\mathbb{C} )$. If any of the following three sums:

$\sum_{n= 1}^\infty\sum_{m=1}^\infty |z_{n,m}|$, $\sum_{m= 1}^\infty\sum_{n=1}^\infty |z_{n,m}|$, $\sum_{n,m= 1}^\infty |z_{n,m}|$ is finite, then all of the following series:

1. $\sum_{n=1}^\infty z_{n,m}$, for $m\in\mathbb{N}$
2. $\sum_{m=1}^\infty z_{n,m}$, for $n\in\mathbb{N}$
3. $\sum_{n = 1}^\infty \sum_{m=1}^\infty z_{n,m}$, $\sum_{m = 1}^\infty \sum_{n=1}^\infty z_{n,m}$, $\sum_{n,m=1}^\infty z_{n,m}$

are absolutely convergent and the three series in $(3)$ have the same sum

_**Theorem:**_ Let $\sum_{n=1}^\infty a_n$, and $\sum_{m= 1}^\infty b_m$ be absolutely series of complex numbers with sums of $a$ and $b$, respectively. Let $z_{n,m}$ be a double sequence defined as:

$$ \forall n,m\in\mathbb{N}(z_{n,m} := a_nb_m) $$

Then the double series $\sum_{n,m= 1}^\infty z_{n,m} = ab$.