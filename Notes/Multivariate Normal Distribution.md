---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Normal Distribution]]

We say that the random vector $X=(X_1, \dots, X_k)$ have a multivariate normal, denoted as $X\sim N(\mu, \Sigma)$distribution if the density function is

$$
f(x) = \frac{1}{(2\pi)^{n/2}\sqrt{\det \Sigma}}\exp\left(-\frac{1}{2}(x-\mu)^\top\Sigma^{-1}(x-\mu )\right)
$$
where $x$ and $\mu$ are $n$ dimensional vectors, and $\Sigma$ is a positive definitee matrix. We have a lot of important properties
- $E[X] = \mu$
- $\text{Var}(X) = \Sigma$
This means that the covariance matrix is inputted, and if the covariance matrix is diagonal it means that each $X_i$ is independent of each other. 