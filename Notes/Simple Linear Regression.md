---
tags:
---
Subjects: [[Statistics]], [[Machine Learning]]
Links: [[Normal Distribution]], [[]]

Let $X_i, Y_i$ and $\varepsilon_i$ be random variables that satisfy the equation: $$Y_i = \beta_0 + \beta_1 X_i + \varepsilon_i$$We call $\varepsilon_i \sim N(0, \sigma^2)$ where $\sigma^2> 0$ is constant, and $\beta_0$ and $\beta_1$ are real constants that we want to estimate. 

# Parameter Estimation

We want to estimate the parameters $\beta_0$ and $\beta_1$ such that they minimise the distance between the errors: $$Y_i = \beta_0 + \beta_1 X_i + \varepsilon_i$$then $$\varepsilon_i = Y_i - \beta_0 - \beta_1 X_i$$We would like to minimise the value $S = \sum_{i = 1}^n |\varepsilon_i|$. To minimise this quantity, is the same as to minimise the quantity: $$S' = \sum_{i = 1}^n \varepsilon_i ^2$$
We want to calculate the derivatives: $$ \frac{\partial}{\partial \beta_0} S' = -2 \sum_{i = 1}^n Y_i + 2n \beta_0 + 2\beta_1 \sum_{i = 1}^n X_i$$
and $$\frac{\partial}{\partial \beta_1} S' = -2 \sum_{i = 1}^n Y_i X_i + 2\beta_0\sum_{i = 1}^n X_i + 2\beta_1 \sum_{i = 1}^n X_i ^2$$
We set the equations equal to $0$, and we make some algebraic manipulations and get: $$\begin{align}
n \beta_0 + \beta_1 \sum_{i = 1}^n X_i  &=  \sum_{i = 1}^n Y_i \\
\beta_0\sum_{i = 1}^n X_i + \beta_1 \sum_{i = 1}^n X_i ^2 &= \sum_{i = 1}^n Y_i X_i
\end{align}$$
These equations are called the *Normal Equations*. 

Trying to solve for $\beta_0$ from the first equation, we get that $$ \beta_0 = \frac1n \sum_{i = 1}^n Y_i + \frac1n \sum_{i = 1} X_i= \bar Y + \beta_1 \bar X$$
We multiply the first equation by $\sum_{i = 1}^n X_i$ and get $$n \beta_0\sum_{i = 1}^n X_i + \beta_1 \left(\sum_{i = 1}^n X_i\right)^2=  \sum_{i = 1}^n Y_i \sum_{i = 1}^n X_i$$
We subtract this equation with the second normal equation getting that $$\beta_1 \left[\left(\sum_{i = 1}^n X_i\right)^2 - n \sum_{i = 1}^n X_i^2\right] = \sum_{i = 1}^n Y_i \sum_{i = 1}^n X_i- n \sum_{i = 1}^n X_i Y_i$$
We get that $$\beta_1 = \dfrac{\sum_{i = 1}^n Y_i \sum_{i = 1}^n X_i- n \sum_{i = 1}^n X_i Y_i}{\left(\sum_{i = 1}^n X_i\right)^2 - n \sum_{i = 1}^n X_i^2}$$
Making some algebraic manipulations we get the value of the estimator of $\beta_1$ to be $$\hat \beta_1 = \dfrac{\sum_{i = 1}^n X_i Y_i - n \bar X \bar Y}{\sum_{i = 1}^n X_i^2 - n \bar X^2}$$