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

**Def:** The field $\Bbb Q(\zeta_n)/\Bbb Q$ is called the *cyclotomic field of $n$th roots of unity.* 

**Cor:** The degree over $\Bbb Q$ of the cyclotomic field of $n$th roots of unity is $\varphi(n)$: $$[\Bbb Q(\zeta_n) : \Bbb Q] = \varphi(n). $$
**Prop:** If $K/\Bbb Q$ is a finite field extension, then $K$ has only a finite number of roots of unity. 

**Prop:** We can use the [[Möbius Function and Inversion Formula#Möbius Inversion formula|Möbius inversion formula]] to get the following formula: $$\Phi_n (x):= \prod_{d \mid n }(x^d-1)^{\mu(n/d)}.$$
**Prop:** Let $\ell$ be a prime, and let $\Phi_\ell (x) = (x^\ell-1)/(x-1)\in \Bbb Z[x]$. We want to determine the factorisation of $\Phi_\ell(x)$ modulo $p$ for any prime $p$. Let $\zeta$ denote any fixed primive $\ell$th root of unity.
- If $p = \ell$, then $\Phi_\ell(x) = (x-1)^{\ell-1}\in (\Bbb Z/\ell \Bbb Z)[x]$.
- Suppose $p \neq \ell$, and let $f$ denote the order of $p \mod \ell$. The smallest power of $p$ with $p^f \equiv 1 \pmod \ell$. We know that $\mathbb F_{p^n}$ is cyclic, then $n = f$ is the smallest power $p^n$ of $p$ with $\zeta \in \Bbb F_{p^n}$. This means that the minimal polynomial of $\zeta$ over $(\Bbb Z/p\Bbb Z)[x]$ has degree $f$. 
- We see that $(\Bbb Z/p\Bbb Z)(\zeta) = (\Bbb Z/p\Bbb Z)(\zeta^a)$ for any $a$ that is not divisible by $\ell$. Finally, we see that $\Phi_\ell(x)$ is the product of $(\ell-1)/f$ distinct irreducible polynomials of degree $f$in $(\Bbb Z/p\Bbb Z)[x]$. 

We can get a weakened version of [[Prime Numbers#Dirichlet’s Theorem|Dirichlet's Theorem on Primes in Arithmetic Progressions]], but without the machinery that are [[Dirichlet L-functions]]. 

**Lemma:** Given any monic polynomial $p(x)\in \Bbb Z[x]$ of degree at least one there are infinitely many distinct prime divisors of the integers $$\{p(n) \mid n \in \Bbb N^+\}.$$

**Lemma:** Let $p$ be a prime and $m$ an integer such that $p \not\mid m$. If $a$ is an integer such that $\Phi_m(a) \equiv 0 \pmod p$, then $(a, p) = 1$, and the order of $a$ in $(\Bbb Z/p\Bbb Z)^\times$ is $m$. 

**Cor:** Let $a\in \Bbb Z$. If $p$ is an odd prime that divides $\Phi_m(a)$, then either $p$ divides $m$ or $p \equiv 1 \pmod m$. 

**Th:** For any positive integer $m$ there are infinitely many primes $p$ with $p \equiv 1 \pmod m$. 

**Th:** The Galois group of the cyclotomic field $\Bbb Q(\zeta_n)$ of $n$th roots of unity is isomorphic to the multiplicative group $(\Bbb Z/n\Bbb Z)^\times$. The isomorphism is given explicitly by the map $a \pmod n \mapsto \sigma_a$, where $\sigma_a(\zeta_n) = \zeta_n^a$. 

**Obs:** A basis for $\Bbb Q(\zeta_p)$ over $\Bbb Q$ is given by $$\zeta_p, \zeta_p^2, \dots, \zeta_p^{p-2},\zeta_p^{p-1}.$$The reason for choosing this basis is that any $\sigma$ in the Galois group $\text{Gal}(\Bbb Q(\zeta_p)/\Bbb Q)$ simply *permutes* these basis elements since these are precisely the primitive $p$ roots of unity.  This where we need that $p$ is prime. Let $H$ be any subgroup of the Galois group of $\Bbb Q(\zeta_p)$ over $\Bbb Q$ and let $$\alpha_H = \sum_{\sigma\in H} \sigma(\zeta_p), $$the sum of the conjugates by the elements in $H$. We can prove that the fixed field of $H$ is $\Bbb Q(\alpha)$. 

**Cor:** Let $n =\prod_{k = 0}^\infty p_k^{\alpha_k}$ be the prime decomposition of the positive integer $n$ into distinct prime powers. Then the cyclotomic fields $\Bbb Q(\zeta_{p_k^{\alpha_k}})$, $k \in \Bbb N$ intersect only in the field $\Bbb Q$ and their composite is the cyclotomic field $\Bbb Q(\zeta_n)$. We have $$\text{Gal}(\Bbb Q(\zeta_n)/\Bbb Q) \cong \prod_{k = 0}^\infty \text{Gal}(\Bbb Q(\zeta_{p_k^{\alpha_k}})/\Bbb Q) $$which by the we get the following isomorphism, equivalent to the [[Linear Congruences#Chinese Remainder Theorem|Chinese Remainder Theorem]]$$(\Bbb Z/n \Bbb Z)^\times \cong \prod_{k = 0}^\infty (\Bbb Z/p_k^{\alpha_k}\Bbb Z)^\times  $$
**Th:** Let $G$ be any finite abelian group. Then there is a subfield $K$ of a cyclotomic field with $\text{Gal}(K/\Bbb Q) \cong G$. 

$(*)$ **Kronecker-Weber Theorem:** Let $K$ be a finite abelian extension of $\Bbb Q$. Then $K$ is contained in a cyclotomic extension of $\Bbb Q$. 

**Prop:** Let $\zeta_n$ denote the primitive $n$th root of unity and let $K = \Bbb Q(\zeta_n)$ be the associated cyclotomic field. We see that $\text{Tr}_{K/\Bbb Q} (\zeta_n) = \mu(n),$ where $\mu$ is the [[Möbius Function and Inversion Formula|Möbius function]], and $\text{Tr}_{K/\Bbb Q}$ is the [[Linear Algebraic Invariants in Field Theory|trace of an element]].

**Prop:** The primitive $n$th roots of unity form a basis over $\Bbb Q$ for the cyclotomic field of $n$th roots of unity iff $n$ is squarefree. 

**Def:** We see that complex conjugation restricts to the automorphism $\sigma_{-1}\in \text{Gal}(\Bbb Q(\zeta_n)/\Bbb Q)$ of the cyclotomic field of $n$th roots of unity. We see that $\Bbb Q(\zeta_n + \zeta_n^{-1})$ is a subfield of the real elements of $\Bbb Q(\zeta_n)$. We call this field the *maximal real subfield of $\Bbb Q(\zeta_n)$.*

