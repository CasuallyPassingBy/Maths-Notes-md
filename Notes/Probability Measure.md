---
tags:
  - "#ProbabilityTheory"
---
Subjects: [[Probability Theory]]
Links: [[Rings and Algebras of Sets]], [[Measures]], [[Measure Spaces and Measurable Spaces]]

********Def:******** Let $(\Omega, \mathscr A)$ is a [[Rings and Algebras of Sets|measurable space]]. A probability measure is a function $\Bbb P: \mathscr A\to [0,1]$, that satisfies
- $\Bbb P(\Omega)= 1$
- $\Bbb P(A) \ge0$ for any $A \in \mathscr A$
- If $A_1, A_2, \dots\in \mathscr A$ are mutually disjoint, $A_n \cap A_m = \varnothing$ for $n \ne m$, then$$ \Bbb P\left(\bigcup_{n = 1}^\infty A_n\right) = \sum_{n = 1}^\infty \Bbb P(A_n) $$
We say that the triple $(\Omega, \mathscr A, P)$ we call it a probability space. We can write this as $(\Omega, {\scr A}, P)$ is a measure space and $\Bbb P(X) = 1$. The elements of $\Omega$ are called *elementary outcomes* or the *sample points* of our experiment, then the members of $\scr A$ are called *events*, then $P(A)$ is the *probability* of the event $A$.

**Prop:** Let $(\Omega, \mathscr A, P)$ be a probability space, the
- $\Bbb P (\varnothing ) = 0$
- If $A_1, \dots, A_n \in \mathscr A$, are mutually disjoint, then$$ \Bbb P\left(\bigcup_{k = 1}^n A_k\right)=\sum_{k = 1}^n \Bbb P(A_k) $$
- $\Bbb P(\Omega\setminus A) = 1-\Bbb P(A)$
- If $A\subseteq B$, then $\Bbb P(B\setminus A) = \Bbb P(B) -\Bbb P(A)$
- If $A\subseteq B$, then $\Bbb P(A) \le \Bbb P(B)$
- $0 \le \Bbb P(A) \le 1$
- $\Bbb P(A \cup B) = \Bbb P(A)+ \Bbb P(B) -\Bbb P(A \cap B)$
- $\Bbb P(A\cup B) \le \Bbb P(A) + \Bbb P(B)$

**Prop (Boole’s Inequalities):** Let $(A_n) _{n \in \Bbb N}$ be a sequence of events, then
$$ \Bbb P\left( \bigcup_{n \in \Bbb N}A_n \right) \le \sum_{n \in \Bbb N} \Bbb P(A_n) $$
$$ \Bbb P\left( \bigcap_{n \in \Bbb N}A_n \right) \ge 1-\sum_{n \in \Bbb N} \Bbb P(\Omega\setminus A_n) $$

**Prop:** The probability measure $P$, of the probability space $(\Omega, \mathscr A, P)$ is continuous, meaning that if we have a _monotone sequence of events_ $(A_n ) _{n \in \Bbb N}$, then
$$ \lim_{n \to \infty } \Bbb P(A_n) = \Bbb P\left(\lim_{n \to \infty} A_n\right) $$