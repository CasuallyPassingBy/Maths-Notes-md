---
tags:
  - "#NonLinearProgramming"
---
Subjects: [[Nonlinear Programming]]
Links: [[Rn]], [[Connected Sets in Rn]], [[Regular Open and Closed Sets]]

**Def:** A set $S$ in $\Bbb R^n$ is said to be *convex* if the *l*line *segment* joining any two points of the set also belongs to the set. In other words, if $x_1, x_2 \in S$, then $t x_1 + (1-t)x_2 \in S$ for each $t\in [0, 1].$ Weighted averages of the form $t x_1 + (1-t)x_2$, where $t\in [0, 1]$, are referred to as *convex combinations* of $x_1$ and $x_2$. Inductively, the weighted averages of the form $\sum_{i = 1}^k \lambda_i x_i$, where $\sum_{j = 1}^k \lambda_i = 1$, $\lambda_i \ge 0$ for $i = 1, \dots, k$, are also called *convex combinations* of $x_1, \dots x_k$. If we drop the requirement of nonnegativity on the multipliers $\lambda_j$, then the combination $\sum_{i = 1}^k \lambda_i x_i$ is called an *affine combination*. 

**Def:** 
- If $S := \{x \in \Bbb R^n\mid p^\top x = \alpha\}$ is called a *hyperplane in $\Bbb R^n$*, where $p$ is a nonzero vector in $\Bbb R^n$, usually referred to as the *gradient*, of *normal* to the hyperplane, and a $\alpha$ a scalar. 
- If $S := \{x \in \Bbb R^n\mid p^\top x \le \alpha\}$ is called a *half-space* in $\Bbb R^n$.
- The set $S := \{x \in \Bbb R^n\mid Ax \le b\}$ is a convex set, where $A$ is an $m \times n$ matrix and $b$ is an $m$-vector. This set is the intersection of $m$ half-spaces and is usually called a *polyhedral set*. 
**Lemma:** Let $S_1$ and $S_2$ be convex sets in $\Bbb R^n$. Then:
- $S_1 \cap S_2$ is convex. This can be strengthen to arbitrary intersection of convex set
- $S_1 + S_2 = \{x_1 + x_1\mid x_1 \in S_1, x_2 \in S_2\}$ is convex. 
- $S_1 - S_2 = \{x_1 - x_2 \mid x_1 \in S_1, x_2 \in S_2\}$ is convex. 

**Def:** Let $S \subseteq \Bbb R^n$. The *convex hull* of $S$, denoted as $\text{conv}(S)$, is the collection of al convex combinations of $S$. In other words $x \in \text{conv}(S)$ iff there exist a $k \in \Bbb N$ such that $x_1, \dots, x_k \in S$ $\lambda_1, \dots, \lambda_k\in \Bbb R^{\ge 0}$ such that$$x = \sum_{i = 1}^k \lambda_i x_i, \qquad \sum_{i = 1}^k \lambda_i = 1$$
**Lemma:** Let $S \subseteq \Bbb R^n$. The $\text{conv}(S)$ is the smallest convex set containing $S$. Indeed $\text{conv}(S)$ is the intersection of all convex sets containing $S$. 

**Def:** The convex hull of a finite number of points $x_1, \dots, x_k \in \Bbb R^n$ is called a *polytope*. If $x_1 \dots, x_k$, and $x_{k+1}$ are *affinely independent* which means that $x_2 - x_1, x_3 - x_1, \dots, x_{k+1} - x_1$ are linearly independent, then $\text{conv}(x_1, \dots, x_{k+1})$, the convex hull of $x_1, \dots, x_{k+1}$ is called a *simplex* having vertices $x_1, \dots, x_{k+1}$. 

**Th:** Let $S \subseteq \Bbb R^n$ be a convex set with nonempty interior. Let $x\in \text{cl}(S)$ and $y\in \text{int}(S)$. Then $\lambda x_1 + (1-\lambda)x_2\in \text{int}(S)$ for each $\lambda \in (0, 1)$. 

**Cor:** If $S \subseteq \Bbb R^n$ is a convex set, then $\text{int}(S)$ is convex. 

**Cor:** If $S \subseteq \Bbb R^n$ is a convex set with nonempty interior, then $\text{cl}(S)$ is convex. 

**Cor:** If $S \subseteq \Bbb R^n$ is a convex set with nonempty interior, then $\text{cl}(\text{int}(S)) = \text{cl}(S)$. Meaning that closed convex set with nonempty interior are regularly closed.

**Cor:** If $S \subseteq \Bbb R^n$ is a convex set, then $\text{int}(\text{cl}(S)) = \text{int}(S)$. 