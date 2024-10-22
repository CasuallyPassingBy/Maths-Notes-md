---
tags:
  - Combinatorics
---
Subjects: [[Special Numbers]]
Links: [[Equivalence Relations and Partitions]]

We say that the $n$th Bell number counts the amount possible partitions can a set of $n$ elements can have, and it is denoted as $B_n$. 

We define that $B_0 = 1$, and $B_1 = 1$

We can derive a recursive formula as $$B_{n+1} = \sum_{k = 1}^n {n \choose k} B_k$$
We can look at the exponential generating function of $B_n$, and get that $$B(x) = \sum_{n = 0}^\infty \frac{B_n}{n!}x^n$$
If we differentiate it we get that $$B'(x) = B(x) e^x$$with the added constraint that $B(0) = B_0 = 1$, then we solve the differential equation getting that $$B(x) = \exp(\exp(x)-1)$$ If we expand this we get that $$B(x) = \frac1{e} \sum_{n = 0}^\infty \sum_{k = 0}^\infty \frac{k^n x^n}{k! n!}$$
Meaning that the $n$th Bell number can be calculated as $$B_n = \frac1{e} \sum_{k = 0}^\infty \frac{k^n}{k!}$$
And we can use [[Cauchy's Integral Formula]], and get that $$B_n = \frac{n!}{2\pi i e}\oint_\gamma \frac{e^{e^z}}{z^{n+1}}\ dz $$with $\gamma$ a closed simple curve that surrounds the origin. 

We can use the [[Stirling Numbers of the Second Kind]], and get a closed form $$B_n = \sum_{k = 0}^n \left\{{n \atop k}\right\} $$
