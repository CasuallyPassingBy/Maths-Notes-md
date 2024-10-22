---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]], [[Interchange of Limits]], [[Contour Integrals in C]]

Suppose $f_n : \Omega \to \Bbb C$ is a sequence of functions all defined on $\Omega$. The sequence is said to _converge pointwise_, denoted $f_n \to f$, if for each $z \in \Omega$, the sequence $f_n (z)$ converge. The limit defines a new function $f(z)$ on $\Omega$.

The sequence $f_n : \Omega\to \Bbb C$ of functions defined on a set $\Omega$ is said to ****converge uniformly**** to a function $f$ if, for each $\varepsilon >0$, there’s an $N \in \Bbb N$, that $n \ge N$ implies $|f_n(z) -f(z) | < \varepsilon$ for all $z \in \Omega$. This is written as $f_n \rightrightarrows f$ on $\Omega$. We can use the concept of supremum norm and say that for each $\varepsilon >0$, there’s an $N \in \Bbb N$, that $n \ge N$ implies $\|f_n -f \|_\infty < \varepsilon$

A series $\sum_{k \ge 1} g_k$ is said to _**************converge pointwise**************_ if the corresponding partial sums converge pointwise. A series $\sum_{k \ge 1} g_k$ is said to _******************converge uniformly******************_ iff the sequence of partial sums converges uniformly.

### Cauchy Criterion
- A sequence $f_n$ converges uniformly on $A$ iff for each $\varepsilon >0$, there is an $N \in \Bbb N$, such that $n \ge N$ implies for all $p \in \Bbb N$, $\|f_n -f_{n+p}\|_\infty < \varepsilon$
    
- A series $\sum _{k \ge 1} g_k$ converges uniformly on $A$ for each $\varepsilon >0$, there is an $N \in \Bbb N$, such that $n \ge N$ implies for all $p \in \Bbb N$, $$ \left\|\sum_{k = n+1}^{n+p} g_k\right\|_\infty < \varepsilon $$
If the sequence $f_n$ consists of continuous functions defined on $A$ and if $f_n \rightrightarrows f$, then $f$ is continuous on $A$. Similarly, if the functions $g_k$ are continuous and $g = \sum_{k \ge 1} g_k$ uniformly on $A$, then $g$ is continuous on $A$

## Weierstrass Convergence Theorem

**Th:** Let $f_n, f:\Omega \to \Bbb C$ such that for all compact $K \subseteq \Omega$, the sequence $\{f_n\}$ converges uniformly to $f$ on $K$, i.e. $f_n \rightrightarrows f$ on $K$

- If $f_n$ is continuous on $\Omega$ for each $n \in \Bbb N$, then $f$ is continuous on $\Omega$
    
- If $f_n$ is continuous on $\Omega$ for each $n\in \Bbb N$, and $\gamma\subseteq \Omega$ is a piecewise smooth curve then
    
    $$ \int_\gamma f(z) \, dz = \lim_{n \to \infty }\int_\gamma f_n(z) \, dz $$
    
- If $f_n$ is analytic on $\Omega$ for each $n\in \Bbb N$, then $f$ is analytic on $\Omega$ . Furthermore, for each $k\in \Bbb N$ the sequence $(f_n^{(k)})$ converges uniformly to $f^{(k)}$ on each $K \subseteq \Omega$ compact, in particular we have that $$ f^{(k)}(z) = \lim_{n \to \infty}f_n^{(k)}(z) $$
    
    for all $z\in \Omega$
    

**Cor:** Let $f_n, f:\Omega \to \Bbb C$ such that for all compact $K \subseteq \Omega$, the series $\sum f_n$ converges uniformly to $f$ on $K$, i.e. $\sum f_n \rightrightarrows f$ on $K$

- If $f_n$ is continuous on $\Omega$ for each $n \in \Bbb N$, then $f$ is continuous on $\Omega$
    
- If $f_n$ is continuous on $\Omega$ for each $n\in \Bbb N$, and $\gamma\subseteq \Omega$ is a piecewise smooth curve then $$ \int_\gamma f(z) \, dz = \int_\gamma \left(\sum_{n= 1}^\infty f_n(z)\right)\, dz= \sum_{n = 1}^\infty \int_\gamma f_n(z) \, dz $$
- If $f_n$ is analytic on $\Omega$ for each $n\in \Bbb N$, then $f$ is analytic on $\Omega$ . Furthermore, for each $k\in \Bbb N$ the sequence $\sum f_n^{(k)}$ converges uniformly to $f^{(k)}$ on each $K \subseteq \Omega$ compact, in particular we have that
    
    $$ f^{(k)}(z) = \sum _{n = 1}^\infty f_n^{(k)}(z) $$
    
    for all $z\in \Omega$