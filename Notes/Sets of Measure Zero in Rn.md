---
tags:
  - VectorAnalysis
  - RealAnalysis
---
Subjects: [[Real Analysis]], [[Vector Analysis]]
Links: [[Jordan Measure]], [[Riemann Integral in Rn]], [[Riemann Integral in R]]

**Def:** Let $A \subseteq \Bbb R^n$ . $A$ has **Lebesgue measure** $0$ (denoted $\lambda(A) = 0$) if for any $\varepsilon>0$, there’s a countable family of rectangles $\{R_i\}_{i \in \Bbb N}$ such that:
- $A \subseteq \bigcup_{k \in \Bbb N} R_k$
- $\sum_{k \in \Bbb N} m(R_k) < \varepsilon$

**Prop:** Let $A\subseteq \Bbb R^n$ has $\lambda(A) = 0$, then if $B \subseteq A$, $\lambda(B) = 0$.

**Prop:** If $A\subseteq \Bbb R^n$ such that $\lambda(A) = 0$, then $\text{int}(A) = \varnothing$. 

**Lemma:** Suppose $A\subseteq \Bbb R^n$ is a compact subset whose intersection with $\{c\}\times \Bbb R^{n-1}$ has $(n-1)$-dimensional measure zero for every $c\in \Bbb R$. Then $A$ has $n$-dimensional measure zero, 

**Cor:** Any proper affine subspace of $\Bbb R^n$ has measure zero in $\Bbb R^n$.

**Prop:** Suppose $A$ is an open or closed subset of $\Bbb R^{n-1}$ or $\Bbb H^{n-1}$, and $f: A \to \Bbb R$ is a continuous function. Then the graph of $f$ has measure zero in $\Bbb R^n$. 

**Prop:** Let $A \subseteq \Bbb R^n$, be at most numerable then $\lambda(A) =0$

**Prop:** Let $R \subseteq\Bbb R^n$ be a rectangle with $m(R) >0$, then $\lambda(R) \ne 0$.

**Prop:** Let $\{S_i \subseteq \Bbb R^n\mid i \in \Bbb N\}$ be a collection such that $\lambda(S_i)=0$, for any $i \in \Bbb N$. Then ${S = \bigcup_{i \in \Bbb N} S_i}$, $\lambda(S) = 0$.

**Prop:** Let $A \subseteq \Bbb R^n$. $\lambda(A)$ iff for any $\varepsilon > 0$, iff there exists a countable open rectangles $\{R_i\}_{i \in \Bbb N}$ such that
- $A \subseteq \bigcup_{k \in \Bbb N} R_k$
- $\sum_{k \in \Bbb N} m(R_k) < \varepsilon$

### Lebesgue Criterion for Integrability
Let $f:R\subseteq \Bbb R^n\to \Bbb R$ be bounded over the rectangle $R$. $f$ is integrable over $R$ iff the set of discontinuities of $f$ over $R$, $D(f, R)$ has Lebesgue measure $0$, i.e. $\lambda(D(f, R)) = 0$.

**Lemma:** A subset $A\subseteq \Bbb R^n$ has measure zero iff for every $\varepsilon>0$ can be covered by a countable collection of open balls, the sum of whose Jordan-measure is less than $\varepsilon$. 

**Prop:** Suppose $A\subseteq \Bbb R^n$ has measure zero and $F: A \to \Bbb R^n$ is a smooth map. Then $F[A]$ has measure $0$.

**Lemma:** Suppose $F: U \to \Bbb R^n$ is a smooth map, where $U$ is an open subset of $\Bbb R^m$ and $m<n$. Then $F[U]$ has measure zero in $\Bbb R^n$.