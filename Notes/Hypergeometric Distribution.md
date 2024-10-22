---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]]

We use the hyper geometric distribution when we want to take out $x$ white balls while grabbing $n$ balls at at time, out of a bag with $N$ white and black balls, with $K$ white. Then we say that $X$ is a random variable with distribution being hypergeometric with parameters $N$, $K$, and $n$. We write $X \sim \operatorname{hypergeo}(N, K, n)$, with a pmf being

$$

f(x; N, K, n)= \begin{cases}\frac{\left(\begin{array}{c} K \\ x \end{array}\right)\left(\begin{array}{c} N-K \\ n-x \end{array}\right)}{\left(\begin{array}{l} N \\ n \end{array}\right)} & x\in \Bbb N \\ 0 & \text {otherwise}\end{cases} $$

We can see that

- $E[X] = n \dfrac{K}{N}$
- $\operatorname{Var}[X] = n \dfrac{K}{N}\dfrac{N-K}{N}\dfrac{N-n}{N-1}$
