---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Point Estimation]]

Probably the simplest method do is this:

Let $X_1, \dots, X_n$ be a random sample with a distribution function of density $f(x; \theta)$. To $E[X_i^r]$ is called the *$r$th moment of the distribution/population*, and is denoted as $\mu_r$, while $\frac{1}{n}\sum\limits_{i = 1}^n X_i ^r$  is the *$r$th sample moment*, and is denoted as $M_r$. 

The method of estimation of moments consists of making sure the sample and population moments are equal, and solve for $\theta$, or $\theta_1, \dots, \theta_k$. This is $\mu_r = M_r$, where $r = 1, \dots, k$ and $k$ is the number of parameters we would like to estimate

Similarly, the $X_1, \dots, X_n$ be a random sample from a population with density $f(x; \theta_1, \dots, \theta_k)$, in the method of moments, we need to solve the following system of equations
$$\mu_1= M_1, \;\;\;\mu_2 = M_2, \dots, \mu_k = M_k$$
the solution of the system o $\underline{\hat \theta} = (\hat{\theta_1}, \dots, \hat{\theta_k})$ 