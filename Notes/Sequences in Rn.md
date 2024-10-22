---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]]
Links: [[Limits of a Sequence in R]]

We can use sequences of $\Bbb R$ to help us define convergence of sequences on $\Bbb R^n$.

**Th:** Given a sequence $(x_k)_{k\in\Bbb N} \to x$, iff $|x_k - x | \to 0$

**Def:** A sequence$(\mathbf{a}_k)_{k\in\Bbb N}$ in $\Bbb R^n$ is said to converge to $a\in\Bbb R^n$, if $\|{a}_k-{a}\| \to 0$ in $\Bbb R$. The we can write that $\lim_{k\to \infty} {a}_k = {a}$, or ${a}_k \to {a}$. In case that $a_k$ doesn’t converge to $a$, we write that ${a}_k \Bbb Not\to {a}$.

**Th:** A sequence $(a_k)$ in $\Bbb R^n$ converges to $a$ iff:

$$ \forall \varepsilon >0\exists N\in \Bbb N(\forall m \ge N[\|{a}_m - {a}\| < \varepsilon]) $$

**************Th:************** The limit of a sequence in $\Bbb R^n$ is unique.

**Th:** Let$({a}_k)$ be sequence in $\Bbb R^n$, with ${a}_k = (a_{i, k})_{i=1}^n$, and $\mathbf{a} = (a_i) _{i=1}^n$, $\mathbf{a}_k \to \mathbf{a}$ iff each $1\le i \le n$, $a_{i, k} \to a_i$. In other words, convergence of $(\mathbf{a}_k)$ is equivalent to the convergence of each of the coordinates.

**Def:** A sequence $({a}_k)$ in $\Bbb R^n$ is said to be *Cauchy* if:

$$ \forall \varepsilon > 0 \exists N \in \Bbb N[\forall k, m \ge N(\|{a}_k-{a}_m\| < \varepsilon)] $$

**Th:** Let$(a_k)$ be sequence in $\Bbb R^n$, with $\mathbf{a}_k = (a_{i, k})_{i=1}^n$ and it is a _****Cauchy****_ sequence, iff each ${1\le i \le n}$, $(a_{i, k})$ is ******Cauchy******. In other words, $({a}_k)$ _******Cauchy-ness******_ is equivalent to the ********Cauchy-ness******** of each of the coordinates.

********Th: $\Bbb R^n$** is a complete metric space, or $(\mathbf{a}_k)$ is a sequence in $\Bbb R^n$ it is convergent iff it is Cauchy. Then $\Bbb R^n$ is a [[Hilbert Spaces]].

********Th:******** Let $({a}_k)$ and $({b}_k)$ be sequences in $\Bbb R^n$, such that ${a}_k \to {a}$ and ${b}_k \to {b}$, then:

- $({a}_k +{b}_k) \to {a}+{b}$
- $({a}_k \cdot {b}_k) \to {a}\cdot {b}$
- If $c \in \Bbb R$, then $(c{a}_k) \to c{a}$