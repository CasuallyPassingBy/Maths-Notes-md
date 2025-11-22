---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]]

**Def:** Let $\mu_n$ denote the *group of $n$th roots of unity* over $\Bbb Q$. 

**Def:** A generator of the cyclic group $\mu_n$ is called a *primitive $n$th roots of unity*. Let $\zeta_n$ be the a primitive $n$th root of unity. 

**Obs:** Suppose $m$ and $n$ are relatively prime positive integers. Then $\zeta_m \zeta_n$ is a primitive $mn$th root of unity. 

**Def:** We define the $n$th cyclotomic polynomial $\Phi_n(x)$ to be the polynomial whose rors are the primitive $n$th roots of unity $$\Phi_n(x) := \prod_{\zeta \text{ primitive }\in \mu_n}(x-\zeta) = \prod_{\substack{1 \le a <n \\ (a, n) = 1}} (x-\zeta_n^a),$$which has degree $\varphi(n)$, where $\varphi(n)$ is the [[Euler totient function]]. 

**Obs:** Let $n$ be a positive integer, then $$x^n-1 = \prod_{d \mid n}\Phi_d(x).$$This is equivalent to $$n = \sum_{d\mid n}\phi(d) $$
**Lemma:** The cyclotomic polynomial $\Phi_n(x)$ is a monic polynomial in $\Bbb Z[x]$ of degree $\varphi(n)$. 

**Prop:** The cyclotomic polynomial $\Phi_n$ is an irreducible monic polynomial in $\Bbb Z[x]$ of degree $\varphi(n)$. 

**Def:** The field $\Bbb Q(\zeta_n)$ is called the cyclotomic field of $n$th roots of unity. 

**Cor:** The degree over $\Bbb Q$ of the cyclotomic field of $n$th roots of unity is $\varphi(n)$: $$[\Bbb Q(\zeta_n) : \Bbb Q] = \varphi(n). $$

