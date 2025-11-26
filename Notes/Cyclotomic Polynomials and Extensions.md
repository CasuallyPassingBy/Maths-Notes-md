---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]]

**Def:** Let $\mu_n$ denote the *group of $n$th roots of unity* over $\Bbb Q$. 

**Def:** A generator of the cyclic group $\mu_n$ is called a *primitive $n$th roots of unity*. Let $\zeta_n$ be the a primitive $n$th root of unity. 

**Obs:** Suppose $m$ and $n$ are relatively prime positive integers. Then $\zeta_m \zeta_n$ is a primitive $mn$th root of unity. If $\zeta_n$ is a primitive $n$th root of unity, and $d$ is divisor of $n$, then $\zeta_n^d$ is a primitive $(n/d)$th root of unity. 

**Def:** We define the $n$th cyclotomic polynomial $\Phi_n(x)$ to be the polynomial whose rors are the primitive $n$th roots of unity $$\Phi_n(x) := \prod_{\zeta \text{ primitive }\in \mu_n}(x-\zeta) = \prod_{\substack{1 \le a <n \\ (a, n) = 1}} (x-\zeta_n^a),$$which has degree $\varphi(n)$, where $\varphi(n)$ is the [[Euler totient function]]. 

**Obs:** Let $n$ be a positive integer, then $$x^n-1 = \prod_{d \mid n}\Phi_d(x).$$This is equivalent to $$n = \sum_{d\mid n}\phi(d) $$
**Lemma:** The cyclotomic polynomial $\Phi_n(x)$ is a monic polynomial in $\Bbb Z[x]$ of degree $\varphi(n)$. 

**Prop:** The cyclotomic polynomial $\Phi_n$ is an irreducible monic polynomial in $\Bbb Z[x]$ of degree $\varphi(n)$. 

**Prop:** If $n$ is an odd integer, then $\Phi_{2n}(x) = \Phi_n(-x)$. 

**Def:** The field $\Bbb Q(\zeta_n)$ is called the *cyclotomic field of $n$th roots of unity.* 

**Cor:** The degree over $\Bbb Q$ of the cyclotomic field of $n$th roots of unity is $\varphi(n)$: $$[\Bbb Q(\zeta_n) : \Bbb Q] = \varphi(n). $$
**Prop:** If $K/\Bbb Q$ is a finite field extension, then $K$ has only a finite number of roots of unity. 

**Prop:** We can use the [[Möbius Function and Inversion Formula#Möbius Inversion formula|Möbius inversion formula]] to get the following formula: $$\Phi_n (x):= \prod_{d \mid n }(x^d-1)^{\mu(n/d)}.$$

**Prop:** Let $\ell$ be a prime, and let $\Phi_\ell (x) = (x^\ell-1)/(x-1)\in \Bbb Z[x]$. We want to determine the factorisation of $\Phi_\ell(x)$ modulo $p$ for any prime $p$. Let $\zeta$ denote any fixed primite $\ell$th root of unity.
- If $p = \ell$, then $\Phi_\ell(x) = (x-1)^{\ell-1}\in (\Bbb Z/\ell \Bbb Z)[x]$.
- Suppose $p \neq \ell$, and let $f$ denote the order of $p \mod \ell$. The smallest power of $p$ with $p^f \equiv 1 \pmod \ell$. We know that $\mathbb F_{p^n}$ is cyclic, then $n = f$ is the smallest power $p^n$ of $p$ with $\zeta \in \Bbb F_{p^n}$. This means that the minimal polynomial of $\zeta$ over $(\Bbb Z/p\Bbb Z)[x]$ has degree $f$. 
- We see that $(\Bbb Z/p\Bbb Z)(\zeta) = (\Bbb Z/p\Bbb Z)(\zeta^a)$ for any $a$ that is not divisible by $\ell$. Finally, we see that $\Phi_\ell(x)$ is the product of $(\ell-1)/f$ distinct irreducible polynomials of degree $f$in $(\Bbb Z/p\Bbb Z)[x]$. 

We can get a weakened version of [[Prime Numbers#Dirichlet’s Theorem|Dirichlet's Theorem on Primes in Arithmetic Progressions]], but without the machinery that are [[Dirichlet L-functions]]. 

**Lemma:** Given any monic polynomial $p(x)\in \Bbb Z[x]$ of degree at least one there are infinitely many distinct prime divisors of the integers $$\{p(n) \mid n \in \Bbb N^+\}.$$

**Lemma:** Let $p$ be a prime and $m$ an integer such that $p \not\mid m$. If $a$ is an integer such that $\Phi_m(a) \equiv 0 \pmod p$, then $(a, p) = 1$, and the order of $a$ in $(\Bbb Z/p\Bbb Z)^\times$ is $m$. 

**Cor:** Let $a\in \Bbb Z$. If $p$ is an odd prime that divides $\Phi_m(a)$, then either $p$ divides $m$ or $p \equiv 1 \pmod m$. 

**Th:** For any positive integer $m$ there are infinitely many primes $p$ with $p \equiv 1 \pmod m$. 