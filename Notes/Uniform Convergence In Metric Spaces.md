---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Space of Continuous Functions From Rn to Rm]], [[Sequence of Functions in Rn]], [[Compactness in Metric Spaces]], [[Continuous Function Spaces]], [[Bounded Function Spaces]]

A sequence of functions $f_k: S \to X$, with $k \in \Bbb N$, _converges pointwise_ on $S$ to a function ${f:S \to X}$, if $f_k (z) \to f(z)$ on $X$ for all $z\in S$, we can denote it as $f_k \to f$. Meaning that for all $\varepsilon>0$ and $z \in S$ there’s $N \in \Bbb N$, if , then

$$ d_x(f_k(z), f(z)) <\varepsilon $$

The function $f$ is called the _pointwise limit_ of $(f_k)$

A sequence of functions $f_k : S \to X$, with $k \in \Bbb N$, _converges uniformly_ on $S$ to a function ${f:S \to X}$, if for all $\varepsilon>0$, there’s $N \in \Bbb N$ (which only depends of $\varepsilon$) such that

$$ d_X(f_k(z), f(z)) \qquad \forall z \in S $$

The function $f$ is called the _************uniform limit************_ of $(f_k)$, we can denote this limit as $f_k \rightrightarrows f$.

Every uniformly convergent sequence of functions is pointwise convergent of sequence of functions.

Let $Z=(Z, d_Z)$ and $X =(X,d_X)$ be metric spaces. If $f_k : Z\to X$ is continuous for all $k \in \Bbb N$ and $(f_k)$ converges uniformly to $f$ in $Z$, then $f: Z \to X$ is continuous.

Let $(f_k)$ be a sequence in ${\cal B}(S, X)$. Then $(f_k)$ converges uniformly to $f$ in $S$ iff $(f_k)$ converges to $f$ in ${\cal B}(S, X)$.

Let $Z$ and $X$ be metric spaces. The ***_space of continuous and bounded functions from $Z$ to $X$_ is the metric space.

$$ {\cal C}^0_b(Z, X) = \{f:Z \to X\mid f \text{ is continuous and bounded}\} $$

Let $Z$ and $X$ be metric spaces. Then ${\cal C}^0_b(Z, X)$ is closed subspace of ${\cal B}(Z, X)$.

A compact metric space is complete

The finite product of complete metric spaces is complete

We can see that if $K$ is a compact metric space, then

$$ {\cal C}^0(K, X) = {\cal C}^0_b(K, X) $$

[[Interchange of Limits|Differentiable Limit Theorem]], is a consequence of the general version uniform convergence.