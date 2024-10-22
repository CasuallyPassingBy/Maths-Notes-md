---
tags:
  - RealAnalysis
  - ComplexAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Power Series in R]], [[Cesàro Convergence]], [[Series in R]], [[Cesàro Convergence]]
#### Abel's Theorem
Suppose that the power series $\sum_{n = 0}^\infty a_n x^n$ converges to $f(x)$ for $|x| <1$  and that $\sum_{n = 0}^\infty a_n$ converges to $A$. Then the power series converges uniformly on $[0, 1]$ and 
$$
\lim_{x \to 1^-}f(x) = A
$$

A series $\sum_{n= 0}^\infty a_n$ is said to be _Abel Summable to $L$_ if the power series,

$$ f(x) = \sum_{n= 0}^\infty a_nx^n $$

converges in $[0,1)$ and $L = \lim_{x\to 1^-} f(x)$. It can be expressed as ${\sum_{n = 0}^\infty a_n = L \quad(\text{Abel})}$

If $\sum_{k= 1}^\infty a_k = L$ in the usual sense then $\sum_{k = 1}^\infty a_k = L \quad (\text{Abel})$

#### Tauber's Theorem
Suppose that the power series $\sum_{n = 0}^\infty a_n x^n$ converges to $f(x)$ for $|x| <1$  and $\lim na_n =0$, or $a_n = o(1/n)$. If $\lim\limits_{x\to 1^-}f(x) = A$, then the series $\sum_{n = 0}^\infty a_n$ converges to $A$.

#### Littlewood's Tauberian Theorem
Suppose that the power series $\sum_{n = 0}^\infty a_n x^n$ converges to $f(x)$ for $|x| <1$  and $a_n =O(1/n)$. If $\lim\limits_{x\to 1^-}f(x) = A$, then the series $\sum_{n = 0}^\infty a_n$ converges to $A$.

We have that for series $$\text{summable} \implies \text{Cesàro summable} \implies \text{Abel summable}$$

