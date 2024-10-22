---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Continuity on Metric Spaces]], [[Topology on Metric Spaces]]

### Equivalence of Metrics and Norms
Two metrics $d_1$ and $d_2$, on a set $X$, are _**equivalent**_ if the identity $id:(X, d_1) \to (X, d_2)$ is an equivalence, meaning, if there are constants $c_1, c_2 >0$ such that

$$ c_1 d_2(x, y) \le d_1(x,y) \le c_2 d_2 (x,y) \quad \forall x, y \in X $$

Analogously, two norms $\| \cdot \|_1$ and $\|\cdot\|_2$ in a vector space $V$ are _**********equivalent**********_ if the induced metric are equivalent, meaning, if there are constants $c_1, c_2 >0$ such that

$$ c_1 \|v\|_2 \le \|v\|_1 \le c_2 \|v\|_2 \quad \forall v \in V $$

We can see that $\Bbb R^n_p$ is equivalent to $\Bbb R^n_q$ for $p, q \in [1, \infty]$, and thus no matter the metric we use in the product of metric spaces they are equivalent too.

A property that equivalence of metrics brings is that all the topological properties are preserved and additionally, we have that boundedness is also preserved on its own.

### Topological Equivalence of Metrics

We can have weaker version of equivalence of metrics, namely _*********topological equivalence*********_, let $d$ and $d'$ be metrics on $X$, then we say that those metrics are topological equivalent if ${\text{id}:(X, d) \to (X, d')}$ is a homeomorphism. Namely every open set of $(X, d)$ is also an open set of $(X, d')$ and vice versa.

Let $f:X\to Y$ be a function such that $f:X\to \text{Im }f$ is a homeomorphism then the metric

$$ d'(x,y) =d_Y(f(x), f(y)) $$

is topologically equivalent to $d_X$ (the original metric of $X$)

We get that $(x_k)$ be a sequence in $X$, with $d$ and $d'$ being topological equivalent norms, then $(x_k)$ converges in $(X, d)$ iff $(x_k)$ converges in $(X, d')$

This notion of topological equivalence preserve all the topological properties of each metric, but doesn’t necessarily preserve boundedness. Meaning a bounded set in a metric might not be one in the other. A clear example of this, is the normal metric of $\Bbb C$ and the metric of the Riemann Sphere $\hat{\Bbb C}$, where $\Bbb C$ is unbounded in the normal one, and bounded in the Riemann Sphere

Let $d$ be metric on $X$, then $\rho:X \times X \to \Bbb R$ defined as
$$
\rho(x, y) = \frac{d(x, y)}{1+d(x, y)} 
$$
is metric and is topologically equivalent to $d$. If a sequence $(x_n)_{n \in \Bbb N}$ is converges or it is Cauchy  on $\rho$ iff $(x_n)_{n \in \Bbb N}$ is converges or it is Cauchy on $d$, respectively. 

Additionally, if $d$ is a pseudometric, then so is $\rho$