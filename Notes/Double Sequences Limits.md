---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Limits of a Sequence in R]]

### Definition
$s: \mathbb{N}\times\mathbb{N}\to\mathbb{C}$ is a _double sequence,_ denoted as $(s(n, m))$ or $(s_{n,m})$. The double sequence $s_{n,m}$ converges to some $a \in\mathbb{C}$ iff

$$ \forall\varepsilon>0\exists N\in\mathbb{N}(\forall n, m\geq N [\left|s_{n,m} -a \right|<\varepsilon]) $$

$a$ is called the _double limit_ of the sequence $s_{n,m}$, also denoted as $\lim_{n,m\to\infty} s_{n,m} = a$. If there’s no $a$ we say that the sequence _diverges._

_**Uniqueness of the Double limit:**_ A double sequence of complex numbers of has at most one limit.

### Boundedness

A double sequence $s_{n,m}$ is bounded iff there’s a $M > 0$ such that $\forall n,m\in\mathbb{N}|(|s_{n,m}| < M)$

Every convergent double sequence is _bounded_

### Iterated Limits

The limits of the sequence $s_{n,m}$:

$$ \lim_{n\to\infty}\left(\lim_{m\to\infty} s_{n,m}\right) \text{ and } \lim_{m\to\infty}\left(\lim_{n\to\infty} s_{n,m}\right) $$

Are called _iterated limits._

_**Theorem:**_ Let $\lim_{n,m\to\infty} s_{n,m} = a$. Then the iterated limits:

$$ \lim_{n\to\infty}\left(\lim_{m\to\infty} s_{n,m}\right) \text{ and } \lim_{m\to\infty}\left(\lim_{n\to\infty} s_{n,m}\right) $$

exists and both are equal to $a$ iff:

- $\lim_{m\to\infty} s_{n,m}$ exists for every $n\in\mathbb{N}$, and
- $\lim_{n\to\infty} s_{n,m}$ exists for every $m\in\mathbb{N}$.

### Moore-Osgood Theorem for Double Sequences

Let the double sequence $s_{n,m}$ such that:

1. The iterated limit $\lim_{m\to\infty}\left(\lim_{n\to\infty} s_{n,m}\right)= a$, and
2. the limit $s_{n,m}\rightrightarrows c_m$

for every $m \in\mathbb{N}$.

Then, $\lim_{n,m\to\infty} s_{n,m} = a$.

### Cauchy Double Sequences

_**Definition:**_ A double sequence is called a _Cauchy double sequence_ iff:

$$ \forall\varepsilon>0\exists N\in\mathbb{N[\forall p,q\geq n,m\geq N(\left|s_{n,m} -s_{p,q} \right| <\varepsilon)]} $$

_**Theorem:**_ A double sequence of complex numbers _converges_ iff it’s _Cauchy_.