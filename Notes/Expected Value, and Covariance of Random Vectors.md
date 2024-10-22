---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Random Vectors]], [[Expected Value of Random Variables]], [[Variance of Random Variables]], [[Singular Value Decomposition#Positive Definite Matrix| Positive definite matrix]]

We define the expected value of a random vector $(X, Y)$ composed of two random variable with finite expected values, as the vector of the expected values as 
$$
E[(X, Y)] = (E[X], E[Y])
$$
Similarly for $n$ dimensional random vector.

We can define the covariance of two vectors, where how much the each change with respect to the other and it is defined as 
$$
\text{Cov}(X, Y) = E[(X-E[X])(Y-E[Y])]
$$
doing some algebra we can see that 
$$
\text{Cov}(X, Y) = E[XY]-E[X]E[Y]
$$

and that 
$$
\text{Cov}(X, Y) = \text{Cov}(Y, X)
$$
It has a few properties:
- Let $c\in \Bbb R$, then $\text{Cov}(X, c)= 0$
- $\text{Cov}(cX, Y) = \text{Cov}(X, cY) = c\text{Cov}(X, Y)$
- $\text{Cov}(X+ c, Y) = \text{Cov}(X, Y+c ) = \text{Cov}(X, Y)$
- $\text{Cov}(X_1 +X_2, Y) = \text{Cov}(X_1, Y)+ \text{Cov}(X_2, Y)$
This properties are actually enough to tell us that the covariance is a bilinear operator
- $\text{Var}(X+ Y) = \text{Var}(X)+ \text{Var }(Y) + 2\text{Cov}(X, Y)$
- If $X$ and $Y$ are independent, then we know that $\text{Cov}(X, Y) =0$. In general it is not true that $\text{Cov}(X, Y)=0$, then $X$ and $Y$ are independent
- $\text{Cov}(X, X) = \text{Var}(X)$
We can prove that 
$$
|\text{Cov}(X, Y)| \le \sqrt{\text{Var}(X)\text{Var}(Y)}
$$

With this we can define the variance of a random vector composed of $n$ random variables with a finite variance. It is the square matrix 
$$
\text{Var}(X_1,\dots, X_n) = (\text{Cov}(X_i, X_j))_{i, j}
$$
this matrix is symmetric. 
We can get the identity, let $X = (X_1, \dots, X_n)$:
$$
\text{Var}(X) := E[(X-E(X))(X-E(X))^\top]
$$
The matrix $\text{Var}(X)$ is symmetric and positive definite

# Expected Value of functions of a Random Vector

Let $(X, Y)$ be a random vector and $\varphi:\Bbb R^2 \to \Bbb R$ be Borel measurable function such that the random variable $\varphi(X, Y)$ has a finite expected value. Then $$E[\varphi(X, Y) ] = \int_{\Bbb R^2} \varphi(x, y) dF_{X, Y}(x, y)$$
From this we can actually get that:

Let $X$ and $Y$ have finite expected value, then $$E[X + Y] = E[X] + E[Y]$$
Let $X$ and $Y$ be independent random variables, and let $g, h$ be Borel measurable functions such that $g(X)$ and $h(Y)$ have finite expected values:
$$E[g(X) \cdot h(Y) ]  = E[g(X)] \cdot E[h(Y)]$$