---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Basic Cardinal Arithmetic]], [[Regular and Singular Cardinals]]

Let $\langle A_i \mid i \in I\rangle$  be a system of mutually disjoint sets, and let $|A_i| = \kappa_i$  for all $i \in I$. We define the *sum* of $\langle \kappa_i \mid i \in I\rangle$ by
$$
\sum_{i \in I} \kappa_i = \left|\bigsqcup _{i \in I} A_i\right|
$$
If $\langle A_i \mid i \in I\rangle$ and $\langle A'_i \mid i \in I\rangle$ are systems of mutually disjoint sets such that $|A_i| = |A_i'|$  for all $i \in I$, then $\left|\bigsqcup_{i \in I}A_i \right| = \left|\bigsqcup_{i \in I}A_i'\right|$ 

This lemma makes the definition of $\sum_{i\in I}\kappa_i$ legitimate. 

If $\kappa_i \le \lambda_i$ for all $i \in I$, then $\sum_{i \in I}\kappa_i \le \sum_{i\in I}\lambda_i$. 

We can see that $$\left|\bigcup_{i \in I} A_i\right| \le \sum_{i \in I} |A_i|$$

If the summands are all equal, then the following holds, as the finite case: If $\kappa =\kappa_i$ for all $i \in \lambda$, then
$$
\sum_{i \in \lambda} \kappa_i = \kappa\cdot \lambda
$$
**Th:** Let $\lambda$ be an infinite ordinal, let $\kappa_\alpha$ $(\alpha < \lambda)$ be a nonzero cardinal numbers, and let $\kappa = \sup\{\kappa_\alpha \mid \alpha < \lambda\}$
$$
\sum_{\alpha < \lambda}\kappa_\alpha = \lambda \cdot \kappa = \lambda \cdot \sup\{\kappa_\alpha \mid \alpha < \lambda \}
$$
If $J_i$ $(i \in I)$ are mutually disjoint sets and $J = \bigcup_{i \in I}J_i$, and $\kappa_j$ $(j\in J)$ are cardinals, then 
$$
\sum_{i \in I}\left(\sum_{j \in J_i} \kappa_j\right) = \sum_{j \in J}\kappa_j
$$

We also get the distributive law, let $\lambda$ be a cardinal, and $\kappa_i$ be a cardinal for every $i \in I$, then $$\lambda \cdot \left(\sum_{i \in I}\kappa_i\right) = \sum_{i \in I} (\lambda \cdot \kappa_i)$$

Let $\langle A_i \mid i \in I\rangle$ be a family of sets such that $|A_i| = \kappa_i$ for all $i \in I$. We define the product $\langle \kappa_i \mid i \in I\rangle$ by
$$
	\prod_{i \in I}\kappa_i = \left|\prod_{i \in I} A_i\right|
$$
Let $\langle A_i \mid i \in I\rangle$ and $\langle A_i' \mid i \in I\rangle$ are such that $|A_i|= |A_i'|$  for all $i \in I$, then $|\prod_{i \in I} A_i| = |\prod_{i \in I} A_i'|$ 

The infinite products have many properties of finite products of natural numbers. For instance, if at least on $\kappa_i$ is $0$, then $\prod_{i \in I}\kappa_i =0$. 

If $J_i$ $(i \in I)$ are mutually disjoint sets and $J = \bigcup_{i \in I}J_i$, and $\kappa_j$ $(j\in J)$ are cardinals, then 
$$
\prod_{i \in I}\left(\prod_{j \in J_i} \kappa_j\right) = \prod_{j \in J}\kappa_j
$$
If $\kappa_i \le \lambda_i$ for all $i \in I$, then $\prod_{i \in I}\kappa_i \le \prod_{i\in I}\lambda_i$. 

If the factors are all equal, then the following holds, as the finite case: If $\kappa =\kappa_i$ for all $i \in \lambda$, then
$$
\prod_{i \in \lambda} \kappa_i = \kappa^ \lambda
$$

The following rules, involving exponentiation, also generalize from the finite to the infinite case
$$
\prod_{i \in I}(\kappa_i ^\lambda) = \left(\prod_{i\in I} \kappa_i\right)^\lambda
$$
$$
\prod_{i \in I}\kappa^{\lambda_i} = 
\kappa^{\sum_{i \in I}\lambda_i}
$$
##### König's Theorem
If $\kappa_i$ and $\lambda_i$ $(i \in I)$ are cardinal numbers, and if $\kappa_i < \lambda_i$, for all $i \in I$, then
$$
	\sum_{i \in I}\kappa_i < \prod_{i \in I}\lambda_i
$$
We have that if $1 < \kappa_i \le \lambda_i$  for all $i\in I$, then
$$
	\sum_{i \in I}\kappa_i \le \prod_{i \in I}\lambda_i
$$
# Cardinal Exponentiation

By Cantor's Theorem, we get that $2^{\aleph_\alpha} > \aleph_\alpha$, in other words,  $$\aleph_{\alpha +1} \le 2^{\aleph_\alpha}$$We can look at the [[Generalised Continuum Hypothesis]], and we get that $$ \aleph_{\alpha +1} = 2^{\aleph_\alpha}$$Without assuming the Generalised Continuum Hypothesis, there is not much one can prove about $2^{\aleph_\alpha}$ except, the first property and the trivial property $$2^{\aleph_\alpha} \le 2^{\aleph_\beta} \quad \text{whenever} \quad \alpha\le \beta$$
**Lemma:** For every $\alpha$, $$\aleph_\alpha < \text{cf}(2^{\aleph_\alpha})$$Thus $2^{\aleph_0}$ cannot be $\aleph_\omega$, since $\text{cf}(2^{\aleph_\omega}) = \aleph_0$, but the lemma doesn't prevent $2^{\aleph_0}$ from being $\aleph_{\omega_1}$. Similarly, $2^{\aleph_1}$ cannot be either $\aleph_{\omega_1}$ or $\aleph_\omega$ or $\aleph_{\omega + \omega}$, etc.

If there's a $\gamma < \alpha$ such that $\aleph_\gamma^{\aleph_\beta}\ge \aleph_\alpha$, then $\aleph_{\alpha}^{\aleph_\beta} = \aleph_\gamma^{\aleph_\beta}$ 

**Th:** Let $\aleph_\alpha$ be a singular cardinal. Let us assume that  the value of $2^{\aleph_\xi}$ for all $\xi < \alpha$, say $2^{\aleph_\xi} = \aleph_\beta$. Then $2^{\aleph_\alpha} = \aleph_\beta$.   

**Lemma:** If $\alpha \le \beta$, then $\aleph_\alpha^{\aleph_\beta} = 2^{\aleph_\beta}$ 

**Lemma:** Let $\alpha \ge \beta$, and let $S$ be the set of all subsets $X\subseteq \omega_\alpha$ such that $|X| = \aleph_\beta$. Then $|S| = \aleph_\alpha^{\aleph_\beta}$.

**Th:** Let us assume the Generalised Continuum Hypothesis. If $\aleph_\alpha$ is a regular cardinal, then $$ \aleph_\alpha^{\aleph_\beta} = \begin{cases} \aleph_\alpha & \beta < \alpha\\  \aleph_{\beta +1} & \beta \ge \alpha\end{cases}$$
**Lemma:** For every cardinal $\kappa >1$, and every $\alpha$, $\text{cf}(\kappa^{\aleph_\alpha}) > \aleph_\alpha$

**Th:** Let us assume the Generalised Continuum Hypothesis. If $\aleph_\alpha$ is a singular cardinal, then $$ \aleph_\alpha^{\aleph_\beta} = \begin{cases}
\aleph_\alpha & \aleph_\beta < \text{cf}(\aleph_\alpha)\\
\aleph_{\alpha +1} & \text{cf}(\aleph_\alpha) \le \aleph_\beta \le  \aleph_\alpha\\
\aleph_{\beta+1} & \aleph_\beta \ge \aleph_\alpha
\end{cases}$$
**Hausdorff's Formula:** 
For every $\alpha$ and every $\beta$ $$\aleph_{\alpha+1}^{\aleph_\beta} = \aleph_\alpha^{\aleph_\beta}\cdot \aleph_{\alpha +1}$$
We get the result that for $n < \omega$, then $$ \aleph_n ^{\aleph_\beta} = \aleph_n \cdot 2^{\aleph_\beta}$$ We can also get the result $$\prod_{n <\omega} \aleph_n = \aleph_\omega ^{\aleph_0} $$We get a small corollary from this let $\beta > 0$, then $$\aleph_\omega^{\aleph_\beta} = \aleph_\omega^{\aleph_0} \cdot 2^{\aleph_\beta}$$