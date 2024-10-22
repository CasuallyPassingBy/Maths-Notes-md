---
tags:
  - AlgorithmsAndDataStructures
---
Subjects: [[Algorithms and Data Structures]]
Links: [[Asymptotic notation]], [[Divide and Conquer]]

## Substitution method for solving recurrence

The *substitution method* for solving recurrence compromises two steps:
- Guess the form of the solution
- Use mathematical induction to find the constants and who that the solution works

# Master Theorem

**Lemma:** Let $a\ge 1$ and $b>1$ be constants, and let $f(n)$ be a nonnegative function defined on exact powers of $b$. Define $T(n)$ on exact powers of $b$ by the recurrence $$T(n) = \begin{cases} \Theta(1) & n = 1 \\ aT(n/b) + f(n) & n = b^k\end{cases}$$
where $i$ is a positive integer. Then $$T(n) = \Theta(n^{\log_b a})+\sum_{k = 0}^{\log_b n-1} a^k f(n/b^k)$$**Lemma:** Let $a\ge 1$ and $b>1$ be constants, and let $f(n)$ be a nonnegative function defined on exact powers of $b$. A function $g(n)$ defined over exact powers of $b$ by $$g(n)=\sum_{k = 0}^{\log_b n-1} a^k f(n/b^k) $$has the following asymptotic bounds for exact powers of $b$:
- If $f(n) = O(n^{\log_b a-\varepsilon})$ for some constant $\varepsilon>0$, then $g(n) =O (n^{\log_b a})$ 
- If $f(n) = \Theta(n^{\log_b a})$, then $g(n) = \Theta( n^{\log_b a}\log n)$ 
- If $f(n) = \Omega(n^{\log_b a + \varepsilon})$ for some constant $\varepsilon>0$, and if $af(n/b) \le cf(n)$ for some constant $c<1$ and all sufficiently large $n$, then $g(n) = \Theta(f(n))$

**Lemma:** Let $a\ge 1$ and $b>1$ be constants, and let $f(n)$ be a nonnegative function defined on exact powers of $b$. Define $T(n)$ on exact powers of $b$ by the recurrence $$T(n) = \begin{cases} \Theta(1) & n = 1 \\ aT(n/b) + f(n) & n = b^k\end{cases}$$
where $i$ is a positive integer. Then  $T$ has the following asymptotic bounds: 
- If $f(n) = O(n^{\log_b a-\varepsilon})$ for some constant $\varepsilon>0$, then $T(n) = \Theta(n^{\log_b a})$ 
- If $f(n) = \Theta(n^{\log_b a})$, then $T(n) = \Theta( n^{\log_b a}\log n)$ 
- If $f(n) = \Omega(n^{\log_b a + \varepsilon})$ for some constant $\varepsilon>0$, and if $af(n/b) \le cf(n)$ for some constant $c<1$ and all sufficiently large $n$, then $T(n) = \Theta(f(n))$

**Th**: Let $a\ge 1$ and $b>1$ be constants, let $f(n)$ be a function, and let $T(n)$ be defined on nonnegative integers by the recurrence 
$$ T(n) = aT(n/b) + f(n)$$where we interpret $n/b$ to mean either $\lfloor n/b\rfloor$ or $\lceil n/b \rceil$. Then $T$ has the following asymptotic bounds: 
- If $f(n) = O(n^{\log_b a-\varepsilon})$ for some constant $\varepsilon>0$, then $T(n) = \Theta(n^{\log_b a})$ 
- If $f(n) = \Theta(n^{\log_b a})$, then $T(n) = \Theta( n^{\log_b a}\log n)$ 
- If $f(n) = \Omega(n^{\log_b a + \varepsilon})$ for some constant $\varepsilon>0$, and if $af(n/b) \le cf(n)$ for some constant $c<1$ and all sufficiently large $n$, then $T(n) = \Theta(f(n))$

