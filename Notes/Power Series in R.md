---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Series of Functions in Rn]], [[Series in R]], [[limsup and liminf]]
**********Def:********** Let $f_n= a_n(x-c)^n$, for all $n\in\Bbb N$. Then the series of of the form

$$ \sum_{n=0}^\infty f_n = \sum_{n=0}^\infty a_n (x-c)^n $$

It is called a power series around $c\in\Bbb R$

## Theorems

If a power series $\sum a_n x^n$ converges for some $x_0\in\Bbb R$, then it converges absolutely for any $x$ that satisfies $|x|<x_0$.

If If a power series $\sum a_n x^n$ absolutely converges for some $x_0\in\Bbb R$, then it converges uniformly on $[-c, c]$, where $c = |x_0|$.

_**Abel Theorem:**_ Let $g(x) = \sum a_n x^n$ be a power series that converges at the point $x = R >0$. Then the series converges uniformly on $[0, R]$. A similar result if the series converges at ${x = -R}$.

If a power series converges pointwise on $A \subseteq \Bbb R$, then it converges uniformly on any compact set $K \subseteq A$.

Let a power series $\sum a_n x^n$. Considering the sequence $(\sqrt[n]{|a_n|})$ if it is bounded. Let ${\rho = \limsup \sqrt[n]{|a_n|}}$. We can define the _radius of convergence $R$_ as $1/\rho$, and $\sum a_n x^n$ will converge on $(-R, R)$

$$ \limsup\sqrt[n]{|a_n|} = \lim\left | \frac{a_{n+1}}{a_n}\right| $$

$\limsup\sqrt[n]{|a_n|} = \lim\left | \frac{a_{n+1}}{a_n}\right|$

**Cauchy-Hadamard Theorem:**

If $R$ is the radius of convergence of the power series $\sum a_n x^n$, then for $|x| < R$ will converge absolutely, and if $|x| > R$ will diverge.

If a power series $\sum a_n x^n$ converges on $(-R, R)$, then the differentiated series $\sum n a_{n-1}x^{n-1}$ also converges on $(-R, R)$, and any compact set contained in $(-R, R)$.

**Term by Term Differentiation:**

Assume:

$$ f(x) = \sum_{n=0}^\infty a_n x^n $$

converges on an interval $A \subseteq \Bbb R$, then $f$ is continuous on $A$, and differentiable on $(-R, R) \subseteq A$. The derivative is given by:

$$ f'(x) = \sum_{n=0}^\infty na_{n-1}x^{n-1} $$

Moreover, $f$ is infinitely differentiable on $(-R, R)$, and the successive derivatives are obtained via term-by-term differentiation.

**Term-by-Term Antidifferentiation:**

Assume:

$$ f(x) = \sum_{n=0}^\infty a_n x^n $$

converges on $(-R,R)$, and let:

$$ F(x) =\sum _{n=0}^\infty \frac{a_n}{n+1} x^{n+1} $$

is defined on $(-R, R)$ and $F'(x) = f(x)$, and $f$ can be integrated on any compact set $K \subseteq (-R, R)$, using $F$ as an antiderivative.

**Uniqueness:** If $\sum a_nx^n$ and $\sum b_nx^n$ converges on $(-R, R)$ to the same function $f$, then $\forall n\in \Bbb N[a_n = b_n]$

###### Cauchy Multiplication Theorem

**Let $f(x)= \sum a_nx^n$, and $g(x) = \sum b_n x^n$, then

$$ (fg)(x) = \left(\sum_{n= 0}^\infty a_nx^n \right)\left(\sum_{n= 0}^\infty b_nx^n \right) = \left(\sum_{n= 0}^\infty x^n \sum_{k=0}^n a_k b_{n-k}\right) $$

We can think of $$
\sum_{k = 0}^n a_k b_{n-k} = c_k
$$
as a discrete convolution