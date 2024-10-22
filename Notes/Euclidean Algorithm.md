---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Greatest Common Divisor]]

## Division Algorithm

Let $a, b \in \Bbb Z$, then there are unique $q \in \Bbb Z$ and $0\le r < |b|$ such that: $a = bq +r$, in other words:

$$ \forall a,b \in \Bbb Z \exists!q ,r \in \Bbb Z[0\le r <|b|\land a=bq+r] $$


_Lemma:_ If $a = bq +r$, then $\gcd(a,b) = \gcd(b, r)$

The Euclidean Algorithm:

Let $a, b \in \Bbb N$, such that $a < b$, applying the division algorithm successive times as:

$b = aq_1 +r_1$, with $0 < r_1 <a$

$a = r_1q_2 +r_2$, with $0 < r_2 <r_1$

$\vdots$

$r_{n-2} = r_{n-1}q_{n} + r_n$, with $0 < r_n < r_{n-1}$

$r_{n-1}= r_n q_{n+1}$, then

$\gcd(a,b) = r_n$
