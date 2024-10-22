---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
**********Def:********** A cube in $\Bbb R^n$ is a rectangle $C \subseteq \Bbb R^n$ with all of its dimensions being equal, i.e. ${C = \prod_{i = 1}^n}[a_i, b_i]$, then for any $1\le i, j\le n$, $(b_j-a_j) = (b_i - a_i)$. The value ${s = b_i-a_i}$ is called the cube’s dimension.

************Prop:************ If $C = \prod_{i = 1}^n [a_i, b_i]$ is a cube with dimension $s$ and center $c = (c_i)_{i = 1}^n \in C$, then ${c_i = a_i + \frac{s}{2}}$ for all $i$ , and the diagonal of $C$ has length of $s\sqrt{n}$, i.e. $d(C) = s\sqrt{n}$

************Prop:************ Let $R = \prod_{i = 1}^n[a_i,b _i]$ be a rectangle with rational dimensions, then there’s a partition of $R$ of cubes, with the same rational dimension.

This can be made stronger into a version where the dimension of the cubes can be arbitrarily small dimension, while preserving the rationality of the dimension.

**************Lemma:************** Let $R_1, \dots, R_k \subseteq \Bbb R^n$ are rectangles, for any $\varepsilon >0$ exists a finite amount of cubes ${C_1, \dots, C_l}$ with rational dimensions that

$$ \bigcup _{j = 1}^k R_j \subseteq \bigcup_{i = 1}^l C_i $$

and

$$ 0 \le \sum_{i = 1}^l m(C_i) - \sum_{j = 1}^k m(R_j) < \varepsilon $$