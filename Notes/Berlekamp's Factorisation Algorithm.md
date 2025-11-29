---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Finite Fields]], [[Polynomial Ring of a Single Variable]]

We outline the *Berlekamp factorisation algorithm* for factoring polynomial in $\Bbb F_p[x]$. The efficiency of this algorithm is bases on the efficiency of computing greatest common divisors in $\Bbb F_p[x]$ by the Euclidean Algorithm and on the efficiency of row-reduction matrix algorithms for solving systems of linear equations.

Let $f(x) \in \Bbb F_p[x]$ be a monic polynomial of degree $n$ and let $f(x) = p_1(x) \cdots p_k(x)$ where $p_1(x), p_2(x), \dots, p_k(x)$ are powers of distinct monic polynomials in $\Bbb F_p[x]$. We know that it suffices to determine the factors $p_1(x), \dots, p_k(x)$, since the original irreducibles can be  determined from their powers using the $p$th powers and by computing greatest common divisors with derivatives. 

**Lemma:** Let $g(x)\in \Bbb F_p[x]$ be any polynomial of degree $n$. Denote $R(h(x))$ to be the remainder of $h(x)$ after division by $f(x)$. The following statements are equivalent.
- $R(g(x^p)) = g(x)$
- $f(x)$ divides $\prod\limits_{m = 0}^{p-1} (g(x)-m)$
- $p_i(x)$ divides $\prod\limits_{m = 0}^{p-1} (g(x)-m)$, for $i \in \{1,\dots, k\}$.
- For each $i\in \{1,\dots, k\}$ there is an $s_i\in\Bbb F_p$ such that $p_i(x)$ divides $g(x) - s_i$, or $g(x) \equiv s_i \pmod{p_i(x)}$. 

The proof of this actually, relies on [[Prime Ideals on Commutative Rings#^096736|primary ideals]], which i thought was neat. 

**Lemma:** The polynomials $g(x)$ of degree $<n$ satisfying the equivalent conditions of the previous lemma form a $\Bbb F_p$-vector space, call it $V$, of dimension $k$. The proof of this theorem relies on the [[Chinese Remainder Theorem for Rings]]. 

**Lemma:** Let $g(x) = b_0 + b_1x + \cdots b_{n-1}x^{n-1}\in V$. For $0 \le j < n$ let $$R(x^{pj}) = \sum_{m = 0}^{n-1}a_{m, j}x^m,$$and let $A$ be the $n \times n$ matrix $$A = \begin{pmatrix}a_{0,0} & a_{0,1} & \cdots & a_{0, n-1} \\ a_{1,0} & a_{1,1} & \cdots & a_{1, n-1} \\ \vdots & \vdots & \ddots & \vdots \\ a_{n-1, 0} & a_{n-1, 1} & \cdots & a_{n-1, n-1} \end{pmatrix}.$$$R(g(x^p)) = g(x)$ iff $(A-I)B = 0$, where $B$ is the column matrix with entries $b_0, \dotsm, b_{n-1}$. This means that the rank of the matrix $A-I$ is $n-k$, and, consequently, this already suffices to determine if $f(x)$ is irreducible, without actually determining the factors. 

**Berlekamp's Algorithm:** Let $g_1(x), \dots, g_k(x)$ be a basis of solutions for $(A-I)B = 0$, a basis for $V$, where we may take $g_1(x) = 1$. Beginning $w(x) = f(x)$, we compute the greatest common divisor $(w(x), g_i(x)-s)$ for $1 < i < k$ and $s\in \Bbb F_p$ for every factor of $f(x)$ already computed. The process terminates when $k$ relatively prime factors have been determined. 