---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Continuity on R]], [[Normed Vector Spaces]], [[Vector Spaces]], [[Bounded Function Spaces]], [[Continuity on Metric Spaces]], [[Compactness in Metric Spaces]], [[Compactness]], [[Space of Compactly Supported Functions]]

# Space of Continuous Functions
We usually work with two types of functions spaces, the bounded ones and the continuous ones. We actually have a special notation for the set of all continuous functions from a topological space $X$ to metric spaces $Y$
$$
{\mathcal C(X, Y)}={\cal C}^0(X, Y):= \{f:X\to Y\mid f \text{ is continuous}\}
$$
But this might not be good enough and we actually work with a subset 
$$
{\mathcal C_b (X, Y)}={\cal C}^0_b(X, Y):= \{f:X\to Y\mid f \text{ is continuous and bounded}\}
$$
This more restricted space is usually better behaved.

If we make it such that $X$ is a compact space, we actually get that 
$$
{\cal C}_b(X, Y) =  {\cal C}(X, Y)
$$
Meaning that this is the most well behaved. If we have that $Y$ is a normed space then any ${\cal C}(X, Y)$ is also a normed space, and we usually endow it with the uniform norm, or uniform metric as the [[Bounded Function Spaces]]

Lastly, if we only denoted it as 
$$
{\cal C}(X) := {\cal C}_b(X, \Bbb R) 
$$
Since it is so common to send them to $\Bbb R$

**Obs:** Let $X$ be a metric space, then $\mathcal C(X)$ is metrisable using the norm $\|\cdot\|_\infty$. 

**Prop:** If $X$ be a second countable compact Hausdorff space , then $\mathcal C(X)$ is separable. 

**Prop:** Let $X$ be a compact Hausdorff space. Then for each continuous linear functional $L$ on $\mathcal C(X)$ there are positive continuous linear functionals $L_+$ and $L_-$ on $\mathcal C_0(X)$ such that $L = L_+ - L_-$. We define $L_+$ by $$L_+(f) := \sup \{L(g) \mid g\in \mathcal C_0(X) \land 0\le g\le f\}, $$and the functional $L_- := L- L_+$. In addition, this decomposition is minimal in the sense that if $L = L_1-L_2$ is another decomposition of $L$ into a difference of positive linear functionals $L_1(f) \ge L_+(f)$ and $L_2(f) \le L_-(f)$ hold for each nonnegative $f\in \mathcal C(X)$. 

# Continuous Functions from $[a, b]$ to $\Bbb R$
We will look at ${\cal C}^0[a,b]$ be the set of continuous functions $f:[a,b] \to \Bbb R$. Then we can see that ${\cal C}^0[a,b]$ is a vector space. Similarly, that in the case of the $\ell^p$ spaces we will define a ${\|\cdot\|_p:{\cal C}^0[a,b] \to \Bbb R}$ with $p \in [1, \infty)$ having
$$ \|f\|_p = \left(\int_a^b |f(x)|^p\, dx\right)^{1/p} $$

and in the case that $p = \infty$ we get that
$$ \|f\|_\infty = \max_{a\le x\le b} |f(x)|.$$

### Hölder’s Inequality for Integrals
Let $p, q$ be harmonic conjugates. Let $f, g \in {\cal C}^0[a,b]$, then we get that
$$ \|fg\|_1 \le \|f\|_p \|g\|_q $$

### Minkowski’s Inequalities for Integrals
For $p \in [1,\infty]$, and $f,g \in {\cal C}^0[a,b]$, then
$$ \|f+g\|_p \le \|f\|_p +\|g\|_p $$

Then for $p\in [1, \infty]$, then $({\cal C}^0[a,b], \|\cdot\|_p)$ is a normed space. We can compact the notation to ${\cal C}^0_p[a,b]$ to represent $({\cal C}^0[a,b], \|\cdot\|_p)$, and if we write ${\cal C}^0[a,b]$ refers to $({\cal C}^0[a,b], \|\cdot\|_\infty)$

We can see some properties of these $p$-norms
- $\|f\|_s \le (b-a)^{\frac{r-s}{sr}}\|f\|_r$ for $1 \le s <r <\infty$
- $\|f\|_s \le (b-a)^{\frac{1}{s}}\|f\|_\infty$ for $1 \le s < \infty$

One important characteristic to note about ${\cal C}^0_p[a,b]$ is that for $p < \infty$, then ${\cal C}^0_p[a,b]$ it is not complete, and the [[Completion of a Metric Space|completion]] of this space is actually closely related to the [[Lp spaces]] 