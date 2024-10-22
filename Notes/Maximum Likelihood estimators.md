---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Point Estimation]]

**Def:** Let $X_1, \dots, X_n$ be a random sample of a population with density $f(x; \theta)$. We define the *likelihood function* as the joint density function of the sample and is denoted as $L(\theta) = L(\theta \mid \underline x)$. Meaning $$L(\theta)  = f_{\underline X}(\underline x; \theta) = \prod_{i = 1}^n f_{X_i}(x_i; \theta)$$
**Def:** Let $X_1, \dots, X_n$ be a random sample of a population with density $f(x; \theta)$, and $L(\theta)$ be the corresponding likelihood function. $\hat \theta = T(\underline X)$ is called the *maximum likelihood estimator* of $\theta$, if it satisfies that for any $\theta \in \Theta$, then $L(\hat \theta) \ge L(\theta)$.

## General method

Let $f(x; \theta_1, \dots, \theta_k)$ be a pdf with $k$ parameters. If $(\hat{\theta_1}, \dots, \hat{\theta_k})$ satisfies the $$\nabla L(\hat{\theta_1}, \dots, \hat{\theta_k}) = 0$$
Then $(\hat{\theta_1}, \dots, \hat{\theta_k})$ is a critical point of $L$. A maximum likelihood estimator is critical point $L$, since every maximum is a critical point. 

We can simplify the calculation a bit. We see that $\ln$ is continuous and strictly increasing function. Then $$\nabla (\ln ( L({\theta_1}, \dots, {\theta_k})) =  \frac{1}{L(\theta_1, \dots, \theta_k)} \nabla L(\theta_1, \dots, \theta_k)$$
Thus $$\nabla (\ln ( L({\theta_1} , \dots, {\theta_k})) =  0 \iff  \nabla L(\theta_1, \dots, \theta_k) = 0$$
By the increasing quality, we have that $\ln(L)$ achieves it maximum at the same point as $L$. 

We define the the *log-likelihood function* of $f(x; \theta_1, \dots, \theta_k)$ as $$l(\theta_1, \dots, \theta_k) = \ln(L(\theta_1, \dots, \theta_k))$$We usually look for the maximum of $l(\theta)$ instead of $L(\theta)$. 

If we already found a critical point in the (log-)likelihood function, then we check that is indeed a maximum of the function. 

## Invariance property

Sometimes it is not the objective to estimate $\theta$, but a function of $\theta$, $\tau(\theta)$. We would like to have an estimator of the function $\tau(\theta)$, meaning $\widehat{\tau(\theta)}$.

A really important property of the maximum likelihood estimators is the *invariance property*. This means that if we want the maximum likelihood estimator of a function $\tau(\theta)$, denoted as $\widehat{\tau(\theta)}$, then $$\widehat{\tau(\theta)} = \tau(\hat\theta)$$
**Def:** The likelihood function induced by $\tau(\theta)$ is denoted as $L^*$, is given by $$L^*(\eta) = \sup_{\{\theta \mid \tau(\theta) = \eta\}} = L(\theta)$$
In this case, we say that the value $\hat \eta$ that maximises the function $L^*(\eta)$ is a maximum likelihood estimator of $\eta = \tau(\theta)$. 

We see that $$\sup_\eta L^* (\eta) = \sup_\eta \sup_{\{\theta \mid \tau(\theta)= \eta\}} L(\theta) = \sup_\theta L(\theta) $$
Thus the maximum coincides of each function

**Th:** If $\hat \theta$ is the maximum likelihood estimator of $\theta$, then for any function $\tau(\theta)$, the maximum likelihood estimator of $\tau(\theta)$ is $\tau(\hat \theta)$. 

In some cases, the system of equations to solve to find the maximum likelihood estimator can be too difficult, and we can use numerical methods to solve it. 

# Examples
