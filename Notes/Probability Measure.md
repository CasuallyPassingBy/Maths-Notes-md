---
tags:
  - "#ProbabilityTheory"
---
Subjects: [[Probability Theory]]
Links: [[Sigma Algebra]], [[Measure]]

********Def:******** Let $(\Omega, \mathscr F)$ is a [[Measurable Spaces|measurable space]]. A probability measure is a function $P: \mathscr F\to [0,1]$, that satisfies
- $P(\Omega)= 1$
- $P(A) \ge0$ for any $A \in \mathscr F$
- If $A_1, A_2, \dots\in \mathscr F$ are mutually disjoint, $A_n \cap A_m = \varnothing$ for ${n \Bbb Ne m}$, then$$ P\left(\bigcup_{n = 1}^\infty A_n\right) = \sum_{n = 1}^\infty P(A_n) $$

We say that the triple $(\Omega, \mathscr F, P)$ we call it a probability space

**Prop:** Let $(\Omega, \mathscr F, P)$ be a probability space, the
- $P (\varnothing ) = 0$
- If $A_1, \dots, A_n \in \mathscr F$, are mutually disjoint, then$$ P\left(\bigcup_{k = 1}^n A_k\right)=\sum_{k = 1}^n P(A_k) $$
- $P(\Omega\setminus A) = 1-P(A)$
- If $A\subseteq B$, then $P(B\setminus A) = P(B) -P(A)$
- If $A\subseteq B$, then $P(A) \le P(B)$
- $0 \le P(A) \le 1$
- $P(A \cup B) = P(A)+ P(B) -P(A \cap B)$
- $P(A\cup B) \le P(A) + P(B)$

**Prop (Boole’s Inequalities):** Let $(A_n) _{n \in \Bbb N}$ be a sequence of events, then
$$ P\left( \bigcup_{n \in \Bbb N}A_n \right) \le \sum_{n \in \Bbb N} P(A_n) $$
$$ P\left( \bigcap_{n \in \Bbb N}A_n \right) \ge 1-\sum_{n \in \Bbb N} P(\Omega\setminus A_n) $$

**Prop:** The probability measure $P$, of the probability space $(\Omega, \mathscr F, P)$ is continuous, meaning that if we have a _monotone sequence of events_ $(A_n ) _{n \in \Bbb N}$, then
$$ \lim_{n \to \infty } P(A_n) = P\left(\lim_{n \to \infty} A_n\right) $$