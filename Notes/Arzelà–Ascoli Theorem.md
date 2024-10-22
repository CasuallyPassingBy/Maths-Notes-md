---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Space of Continuous Functions From Rn to Rm]], [[Compact Sets in Rn]], [[Compactness in Metric Spaces]], [[Complete Metric Spaces]], [[Continuous Function Spaces]], [[Total Boundedness]], [[Relative Compactness in Metric Spaces]], [[Compact Sets]]

For the rest of this section, let $K=(K, d_K)$ be a compact metric space and $(X, d_X)$ be a metric space, then we will consider the space of continuous functions

$$ {\cal C}^0(K, X) = \{f:K \to X\mid f \text{ is continuous} \} $$
## Arzelà-Ascoli Theorem
Let $K$ be a compact metric space, and $X$ be a complete metric space. A subset $\cal H$ of ${\cal C}^0(K, X)$ is relatively compact on ${\cal C}^0(K, X)$ iff $\cal H$ is [[Equicontinuity|equicontinuous]] and the sets

$$ {\cal H}(z) :=\{f(z) \mid f \in {\cal H}\} $$

are relatively compact in $X$ for all $z \in K$

Let $X$ and $K$ be compact metric spaces, then a subet ${\cal H}$ of ${\cal C}^0(K, X)$ is relatively compact iff ${\cal H}$ is equicontinuous.

Let $K$ be compact metric space, and $X$ be a complete metric space, the sequence $(f_k)$ in the space ${\cal C}^0(K, X)$ congerves pointwise to the function $f:K \to X$. If ${\cal H}:=\{ f_k \mid k \in \Bbb N\}$ is equicontinuous then $f$ is continuous and $f_k$ converges uniformly to $f$ or $f_k$ converges in ${\cal C}^0(K,X)$

### Arzelà-Ascoli Theorem to $\Bbb R^n$

Let $K$ be a compact metric space. A subset ${\cal H}$ of ${\cal C}^0(K, \Bbb R^n)$ is relatively compact on ${\cal C}^0(K, \Bbb R^n)$ iff $\cal H$ is equicontinuous bounded in ${\cal C}^0(K, \Bbb R^n)$

### **Arzelà–Ascoli** Theorem from $\Bbb R^m$ to $\Bbb R^n$
Let $A \subseteq \Bbb{R}^m$ be compact and let $B \subseteq \mathcal C(A, \Bbb{R}^n)$. If $B$ is bounded and equicontinuous, then any sequence in $B$ has a uniformly convergent subsequence.

Thus we have a characterization of sequential compactness in $\mathcal C(A, \Bbb{R}^n)$, when $A$ is compact.