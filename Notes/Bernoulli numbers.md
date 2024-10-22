---
tags:
  - "#SpecialNumbers"
---
Subjects: [[Special Numbers]]
Links: [[Bernoulli Polynomials]]

There are a lot of definitions of the Bernoulli numbers, but the one that i will use for the moment is this one, $$\frac{z}{e^z-1} = \sum_{n = 0}^\infty \frac{B_n}{n!}z^n$$
We see that is analytic at $0$ since it has a removable singularity. 

We can calculate a couple of values:
- $B_0 = 1$ 
- $B_1 = -1/2$ 
- $B_2 = 1/6$
- $B_3 = 0$
- $B_4 =-1/30$
- $B_5 = 0$

We have that for $n\ge 1$: $$ B_n = -\frac{1}{n+1}\sum_{k = 0}^{n-1}{n+1\choose k} B_k$$
We also have the neat property that for $n \ge 1$, then $$B_{2n+1} = 0$$and that $$z \cot z =  \sum_{n = 0}^\infty (-1)^n \frac{2^{2n}B_{2n}}{(2n)!}z^{2n}$$from this we get the result: $$z \coth z =  \sum_{n = 0}^\infty \frac{2^{2n}B_{2n}}{(2n)!}z^{2n}$$
along with using that $$z\cot z = 1+2\sum_{n = 1}^\infty \frac{z^2}{z^2-n^2\pi ^2}$$, we can actually get that, where $\zeta$ represent the [[Riemann Zeta Function]] $$z\cot z =1-2\sum_{n = 1}^\infty \frac{\zeta(2n)}{\pi^{2n}}z^{2n}$$
Getting the result that $$\zeta(2n) = (-1)^{n+1}\frac{(2\pi)^{2n}B_{2n}}{2(2n)!}$$
We have that Ross Tang have an explicit formula for the Bernoulli numbers:
$$ B_{2n} = \frac{2n}{2^{2n}-4^{2n}}\sum_{k = 1}^{2n}\sum_{j = 0}^k \frac{(-1)^j (k-2j)^{2n}}{2^ki^kk}$$the explicit formula that appears on Wikipedia is $$B_m = \sum_{k=0}^m \frac1{k+1} \sum_{j=0}^k \binom{k}{j} (-1)^j j^m$$
If we recall the identity $$2\coth(2z)-\coth z = \tanh z$$Then we can get the identity $$\tanh z = \sum_{n = 1}^\infty \frac{4^n(4^n -1)B_
2n}{(2n)!}z^{2n-1}$$if we add that $\tan z = -i \tanh(iz)$, then $$\tan z = \sum_{n = 1}^\infty (-1)^{n-1}\frac{4^n(4^n -1)B_2n} {(2n)!}z^{2n-1} $$