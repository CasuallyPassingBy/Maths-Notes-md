---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Expected Value, and Covariance of Random Vectors]]

We define the *correlation coefficient between two random variables* $X$ and $Y$ with finite variances and nonzero, as the number 
$$
\rho(X, Y) = \frac{\text{Cov}(X, Y)}{\sqrt{\text{Var}(X)\text{Var}(Y)}}
$$
This numbers measures the *linear dependence betweeen the variables*
Then we have that 
$$
|\rho(X, Y)|\le 1
$$
Other properties:
- $\rho(X, X) = 1$
- $\rho(X, Y) = \rho(Y, X)$
- $\rho(cX, Y)= \rho(X, cY) = \text{sgn}(c)\rho(X, Y)$, when $c\ne 0$
- $\rho(cX, cY)=\rho(X, Y)$, when $c\ne 0$
- $\rho(X+c, Y) = \rho(X, Y+c) = \rho(X, Y)$ for any $c \in\Bbb R$
- $\rho(X, aX+b) =\text{sgn}(a)$, when $a\ne 0$ and $b\in \Bbb R$
- If $|\rho(X, Y)| = 1$, iff $Y = aX + b$, with $a\ne 0$ and $b\in \Bbb R$

When $\rho(X, Y) =0$ we say that $X$ and $Y$ are not correlated. When $|\rho(X, Y)| =1$, we say that $X$ and $Y$ are perfectly correlated positively or negatively depending on the sign of $\rho(X, Y)$.

If we have that $(X, Y)$ is a random vector with a bi distributed normal such that $\rho(X, Y) =0$, then $X$ and $Y$ are independent

Let $X = (X_1, \dots, X_n)$ be a random vector, then we can define the *correlation coefficient matrix*, defined as
$$
\rho(X) = (\rho(X_i, X_j))_{i, j}
$$
