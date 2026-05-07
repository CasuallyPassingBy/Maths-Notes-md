---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Integers modulo n]]

********Th:******** The linear congruence $ax\equiv b \pmod n$ has solution iff $d \mid b$, where $d = \gcd(a,n)$. If ${d\mid b}$, then it has $d$ mutually incongruent solutions modulo $n$.

By solving the Diophantine equation $ax+ny = b$, and the solutions will be of the form

$$ x = x_0+\frac{n}{d}t, \qquad 0 \le t < d\land t\in \Bbb Z $$

**********Cor:********** If $\gcd(a,n)$, then the linear congruence $ax\equiv b \pmod n$ has a unique solution modulo $n$.

### Chinese Remainder Theorem
Let $n_1, n_2, \dots, n_r$ be positive integers such that $\gcd(n_i, n_j) =1$ for $i \ne j$. Then the system of linear congruence
$$ \begin{align*} x \equiv a_1& \pmod {n_1} \\ x \equiv a_2& \pmod {n_2} \\ \vdots& \\ x \equiv a_r& \pmod {n_r} \\

\end{align*} $$

has a unique solution, which is unique modulo the integer $N= n_1 n_2\cdots n_r$.

The solution is obtained by
$$ N_k = \frac{N}{n_k} \quad\text{for $i \in\{1, \dots,r\}$} $$

then we know that $\gcd(N_k, n_k) =1$ then we can define
$$ x_k \equiv N_k^{-1} \pmod{n_k}\quad\text{for $i \in\{1, \dots,r\}$} $$

then the solution is of the form $$ x = \sum_{k = 1}^r a_k x_kN_k $$
then $x$ is a solution up to modulo $N$.

********Th:******** The system of linear congruences$$ ax+by \equiv r \pmod n$$$$ cx+dy \equiv s \pmod n $$
has a unique solution modulo $n$ whenever $\gcd(ad-bc, n)=1$.

where the solutions will be of the form $$ x \equiv (ad-bc)^{-1}(dr-bs) \pmod n $$$$ y \equiv (ad-bc)^{-1}(as-cr) \pmod n $$
This to me feels like solving a linear system of equations in a $\Bbb Z_n$ [[Module and Algebra|module]], and a matrix over $\Bbb Z_n$

********************Th:******************** Given a linear congruence of the form
$$ ax+by \equiv c \pmod n $$

there exists solutions if $\gcd(a,b, n )\mid c$ and there will be $n$ different solutions up to modulo $n$, which might be equivalent to looking for solutions of the Diophantine equation
$$ ax+by+nz = c $$
with $0\le x, y < n$

**Lemma:** If $d\mid m$, $d> 0$ and if $u$ is a solution of $f(x) \equiv 0\pmod m$, then $u$ is a solution of $f(x) \equiv 0 \pmod d$. 

**Th:** Let $f(x)$ be a fixed polynomial with integral coefficients, and for any positive integer $m$ let $N(m)$ denote the number of solutions of the congruence $f(x) \equiv 0\pmod m$. If $m = m_1 m_2$ where $(m_1, m_2) = 1$, then $N(m) = N(m_1) N(m_2)$. If $m = \prod_{p}p^{\mu_p}$, then $N(m) = \prod_{p}N(p^{\mu_p})$. 

# Prime 