---
tags:
  - AnalyticNumberTheory
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Dirichlet Product]], [[Prime Numbers]]

**********Def:********** A **************************number-theoretic function************************** $f$ is said to _**************multiplicative**************_ if

$$ f(mn) = f(m)f(n) $$

whenever $\gcd(n,m) =1$

**********Def:********** A **************************number-theoretic function************************** $f$ is said to _**************completely multiplicative**************_ if for any $m,n$ then

$$ f(mn) = f(m)f(n) $$

************Prop:************ Let $f$ and $g$ be arithmetic functions if $f$ and $g$ are multiplicative so is $fg$ and $f/g$

********Th:******** If $f$ is multiplicative then $f(1) =1$

********Th:******** Given that $f(1) = 1$, then

- $f$ is multiplicative iff
    
    $$ f\left(\prod_{i = 1}^r p_i^{a_i}\right) = \prod_{i = 1}^r f(p_i^{a_i}) $$
    
    for all primes $p_i$ and all integers $a_i \ge 1$
    
- If $f$ is multiplicative then $f$ is completely multiplicative iff
    
    $$ f(p^a) = f(p)^a $$
    
    for all primes $p$ and all integers $a \ge1$
    


********Lemma:******** If $\gcd(n, m )=1$, then the set of positive divisors of $mn$ consists all products $d_1d_2$, where $d_1\mid m$, $d_2 \mid n$ and $\gcd(d_1, d_2) =1$; furthermore, these products are all distinct.

******Th:****** If $f$ and $g$ are multiplicative function and $F$ is defined by

$$ F(n) = (f*g)(n) $$

then $F$ is also multiplicative, if $f$ and $g$ can be completely multiplicative but $F$ may not be completely multiplicative.

**********Cor:********** The set of multiplicative functions form a group under the Dirichlet product.

********Th:******** Let $f, g$ be multiplicative functions where $f(p^k) = g(p^k)$ for any prime $p$ and any power $k$, then $f = g$.

********Th:******** If $f, g$ are completely multiplicative then if $f(p)=g(p)$ for any prime, then $f = g$.

**********Def:********** Some important completely multiplicative functions are $\operatorname{Id}_s(n)= n^s$, for a fixed $s\in \mathbb{C}$, in the case that $s =0$, we can also write $u$ or $1$ as the function when writing convolutions