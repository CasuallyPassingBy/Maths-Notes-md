---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]

**Def:** A metric over the non-empty set $X$ is a function $d:X\times X \to \Bbb R$ that satisfies for any ${x, y,z \in X}$:

M1) for any $d(x,y) = 0$ iff $x= y$

M2) $d(x,y) = d(y,x)$

M3) $d(x,z) \le d(x, y)+d(y,z)$

The pair $(X, d)$ is called a _metric space_

Having that $d(x, x) =0$, is a requirement for any of the generalized notions of metric

If we have that a function $d: X \times X \to \Bbb R$, that fails to any of the requirments it is called with another name:

- If M1) fails we call $d$ a pseudo-metric
- If M2) fails we call $d$ a quasi-metric
- If M3) fails we call $d$ a semi-metric

We know that if $X$ is nonempty we can always define a metric on $X$, namely $d:X \times X \to \Bbb R$, defined as

$$ d(x,y) = \begin{cases} 1 &x = y \\ 0 & x\ne y \end{cases} $$

This has a special name, the _**discrete metric_**

We can define the product of metrics spaces $(X, d_X)$ and $(Y, d_Y)$, then we define a metric on $(X \times Y, d_p)$ with $p \in [1,\infty]$. If $p \in[1,\infty)$ we define

$$ d_p((x_1,y_1),(x_2, y_2)) = (d_X(x_1, x_2)+ d_Y(y_1, y_2))^{1/p} $$

if $p = \infty$, then

$$ d_\infty((x_1,y_1),(x_2, y_2)) =\max \{d_X(x_1, x_2), d_Y(y_1, y_2)\} $$

### Metric Identification on Pseudo-metric Spaces
If we have a pseudo-metric space $(X, d)$, we can generate an equivalence relation $\sim$, that is defined as $x \sim y$ iff $d(x,y) = 0$. Then if we take quotient out the zeros we get that $X/\sim$, and $d': (X/\sim) \times (X/\sim) \to \Bbb R$, defined as $d'([x], [y]) = d(x, y)$ , with $[x]$ and $[y]$ being the equivalence clases of $X/\sim$, then we get that $(X / \sim , d')$ is a metric space.

Basically since the metric can’t tell them apart, then neither should we.

## $\infty$-Metrics

We can also consider the metrics with values $[0, \infty]$; that is we allow infinite distance between points. We might call them $\infty$-metrics, but most of the time we use the term metric. 

We can reduce $\infty$-metrics into metrics. Let $$ x\approx y \quad \iff \quad d(x, y) <\infty$$it defines an equivalence relation in $X$. The equivalence of a point $x \in X$ will be called the *metric component* of $x$; it will be denoted by $X_x$; note that $$ X_x = B(x, \infty)$$ that is, the metric component of $x$ is the open ball centered at $x$ and radius $\infty$.

If $\{X_\alpha\}$ is a collection of metric spaces, then *disjoint union* $X = \bigsqcup_\alpha X_\alpha$ will be considered with a natural metric defined by:
$$ d(x, y) = \begin{cases}d_\alpha(x, y) & x, y \in X_\alpha \\
\infty & \text{otherwise} \end{cases}$$
If follows that any $\infty$ metric space is a disjoint union of genuine metric spaces, the metric components of the original $\infty$-metric space. 