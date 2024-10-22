---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Absolute Convergence Test and Properties]]


At first the most natural definition for an infinite product is to have a sequence $\{z_n\}_{n\in \Bbb N}$, and define
$$ \prod_{n = 1}^\infty z_n = \lim_{n \to \infty} \prod_{k = 1}^n z_k$$
but this definition has a bit of trouble since we can have a bunch of non zero terms but still 'converge' to $0$, which would be problematic, for when we want to talk about functions. 

We need to define some notation, we define the sequence of partial products as $$p_n = \prod_{k = 1}^n z_k$$
The better definitions, let $\{z_n\} \subseteq \Bbb C$  be a sequence:
- We say that $\prod\limits_{n = 1}^\infty z_n$ is **strictly convergent** if the sequence $p_n\to p \ne 0$
- We say that $\prod_{n = 1}^\infty z_n$  is **convergent**, if there's an $m \in \Bbb N$, such that $\prod\limits_{n = m+1}^\infty z_n$ is strictly convergent, and $\prod\limits_{n = 1}^\infty = z_1 \cdot z_2 \cdots z_m \prod\limits_{n = m+1}^\infty z_n$ 

Let $\{z_n\}\subseteq \Bbb C$, such that $\prod\limits_{n = 1}^\infty z_n$ converges, then
1. for every $k \in \Bbb N$, we get that $\prod\limits_{n = k+1}^\infty z_n$ is convergent, then we can define $R_k = \prod\limits_{n = k+1}^\infty z_n$ 
2. $\lim\limits_{k\to \infty} R_k =1$
3. $\lim\limits_{n \to \infty} = 1$ 

We would like to have a similar definition for absolute convergence for infinite products, what we would like is that absolute convergence $\implies$ convergence. 

The natural definition, would be $$\prod\limits_{n = 1}^\infty |z_n| $$ converges, iff $\prod\limits_{n = 1}^\infty z_n$ converges absolutely. This is wrong because, we can find some sequences that don't satisfy absolute convergence $\implies$ convergence.

Let $\prod\limits_{n = 1}^\infty z_n$ be strictly convergent, the $\lim\limits_{n \to \infty} z_n = 1$, then $\Re(z_n) \to 1$, there's $N \in \Bbb N$ such that if $n \ge N$, then $\Re(z_n) >0$. 

Let $\{z_n\}\subseteq \Bbb C$, such that for all $n \in \Bbb N$ $\Re(z_n) > 0$. We get that $\prod\limits_{n =1}^\infty z_n$ converges strictly iff $\sum\limits_{n = 1}^\infty \log(z_n)$ converges. If we look at the proof we see that $$\prod\limits_{n =1}^\infty z_n = \exp\left(\sum\limits_{n = 1}^\infty \log(z_n)\right)$$ 

With this equivalence we can now give a definition for absolute convergence:
Let $\{z_n\}\subseteq \Bbb C$ is absolutely convergent, with $\Re(z_n) > 0$ , we say that $\prod\limits_{n = 1}^\infty z_n$ converges absolutely if $\sum\limits_{n = 1}^\infty \log(z_n)$ converges absolutely.

Let $\prod\limits_{n = 1}^\infty z_n$ be absolutely convergent, if $z_n \ne 0$, then $|z_n| >0$, then $\log|z_n| = \Re(\log(z_))$, thus $|\log|z_n|| \le |\log(z_n)|$, then $\sum\limits_{n = 1}^\infty |\log|z_n||$ converges, then $\prod\limits_{n = 1}^\infty |z_n|$  converges.

Let $\{z_n\}\subseteq \Bbb C$, such that $\Re(z_n) >0$. If $\prod\limits_{n = 1}^\infty z_n$ converges absolutely and  $\{w_n\} \subseteq \Bbb C$ is a rearrangement of $\{z_n\}$, then $\prod\limits_{n = 1}^\infty w_n$ converges absolutely, and $\prod\limits_{n = 1}^\infty w_n = \prod\limits_{n = 1}^\infty z_n$. 

Let $\{z_n\}\subseteq \Bbb C$, such that $\Re(z_n) >-1$.  $\prod\limits_{n = 1}^\infty 1 + z_n$ converges absolutely iff $\sum\limits_{n = 1}^\infty z_n$ converges absolutely. 

A corollary, is that let $\{z_n\}\subseteq \Bbb C$, such that $\Re(z_n) >0$. If $\prod\limits_{n = 1}^\infty z_n$ converges absolutely iff $\sum\limits_{n = 1}^\infty z_n -1$ converges absolutely.

We get that let $\{z_n\}\subseteq \Bbb C$, if $\prod\limits_{n = 1}^\infty 1+|z_n|$ converges absolutely, then $\prod\limits_{n = 1}^\infty 1+z_n$ converges absolutely. 

If $\sum|a_n|$ converges, and $a_n \ne 1$ for all $n$, then $$\prod_{n = 1}^\infty \frac1{1-a_n}$$converges. Moreover, this product is non-zero.

