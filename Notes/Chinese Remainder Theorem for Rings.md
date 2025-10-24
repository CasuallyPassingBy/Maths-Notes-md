---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Linear Congruences#Chinese Remainder Theorem|Chinese Remainder Theorem]], [[Ring Ideals and Quotient Rings]], [[Ring Homomorphisms]],  [[Product and Coproduct of Rings]]

In this note $R$ is a unital commutative ring. 

**Def:** The ideals $A$ and $B$ of the ring $R$ are said to be *comaximal* if $A+ B =R$.

This notion generalises the idea of coprime integers. Since by Bézout's identity it is true that $n\Bbb Z + m \Bbb Z = (n, m) = \Bbb Z$, in particular, $n \Bbb Z + m \Bbb Z = \Bbb Z$ when $n$ and $m$ are coprime. 

**The Chinese Remainder Theorem:** Let $A_1, A_2, \dots, A_n$ be ideals in $R$. The map $\varphi: R \to \prod_{k = 1}^n R/A_k$ defined by $$\varphi(r) = (r+A_1, r+A_2,\dots, r+ A_n)$$is a ring homomorphism with kernel $\bigcap_{k = 1}^n A_n$. If for each $i, j \in \{1,\dots, n\}$ with $i \ne j$ the ideals $A_i$ and $A_j$ are comaximal, then this map is surjective and $$\bigcap_{k = 1}^n A_k = A_1A_2\cdots A_k,$$so $$R/(A_1A_2\cdots A_n) = R\left/\bigcap_{k = 1}^n A_k\right. \cong \prod_{k = 1}^n R/A_k.$$

**Cor:** Let $n_1, n_2, \dots, n_r$ be positive integers such that $\gcd(n_i, n_j) =1$ for $i \ne j$. If $N = n_1n_2\cdots n_r$, then $$\Bbb Z/N\Bbb Z \cong \prod_{k = 1}^r \Bbb Z/n_k \Bbb Z.$$
**Cor (Chinese Remainder Theorem):** Let $n_1, n_2, \dots, n_r$ be positive integers such that $\gcd(n_i, n_j) =1$ for $i \ne j$. For any $a_1, \dots, a_r\in \Bbb Z$ there is a solution $x\in \Bbb Z$ to the simultaneous congruences $$x \equiv a_1 \pmod {n_1},\quad x\equiv a_2\pmod{n_2}, \quad \dots \quad x\equiv a_r\pmod{n_r}$$and that the solution $x$ is unique mod $N = n_1n_2\cdots n_r$. 

**Cor:** Let $f_1(x), f_2(x), \dots, f_k(x)$ be polynomials with integer coefficients of the same degree $d$. Let $n_1, n_2, \dots, n_k$ be positive integers such that $\gcd(n_i, n_j) =1$ for $i \ne j$. Then there exists a polynomial with integer coefficients and of degree $d$ with $$f(x) \equiv f_1(x) \pmod {n_1},\quad f(x)\equiv f_2(x)\pmod{n_2}, \quad \dots \quad f(x)\equiv f_k(x)\pmod{n_k}.$$Additionally it all $f_i(x)$ are monic, then $f(x)$ may also be chosen monic. 

**Cor:** Let $n$ be a positive integer and let $n = \prod_{k = 0}^\infty p_k^{\alpha}$ be its factorisation into powers of distinct primes. Then $$\Bbb Z/n \Bbb Z \cong \prod_{k = 0}^\infty \Bbb Z/p_k^{\alpha_k}\Bbb Z $$as rings, so in particular, we have the following isomorphism of multiplicative groups $$(\Bbb Z/n \Bbb Z)^\times \cong \prod_{k = 0}^\infty (\Bbb Z/p_k^{\alpha_k}\Bbb Z)^\times  $$
**Cor:** Let $e$ be an idempotent in $R$ and $e\in Z(R)$. Then $Re$ and $R(1-e)$ are two sided ideals of $R \cong Re \times R(1-e)$, and $e$ and $(1-e)$ are identities for the subrings $Re$ and $R(1-e)$, respectively. 