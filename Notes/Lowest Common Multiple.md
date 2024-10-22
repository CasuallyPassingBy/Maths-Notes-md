---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Greatest Common Divisor]]

Given $a, b \in \Bbb Z^*$ we can define their _least common multiple_ as the positive integer ${m = \operatorname{lcm}(a,b)}$, such that:

- $a \mid m \land b \mid m$
- if $a \mid c \land b \mid c$, then $m \le c$

### Positive Preorder Infimum
Similarly, to the greatest common divisor we can get, using the preorder structure, let ${a, b\in\Bbb Z^*}$ let $m = \operatorname{lcm}(a,b)$ iff:
- $m > 0$
- $a \mid m \land b \mid m$
- if $a \mid c \land b \mid c$, then $m \mid c$

Given two positive integers $a, b$ then: $\operatorname{lcm}(a,b) \gcd(a,b) = ab$, which is really useful to calculate the $\operatorname{lcm}(a,b)$.

_Corollary:_ Given positive integers $a, b$ then $\operatorname{lcm}(a,b) = ab$ iff $\gcd(a,b) = 1$.

Similarly we can define the _least common multiple_ of $n$ numbers as: ${\operatorname{lcm}(a)_{i =1}^n = \operatorname{lcm}(\operatorname{lcm}(a)_{i=1}^{n-1}, a_n)}$.