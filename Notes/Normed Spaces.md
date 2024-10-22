---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Metric Spaces]], [[Vector Spaces]], [[Rn]]
Let $V$ be a vector space over $\Bbb R$. A _***norm**_ of $V$ is a function $\| \cdot\|: V \to \Bbb R$ that

N1) $\|v \| = 0$ iff $v = 0$

N2) $\|\lambda v \| = |\lambda | \| v\|$ for any $v \in V$, and $\lambda \in \Bbb R$

N3) $\|v+w\| \le \|v\| +\|w\|$ for any $v,w\in V$

A _**********normed space**********_ is vector space $V$ with a norm $\|\cdot \|$, usually denoted as $(V, \|\cdot\|)$, or simply $V$ where we don’t need to specify the norm. 

**********Prop:********** Every normed space $(V, \|\cdot\| )$ is a metric space with a metric given by

$$ d(v,w) = \|v-w\| $$

We can see that every norm induces a metric, but a metric is not always induced by a metric, namely, the discrete metric. This metric is transaltion invariant, and absolutely homogenuous.

We can see that [[Bases and Dimension|finite dimensional subspaces]] of a normed space $V$ are [[Topology on Metric Spaces|closed]]

************Def:************ In the special case we define that $\|\cdot\|_p : \Bbb R^n \to \Bbb R$ where $p \in [1, \infty]$, we define that

$$ \|x \|_p = \left(\sum_{i = 1}^n |x_i|^p\right)^{1/p} $$

in the case that $p = \infty$

We define numbers, $p, q \in (1,\infty)$ that satisfy $\dfrac{1}{p} +\dfrac{1}{q} = 1$, are called harmonic conjugates. We can extend the definition with $p = 1$, and $q = \infty$, as long as we define $\dfrac{1}{\infty} = 0$. This DOESN’T MEAN, that $1 = \infty \cdot 0$.

### Young’s Inequality

Let $p, q \in (1, \infty)$ such that $\dfrac{1}{p} +\dfrac{1}{q} =1$. Then, for any real numbers $a, b\ge0$ it follows that

$$ ab \le \frac{1}{p}a^p+\frac{1}{q}b^q $$

### Hölder’s Inequality in $\Bbb R^n$

Let $p, q$ harmonic conjugates. Then for any $x, y \in \Bbb R^n$, it follows that with ${(xy)_i = x_i y_i}$ (Hadarmard product) for $1 \le i \le n$

$$ \sum_{i = 1}^n|x_iy_i | \le \left(\sum_{i = 1}^n |x_i|^p \right)^{1/p}\left(\sum_{i = 1}^n |y_i|^q \right)^{1/q} $$

or equivalently,

$$ \|xy\|_1 \le \|x\|_p \|y\|_q $$

### Minkowski Inequality in $\Bbb R^n$

Let $p \in [1, \infty]$, then for any $x, y \in \Bbb R^n$ we have that

$$ \|x+y\|_p \le \|x\|_p +\|y\|_p $$

This finally gives us that $\|\cdot \|_p$ is a norm in $\Bbb R^n$. Then we can see that $(\Bbb R^n, \|\cdot\|_p)$ is a normed space, and we can denote it simply as $\Bbb R^n _p$.

We can compare different $p$-metrics, and get the following results:

- $\|x \|_r \le \|x\|_s$ for $1 \le s\le r\le\infty$
    
- $\|x\|_s \le n^{\frac{r-s}{sr}} \|x\|_r$ for $1 \le s\le r<\infty$
    
- $\|x\|_s \le n^{\frac{1}{s}} \|x\|_\infty$ for $1 \le s < \infty$
    
- For any $x \in \Bbb R^n$, we have that
    
    $$ \|x\|_\infty = \lim_{r \to \infty} \|x\|_r $$