---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Compactness in Metric Spaces]], [[Continuity on Metric Spaces#Uniform Continuity|Uniform Continuity]], [[Compact Sets in R#Bolzano-Weiestrass Theorem|Bolzano Weiestrass Theorem in R]], [[Rn#Bolzano-Weiestrass in $ Bbb R n$|Bolzano Weiestrass in Rn]], [[ellp spaces]], [[Metric Spaces]]
A sequence $(x_n)$ in $X$ is a _**Cauchy sequence**_ if for any $\varepsilon>0$, there’s an $N \in \Bbb N$, such that

$$ n, m\ge N \implies d_X(x_n, x_m) $$

Every convergent sequence in $X$ is a Cauchy sequence

Every Cauchy sequence in $X$ is a bounded sequence

If $(x_k)$ is a Cauchy sequence with a convergent subsequence then $(x_k)$ is convergent

A metric space $X$ is ********complete,******** if every Cauchy sequence in $X$ converges in $X$. A normed space is complete with the metric induced by its norm then it is called a *********Banach space************.

If there’s an equivalence $\phi: X \to Y$ between to metric spaces $X$ and $Y$, then $X$ is complete iff $Y$ is complete.

$\Bbb R^n$ is complete

Every normed space with finite dimension is a Banach space.

Let $X$ be a complete metric space. A metric subspace $A$ of $X$ is complete iff $A$ is closed in $X$.

A function $f:X \to Y$ is called ********Cauchy continuous or Cauchy-regular******** if for any Cauchy sequence $(x_n)$ in $X$, then $(f(x_n))$ is Cauchy in $Y$

Let $(x_n)$ be a Cauchy sequence on $X$, and $\phi:X \to Y$ is uniformly continuous, then $\phi$ is Cauchy continuous

Let $f: X \to Y$ is Cauchy continuous, then $f$ is continuous.

If $X$ is complete and $f:X \to Y$ is Cauchy continuous iff it is uniformly continuous

We can prove that $\ell^p$ is a Banach space for $1\le p<\infty$.

### Cantor Intersection Theorem
Let $X$ be a metric space, the following are equivalent:

- $X$ is complete
- If $\{ F_n \mid n \in \Bbb N\}$ is a decreasing sequence of nonempty closed sets  then $\bigcap\limits_{n \in \Bbb N}F_n\ne \varnothing$, if we have that $(\text{diam}(F_n))$ tends to $0$ in $\Bbb R$, then $\bigcap\limits_{n \in \Bbb N}F_n$ has only one point

This theorem can be used to prove that a compact set is sequentially compact.

### The Continuous Extension Theorem

Let $D$ be a dense subset of $X$, $Y$ be a complete metric space, and $f:D\to Y$ be uniformly continuous. Then there’s a unique function $f^*:X\to Y$ that is uniformly continuous and ${f^*|_D = f}$. This is similar when we extended a function from $A$ to $\overline A$ in $\Bbb R^n$
[[Topological Characterization of Continuity in Rn#**Uniform Extension Theorem**|Uniform Extension Theorem in Rn]], [[Uniform Continuity on R#Uniform Extension Theorem|Uniform Extension Theorem in R]]
