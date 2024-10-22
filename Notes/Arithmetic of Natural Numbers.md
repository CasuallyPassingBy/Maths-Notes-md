---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Natural Numbers]]
### Addition
********Th:******** There is a unique function $+: \Bbb N \times \Bbb N \to \Bbb N$ such that
- $+(m, 0) = m$ for all $m \in \Bbb N$
- $+(m,n+1) = +(m,n)+1$ for all $m,n \in \Bbb N$
This can be written in the usual way as
- $m+0 = m$ for all $m \in \Bbb N$
- $m+(n+1) = (m+n)+1$

### Multiplication
********Th:******** There is a unique function $\cdot: \Bbb N \times \Bbb N \to \Bbb N$ such that
- $\cdot(m, 0) = 0$ for all $m \in \Bbb N$
- $\cdot(m,n+1) = \cdot(m,n)+n$ for all $m,n \in \Bbb N$
This can be written in the usual way as
- $m\cdot 0 = 0$ for all $m \in \Bbb N$
- $m\cdot(n+1) = (m\cdot n)+n$

********Th:******** Addition and Multiplication are commutative, associative. Additionally, multiplication is distributive over addition.

### Exponentiation

We can uniquely define exponentiation of natural numbers as

$$ m ^0 = 1\quad \text{ for all } m\in \Bbb N $$$$ m^{n+1} = m^n \cdot m \quad \text{for all }m, n \in \Bbb N $$

### Difference or Subtraction

Let $n, m \in \Bbb N$ such that $m \le n$. The unique natural $r$ that satisfies $m +r = n$, we call it the **difference** of $n$ and $m$, denoted as $n-m$

**Prop:** Let $m, n, r, s \in \Bbb N$ such that $m \le n$ and $s \le r$. Then

- $n-n = 0$, and $n-0 = n$ for all $n \in \Bbb N$
- $(s+m)+(n-m) = s+n$
- $(n+r)-(m+s) = (n-m)+(r-s)$
- If $r \le n-m$, then $(n-m)-r = n -(m+r)$
- If $r \le m$, then $n -(m-r) = (n-m)+r$
- $n \cdot (r-s) = n\cdot r-n \cdot s$
- $(n-m)\cdot (r-s) = (n \cdot r+m\cdot s) - ( n\cdot s+ m \cdot r)$

### Peano’s Axioms for Arithmetic
1. If $S(n) = S(m)$ , then $n=m$
2. $S(n) \Bbb Ne0$
3. $n+0 = n$
4. $n + S(m) = S(n+m)$
5. $n\cdot 0 = 0$
6. $n \cdot S(m) =n\cdot m +n$
7. If $n \Bbb Ne 0$, then $n = S(k)$ for some $k$
8. The Induction Schema. Let $A$ be an arithmetic property (a property expresible in terms of $+, \cdot, S, 0$). If $0$ has the property $A$ and if $A(k)$ implies $A(S(k))$ for every $k$, then has the property $A$.

Given what we have we can check that the natural numbers constructed satisify Peano’s Axioms for arithmetic.

### $\Sigma$ and $\Pi$ notation

We can define for each finite sequence $\langle k_i \mid i \in n\rangle$ of natural numbers, define $\sum \langle k_i \mid i \in n\rangle$ so that

$$ \sum \langle \rangle =0 $$$$ \sum \langle k_0\rangle =k_0 $$$$
\sum \langle k_0, \dots, k_n\rangle = \sum \langle k_0, \dots, k_{n-1}\rangle+k_n $$

and $\prod \langle k_i \mid i \in n\rangle$ so that

$$ \prod \langle\rangle =1 $$$$ \prod \langle k_0\rangle =k_0 $$$$ \prod \langle k_0, \dots, k_n\rangle = \prod \langle k_0, \dots, k_{n-1}\rangle \cdot k_n \qquad  
$$