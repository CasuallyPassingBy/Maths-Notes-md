---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Sequences in Rn]], [[Limits of a Sequence in R]], [[Metric Spaces]], [[Continuity on Metric Spaces]], [[Sequences in Rn]]
**Def:** A sequence in $X$ is a function $x_\bullet:\Bbb N\to X$. The sequence it will be usually represented as $(x_n)_{n\in \Bbb N}$

**************Def:************** A sequence $(x_n)_{n\in \Bbb N}$ of points in $(X, d)$ converges to a point $x \in X$ iff

$$ \forall \varepsilon > 0 \exists N\in \Bbb N[\forall n \ge N(d(x_n, x) < \varepsilon] $$

We can use the notations

$$ x_k \to x \ \text{ in }X \quad \text{or} \quad \lim_{k \to\infty} x_k = x $$

Let $x_\bullet$ be a sequence, then $x_\bullet$ converges to $x$ in $X$ iff $U$ is an open subset of $X$, that $x \in U$, then there’s $m \in \Bbb N$ such that if $k \ge m$, then $x_k \in U$. This brings a [[Topology on Metric Spaces|topological description]] to sequence converging

Let $x_\bullet$ be a sequence, then $x_\bullet$ is said to be **eventually constant** if there’s $N \in \Bbb N$, such that if ${n \ge N}$, then $x_n = x_N$. This sequences always converge no matter the metric space, and in the discrete metric this are the only sequences that converge, i.e., if the $d$ is the discrete metric on $X$, then $x_\bullet$ converges iff $x_\bullet$ is eventually constant

A subsequence of $x_\bullet$ is the composition of $x_\bullet$ with an strictly increasing function $f: \Bbb N \to \Bbb N$. Then the $i$th term of the subsequence is $x_{f(i)}$

From this we can see that the limit of a sequence is unique, since all metric spaces are Hausdorff.

If $x_\bullet$ converges to $x$ in $X$, then any subsequence of $x_\bullet$ converges to $x$ in $X$.

A sequence $x_\bullet$ is _bounded_ on $X$ if there’s $x \in X$ and $c\in \Bbb R$ such that $d(x_k, x) \le c$ for all $k \in \Bbb N$

Any convergent sequence is bounded

Let $A$ be a subset of $X$ and $x \in X$. Then $x \in \overline A$ iff there’s a sequence $x_\bullet$ such that $x_k \in A$, for all $k \in \Bbb N$ and $x_k \to x$ in $X$

Let $\phi:X\to Y$ be a function such that for any sequence, $(x_n)_{n\in \Bbb N}$ such that converges  $x_0\in X$, then $(\phi(x_n))_{n\in \Bbb N}$ converges to $\phi(x_0)$. Then $\phi$ is *sequentially continuous* at $x_0$. If it is sequentially continuous for all $x\in X$, then it is just *sequentially continuous.* 

Let $\phi: X\to Y$ is continuous at $x\in X$ iff is sequentially continuous at $x$. This is equivalent to the [[Axiom of Choice#Axiom of Countable Choice|Axiom of Countable Choice]]

We call that $x$ is a partial limit of $x_n$, if there's a subsequence that converges to $x$. 