---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Euclidean Algorithm#Division Algorithm|Division Algorithm]], [[Greatest Common Divisor]]

**Alg:** Let $N$ be a positive integer and $b > 1$. We apply the division algorithm yields the integers $q_1$ and $a_0$ satisfying

$$ N= q_1 b+a_0 \quad 0\le a_0 <b $$

If $q_1 \ge b$, we can divide it once more, obtaining

$$ q_1 = q_2 b+a_1 $$

Now substitute $q_1$ into the earlier equation:

$$ N= q_2 b^2 +a_1 b+a_0 $$

As long $q_2 \ge b$, we can continue in the same fashion. We know that $N >q_1 >q_2> \cdots \ge 0$ is a strictly decreasing sequence of integers, this process must terminate, say at the $(m-1)$th stage, where

$$ q_{m-1} = q_m b+a_{m-1} \quad 0\le a_{m-1} <b $$

and $0 \le q_m < b$. Setting $a_m = q_m$, we reach the representation:

$$ N = a_mb^m + a_{m-1}b^{m-1}+\cdots+a_1b+a_0 = \sum_{k =0}^m a_k b^k $$

which is a unique representation of $N$ since we used the division algorithm. This can summarized into the notation:

$$ N=(a_ma_{m-1} \cdots a_2 a_1 a_0)_b $$

We can call this the ****_base $b$ place-value notation for $N$._

### Divisibility Rules

********Th:******** Let $N = (a_m a_{m-1} \cdots a_2 a_1 a_0)_{b}$, then $S= a_m + a_{m-1}+\cdots +a_1 +a_0$. Then ${b-1 \mid N}$ iff $b-1 \mid S$.

********Th:******** Let $N = (a_m a_{m-1} \cdots a_2 a_1 a_0)_{b}$, then $T= a_0 - a_{1}+\cdots +(-1)^m a_m$. Then ${b+1 \mid N}$ iff $b+1 \mid T$.