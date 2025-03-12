---
tags:
  - SetTheory
  - MeasureTheory
---
Subjects: [[Set Theory]], [[Measure Theory]]
Links: [[Natural Numbers]], [[Basic Set Theoretic Operations]]

**Def:** Let $(A_n)_{n < \omega}$ be a sequence of subsets of $X$. We define the *limit superior of* $A_n$ as $$ \limsup_{n \to \infty} A_n :=\bigcap_{n = 1}^\infty \bigcup_{k =n }^\infty A_k,$$similarly we define the *limit inferior of* $A_n$ as $$ \liminf_{n \to \infty} A_n := \bigcup_{n = 1}^\infty \bigcap_{k =n }^\infty A_k $$
In general, we have that $\liminf\limits_{n \to \infty} A_n \subseteq \limsup\limits_{n \to \infty} A_n$. 

**Obs:** We have that both the limit superior and limit inferior of a sequence of sets always exists since they are bounded by $X$ and $\varnothing$. 

**Def:** Let a sequence of sets $(A_n ) _{n < \omega}$. If there’s an set $A$ such that$$ \limsup_{n \to \infty }A_n = \liminf_{n \to \infty} A_n = A $$then, we say the sequence converges to $A$, and it’s written as $\lim_{n \to \infty }A_n = A$

**Def:** Let $(A_n)_{n < \omega}$  be a sequence such that:
- $A_n \subseteq A_m$ for $n < m$, then the sequence is *increasing*.
- $A_n \supseteq A_m$ for $n < m$, then the sequence is *decreasing*.
If a sequence is either increasing or decreasing, then it is called *monotone*.

**Prop:** If $(A_n)_{n <\omega}$ is a increasing sequence, then $$\lim\limits_{n \to \infty} A_n = \limsup\limits_{n \to \infty} A_n = \bigcup_{n < \omega} A_n.$$If $(A_n)_{n <\omega}$ is a decreasing sequence, then $$\lim\limits_{n \to \infty} A_n = \liminf\limits_{n \to \infty} A_n = \bigcap_{n < \omega} A_n.$$  