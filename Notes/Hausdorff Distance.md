---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Metric Spaces]], [[Compactness in Metric Spaces]]

Let $X$ be a metric space. Given a subset $A\subseteq X$, consider the distance function to $A$, $\text{dist}_A:X\to [0, \infty)$ defined as $$\text{dist}(x, A) =\text{dist}_A(x) :=\inf_{a \in A} d(x, a)$$
Let $A$ and $B$ be two nonempty compact subsets of a metric space $X$. The the *Hausdorff distance* between $A$ and $B$ is defined as: $$d_H(A, B) := \sup_{x \in X}|\text{dist}_A(x)-\text{dist}_B(x)| = \sup_{x \in X}| \text{dist}(x, A) - \text{dist}(x, B)| $$
We denote as the set of all compact sets of $X$, as $\mathcal K(X)$ 

Suppose that $A$ and $B$ be two compact subsets of a metric space $X$. Then $d_H(A, B) <R$ iff $B$ lies in an $R$-neighborhood of $A$, and $A$ lies in an $R$-neighborhood of $B$.

Let $X$ be a metric space. Given a subset $A \subseteq X$ define its diameter as $$ \text{diam} (A) = \sup_{a, b\in A} d(a, b)$$
$\text{diam}\; : \mathcal K(X) \to \Bbb R$ is a $2$-Lipschitz function; that is $$|\text{diam} (A) - \text{diam}(B) | \le 2 d_H(A, B)$$
## Hausdorff Convergence

In this metric space $(\mathcal K(X), d_H)$ sometimes it can be called $\text{Haus }X$  .

Suppose $(K_n)_{n \in \Bbb N}$ be a a sequence of compact subsets of $X$, and. We say that $K_n$ *converges* to $K$ in the *sense of Hausdorff*, iff $\lim d_H(K_n , K) = 0$, just as we did in general metric spaces. We can also say that $K$ is the *Hausdorff limit* of $K_n$. 

**Monotone Convergence:** Let $K_1 \supseteq K_2 \supseteq \cdots$ be a nested sequence of nonempty compact sets in a metric space $X$. Then $K = \bigcap_{n = 1}^\infty K_n$ is the Hausdorff limit of $K_n$; that is $\lim d_H(K_n , K) =0$. 

**Lemma:** If $X$ is a compact metric space, then $\text{Haus }X$ is complete.

**Blaschke selection theorem:** A metric space $X$ is compact iff so is $\text{Haus }X$