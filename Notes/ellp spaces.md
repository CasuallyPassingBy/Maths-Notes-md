---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Normed Spaces]], [[Vector Spaces]]
We can look at the space of sequences such that for $p \in [1, \infty)$, in general we can denote $x_\bullet$ to be a sequnce of real numbers (notation Wikipedia)

$$ \sum_{k = 1}^\infty |x_i|^p $$
This actually forms a infinite dimensional vector space.

converges, and it is a vector space, and it is denoted as $\ell_p$ or $\ell ^p$ denpending of who is writing, and we can define

$$ \|x_\bullet\|_p=\|(x_k)\|_p = \left(\sum_{k = 1}^\infty |x_k|^p\right)^{1/p} $$

defines a norm in $\ell^p$.

In the case where $p = \infty$, the space $\ell^\infty$ is the set of all bounded sequences of real numbers, is a vector space and

$$ \|x_\bullet\|=\|(x_k) \|_\infty = \sup_{k \ge 1} |x_k| $$

is a norm in $\ell ^\infty$.

Since they are norms, we have that
### Hölder’s Inequalities for Series

We have that for $p,q$ harmonic conjuagtes. Then if $x_\bullet \in \ell^p$ and $y_\bullet \in \ell^q$. Then

$$ \|x_\bullet y_\bullet \|_1 \le \|x_\bullet\|_p\|y_\bullet\|_q $$

### Minkowski’s Inequalities for Series

$$ \|x_\bullet +y_\bullet \|_p \le \|x_\bullet\|_p +\|y_\bullet\|_p $$

We can compare how does the $\ell^p$ spaces when varying $p$. We get that

- Let $1 \le s<r\le \infty$, then $\ell^s \subset \ell ^r$ , and for any $x_\bullet \in \ell^s$, we get that $\| x_\bullet\|_r \le \| x_\bullet\|_s$
    
- For any $1 \le p < \infty$ and $x_\bullet\in \ell^p$, we have that
    
    $$ \|x_\bullet\|_\infty = \lim_{r\to \infty}\|x_\bullet\|_r $$

# $\ell^p(\Bbb Z)$ 
This are the two sided sequences

### $\ell^2(\Bbb Z)$

The vector space $\ell^2(\Bbb Z)$ over $\Bbb C$ is the set of all (two-sided) infinite sequences of complex numbers $$(\dots, a_{-n}, \dots, a_{-1}, a_0, a_1, \dots, a_n, \dots)$$such that $$\sum_{n \in \Bbb Z}|a_n|^2 < \infty$$That is, the series converges. Addition is defined componentwise, and so is scalar multiplication. The inner product between two vectors $A = (\dots, a_{-1},a_0, a_1, \dots)$ and $B= (\dots, b_{-1}, b_0, b_1, \dots)$ is defined by the absolutely convergent series $$\langle A, B\rangle := \sum_{n \in \Bbb Z}a_n \overline{b_n}$$Thus the norm of $A$ is given by $$\|A\| = \left(\sum_{n \in \Bbb Z} |a_n|^2\right)^{1/2}$$ 