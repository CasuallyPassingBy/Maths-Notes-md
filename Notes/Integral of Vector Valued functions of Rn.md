---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]]
Links: [[Integral of Vector Valued functions of R]], [[Riemann Integral in Rn]], [[Integral over Jordan-measurable Sets]]

If $D\subseteq \Bbb R^n$ is a domain of integration and $F: D \to \Bbb R^k$ is a bounded continuous vector valued function, we define the integral of $F$ over $D$ to be the vector in $\Bbb R^k$ obtained by integrating $F$ component by component: $$\int_D F := \left(\int_D F_1, \dots, \int_D F_k\right)$$

**Lemma:** Suppose $D\subseteq \Bbb R^n$ is a domain of integration and $F: D\to \Bbb R^k$ is a bounded continuous vector-valued function. Then $$\left\|\int_D F\right\| \le \int_D \|F\|.$$

**Lipschitz Estimate for ${\cal C}^1$ Functions:** Let $U\subseteq \Bbb R^n$ be an open set, and let $F:U \to \Bbb R^m$ be of class ${\cal C}^1$. Then $F$ is Lipschitz continuous on any compact convex subset $B\subseteq U$. The Lipschitz constant can be taken to be $\sup_{x\in B}\|dF_x\|$, where $\|dF_x\|$ is the Euclidean norm of the matrices,