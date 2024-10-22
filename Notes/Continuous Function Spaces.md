---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Continuity on R]], [[Normed Spaces]], [[Vector Spaces]], [[Bounded Function Spaces]], [[Continuity on Metric Spaces]], [[Compactness in Metric Spaces]]

# Space of Continuous Functions

We usually work with two types of functions spaces, the bounded ones and the continuous ones. We actually have a special notation for the set of all continuous functions from a metric space $X$ to another one $Y$
$$
{\mathcal C(X, Y)}={\cal C}^0(X, Y):= \{f:X\to Y\mid f \text{ is continuous}\}
$$
But this might not be good enough and we actually work with a subset 
$$
{\mathcal C_b (X, Y)}={\cal C}^0_b(X, Y):= \{f:X\to Y\mid f \text{ is continuous and bounded}\}
$$
This more restricted space is usually better behaved.

If we make it such that $X$ is a compact metric space, we actually get that 
$$
{\cal C}^0_b(X, Y) =  {\cal C}^0(X, Y)
$$
Meaning that this is the most well behaved. If we have that $Y$ is a normed space then any ${\cal C}^0(X, Y)$ is also a normed space, and we usually endow it with the uniform norm, or uniform metric as the [[Bounded Function Spaces]]

Lastly, if we only denoted it as 
$$
{\cal C}^0(X) := {\cal C}^0_b(X, \Bbb R) 
$$
Since it is so common to send them to $\Bbb R$

# Continuous Functions from $[a, b]$ to $\Bbb R$
We will look at ${\cal C}^0[a,b]$ be the set of continuous functions $f:[a,b] \to \Bbb R$. Then we can see that ${\cal C}^0[a,b]$ is a vector space. Similarly, that in the case of the $\ell^p$ spaces we will define a ${\|\cdot\|_p:\cal C^0[a,b] \to \Bbb R}$ with $p \in [1, \infty)$ having

$$ \|f\|_p = \left(\int_a^b |f(x)|^p\, dx\right)^{1/p} $$

and in the case that $p = \infty$ we get that

$$ \|f\|_\infty = \max_{a\le x\le b} |f(x)| $$

depending on what we are working on we might even work on $L^p$ spaces which depend on Measure Theory and stuff

### Hölder’s Inequality for Integrals

Let $p, q$ be harmonic conjugates. Let $f, g \in {\cal C}^0[a,b]$, then we get that

$$ \|fg\|_1 \le \|f\|_p \|g\|_q $$

### Minkowski’s Inequalities for Integrals

For $p \in [1,\infty]$, and $f,g \in \cal C^0[a,b]$, then

$$ \|f+g\|_p \le \|f\|_p +\|g\|_p $$

Then for $p\in [1, \infty]$, then $(\cal C^0[a,b], \|\cdot\|_p)$ is a normed space. We can compact the notation to ${\cal C^0_p[a,b]}$ to represent $(\cal C^0[a,b], \|\cdot\|_p)$, and if we write $\cal C^0[a,b]$ referers to $(\cal C^0[a,b], \|\cdot\|_\infty)$

We can see some properties of these $p$-norms

- $\|f\|_s \le (b-a)^{\frac{r-s}{sr}}\|f\|_r$ for $1 \le s <r <\infty$
- $\|f\|_s \le (b-a)^{\frac{1}{s}}\|f\|_\infty$ for $1 \le s < \infty$

One important characteristic to note about ${\cal C}^0_p[a,b]$ is that for $p < \infty$, then ${\cal C}^0_p[a,b]$ it is not complete, and the [[Completion of a Metric Space|completion]] of this space is actually closely related to the [[Lp spaces]] 