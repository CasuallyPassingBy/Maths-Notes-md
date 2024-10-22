---
tags:
  - NumberTheory
  - AnalyticNumberTheory
---
Subjects: [[Elementary Number Theory]], [[Analytic Number Theory]]

Links: [[Multiplicative Functions]], [[Möbius Function and Inversion Formula]], [[Fermat's Little Theorem]], [[Integers modulo n]]

**********Def:********** Let $\phi$ be an arithmetic functions that counts the number of numbers relatively prime of $n$, less than $n$, in other words,

$$ \phi(n) = \sum_{\substack{1\le k \le n \\ \\ \gcd(k, n)}} 1 $$

********Th:******** If $p$ is a prime and $k >0$, then

$$ \phi(p^k) = p^k\left(1-\frac{1}{p}\right) = p^k-p^{k-1} $$

**************Lemma:************** Given the integers $a, b , c$, $\gcd(a,bc)=1$ iff $\gcd(a,b) =1$ and $\gcd(a,c)=1$

********Th: $\phi$** is a multiplicative function

******Cor:****** Let $n = p_1^{k_1}p_2^{k_2}\cdots p_r^{k_r}$ is the prime factorization of $n>1$ then

$$ \phi(n) = n \prod_{i = 1}^r \left(1-\frac{1}{p_i}\right) = n \prod_{p\mid n} \left(1-\frac{1}{p}\right) $$

**********Th (Gauss):********** For each $n \ge1$ ********************

$$ \operatorname{Id}(n)= n = \sum_{d\mid n}\phi(d) = (\phi * 1) $$

and

$$ \phi(n) = \sum_{d\mid n}\mu(d) \left(\frac{n}{d}\right) = (\mu * \operatorname{Id})(n) $$

******Cor:****** For each $n \ge 1$ ************

$$ \sum_{k = 1}^n \gcd(k,n) = \sum_{d \mid n} d\phi\left(\frac{n}{d}\right) = n \sum_{d \mid n} \frac{\phi(d)}{d} = (\phi* \operatorname{Id})(n) $$

and

$$ \phi(n) = \sum_{k = 1}^n \gcd(n,k)\omega_n^k $$

where $\omega_n = e^{\frac{2\pi i }{n}}$

- Properties:
    
    $\phi(mn) = \phi(m)\phi(n) \frac{d}{\phi(d)}$ where $d = \gcd(m,n)$
    
    $a \mid b$ implies that $\phi(a) \mid \phi(b)$
    
    $\phi(n)$ is even for $n \ge 3$. Moreover, if $n$ has $r$ distinct odd prime factors, then $2^r \mid \phi(n)$
    

**********Def:********** A _**********************reduced residue system**********************_ modulo $n$ is a set $\{b_1, \dots, b_{\phi(n)}\} \subseteq \Bbb Z$, such that for any $b_i$ $\gcd(b_i, n) =1$, and if $i \ne j$, then $b_i \not\equiv b_j \pmod n$.

**************Lemma:************** Let $\{b_1, \dots, b_{\phi(n)}\}$ be a reduced residue system modulo $n$ and $a \in \Bbb Z$ be such that $\gcd(a,n) =1$, then $\{ab_1, \dots, ab_{\phi(n)}\}$ is also a reduced residue system.

### Euler’s Theorem

If $n \ge 1$ and $\gcd(a,n) =1$ then

$$ a^{\phi(n)} \equiv 1 \pmod n $$

********Th:******** For $n >1$, the sum of the positive integers less than $n$ and relatively prime to $n$ is $\frac{1}{2}\phi(n)n$, i.e.

$$ \sum_{\substack{1 \le k \le n \\ \gcd(k,n)=1}}k = \frac{\phi(n) n}{2} $$