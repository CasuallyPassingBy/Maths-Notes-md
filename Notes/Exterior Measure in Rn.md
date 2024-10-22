---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Darboux Sums in Rn]], [[Cubes in Rn]]

A rectangle $R$ in $\Bbb R^n$ is given by the product of $n$ one-dimensional closed and bounded intervals: $$R = \prod_{i = 1}^n[a_i, b_i]$$
where $a_i \le b_i$ are real numbers, $1\le i \le n$. We say that the *volume* of the rectangle $R$ is denoted as $|R|$, $m_*(R)$, or just $m(R)$ and it is defined to be $$m(R) = \prod_{i = 1}^n (b_i -a_i)$$
Also a *cube* is a rectangle for which $b_i - a_i = c$ for all $1 \le i \le n$. So if $Q$ is a cube in $\Bbb R^n$ is a cube of common side length $\ell$, then $m(Q) = \ell^n$.

A union of rectangles is said to be *almost disjoint* if the interiors of the rectangles are disjoint. 

**Lemma:** If a rectangle is the almost disjoint union of finitely many other rectangles, say $R = \bigcup\limits_{k = 1}^N R_k$, then $$m(R) = \sum_{k = 1}^N m(R_k)$$
**Lemma:** If $R, R_1, R_2, \dots, R_N$ are rectangles, and $R \subseteq \bigcup_{k = 1}^n R_k$, then $$m(R) \le \sum_{k = 1}^N m(R_k)$$
**Th:** Every open subset $U$ of $\Bbb R$ can be written uniquely as a countable union of disjoint open intervals. 

This a related to the fact that of $\Bbb R$ is a [[Separable, First and Second Countable Spaces|second-countable topological sapce]]

**Th:** Every open subset $U$ of $\Bbb R^n$, $n \ge 1$, can be written as a countable union of almost disjoint closed cubes

# Exterior Measure
