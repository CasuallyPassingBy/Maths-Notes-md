---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Probability Measure]]

********Def:******** Let a sequence of events $(A_n ) _{n \in \Bbb N}$, is defined the limit superior and the limit inferior as

$$ \limsup_{n \to \infty} A_n :=\bigcap_{n = 1}^\infty \bigcup_{k =n }^\infty A_k $$

$$ \liminf_{n \to \infty} A_n := \bigcup_{n = 1}^\infty \bigcap_{k =n }^\infty A_k $$

We can see that $\liminf\limits_{n \to \infty} A_n \subseteq\limsup\limits_{n \to \infty} A_n$ .

********Def:******** Let a sequence of events $(A_n ) _{n \in \Bbb N}$. If there’s an event $A$ such that

$$ \limsup_{n \to \infty }A_n = \liminf_{n \to \infty} A_n = A $$

then, we say the sequence converges to $A$, and it’s written as $\lim_{n \to \infty }A_n = A$

************Prop:************ Let a sequence of events $(A_n ) _{n \in \Bbb N}$ be a monotone sequence of events

- If $A_k \subseteq A_{k+1}$, for all $k \in \Bbb N$, then $\lim_{n \to \infty} A_n = \bigcup_{n \in \Bbb N} A_n$
- If $A_k \supseteq A_{k+1}$, for all $k \in \Bbb N$, then $\lim_{n \to \infty} A_n = \bigcap_{n \in \Bbb N} A_n$

**********Prop:********** Let a sequence of events $(A_n ) _{n \in \Bbb N}$. We define the sequence

$$ B_0 = A_0 \quad \text{and} \quad B_n = A_n \setminus \left(\bigcup_{k =0}^{n-1}A_k\right) $$

Then the sequence of events $(B_n ) _{n \in \Bbb N}$ satisfies:

- $B_n \subseteq A_n$
- $B_n \cap B_m = \varnothing$, if $n \Bbb Ne m$
- $\bigcup_{n \in \Bbb N} B_n = \bigcup_{n \in \Bbb N} A_n$