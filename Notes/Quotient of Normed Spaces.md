---
tags:
  - Analysis
  - FunctionalAnalysis
---
Subjects: [[Metric and Normed Spaces]], [[Functional Analysis]]
Links: [[Quotient of Vector Spaces]], [[Complete Metric Spaces]], [[Normed Vector Spaces]]

Let $V$ be a normed space over $\Bbb R$, and $W$ be a closed linear subspace of $V$. Let $V/W$  be the quotient vector space of $V$ modulo $W$. and we define the quotient norm $\|\cdot \|_{V/W}$ , with the quotient mapping $\pi: V \to V/W$ as $\pi (x) = x + W$

$$
\|\pi(x)\|_{V/W} := \inf_{z \in W}\|x-z\|
$$

This is well-defined and it is a norm

We get that $V$ is a Banach space iff $W$ and $V/W$ are Banach Spaces, with their respective norms

**Th:** Let $V$ be a seminormed space, and $W$ be closed vector subspace of $V$, then $V/W$ is a normed space with the normed defined above. 

**Cor:** Let $V$ be a seminormed space, and $N := \{x \in V \mid \|x \| = 0\}$, then $V/N$ is a normed space. 