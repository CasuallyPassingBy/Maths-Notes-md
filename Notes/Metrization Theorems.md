---
tags:
  - Topology
  - Analysis
---
Subjects: [[Topology]], [[Metric and Normed Spaces]]
Links: [[Metrizable Spaces]], [[Paracompacteness]]

**Th:** Every open cover of a psuedometrizable space has an open refinement which is both locally finite and $\sigma$-discrete; in particular, every psuedometrizable space is paracompact.

**Prop:** Every psuedometrizable space has a $\sigma$-discrete base.

**Cor:** Every psuedometrizable space has a $\sigma$-locally finite base.

**Lemma:** Every regular space which has a $\sigma$-locally finite base is perfectly normal.

**Lemma:** Let $X$ be a $T_0$ space and $\{d_n \mid n < \omega\}$ a countable family of psuedometrics on the set which are all bounded by $1$ and satisfy the following two conditions:
- $d_n: X \times X \to \Bbb R$ is a continuous function for all $n < \omega$.
- For every $x\in X$ and every nonempty closed set $A\subseteq X$ such that $x\notin X$ there exists $n <\omega$ such that $d(x, A) := \inf\{d_n(x, a) \mid a \in A\} > 0$
Then the space $X$ is metrizable and the function $d$ defined by $$
d(x, y) := \sum_{n < \omega} \frac1{2^n} d_n(x, y)
$$is a metric space on the space $X$.

**Th:** The product space $(J(\kappa))^\omega$ of the hedgehog $J(\kappa)$ is universal for all $T_3$ spaces of weight $\kappa \ge \omega$ and with a $\sigma$-locally finite base.

**Nagata-Smirnov Metrization Theorem:** A topological space is metrizable iff it is $T_3$ and has a $\sigma$-locally finite base.

**Nagata-Smirnov Psuedometrization Theorem:** A topological space is metrizable iff it is regular and has a $\sigma$-locally finite base.

**Bing Metrization Theorem:** A topological space is metrizable iff it is $T_3$ and has a $\sigma$-discrete base.

**Kowalsky's Metrization Theorem:** The product space $(J(\kappa))^\omega$ of the hedgehog $J(\kappa)$ is universal for all metrizable spaces of weight $\kappa \ge \omega$.

**Th:** If $X$ is a metrizable space and $f: X \to Y$ is a perfect function, then $Y$ is metrizable.

**Vaĭnšteĭn's Lemma:** If $f:X \to Y$ is a closed, continuous surjective function, and $X$ is metrizable, then for every $y\in Y$ such that $\chi(y, Y) \le\omega$ the set $\text{Fr}(f^{-1}\{y\})$ is compact.

**Hanai-Morita-Stone Theorem:** The following statements are equivalent if $X$ is a metrizable space, and $f: X \to Y$ is a closed, continuous and surjective function. ^fdd00b
- $Y$ is metrizable.
- $Y$ is first-countable.
- For every $y\in Y$ the set $\text{Fr}f^{-1}\{y\}$ is compact. 

**Th:** If $f:X \to Y$ is a closed, open, continuous, surjective function, and $X$ is metrizable, then $Y$ is metrizable.

**Th:** If a topological space $X$ has a point finite closed cover consisting of metrizable spaces, then $X$ is itself metrizable.