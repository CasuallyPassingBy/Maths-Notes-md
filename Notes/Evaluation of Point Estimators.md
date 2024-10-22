---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Point Estimation]]

## Mean Squared Error

**Def:** Let $T(X_1, \dots, X_n)$ be an estimator of $\tau(\theta)$. We define the mean squared error $(MSE)$, of $T$  is defined as $$MSE_T(\tau(\theta)) = E[T(\underline X)- \tau(\theta))^2] $$
With this definition we can get a relationship with the variance, getting that $$MSE_T(\tau(\theta)) = \text{Var}(T)+ [E[T] - \tau(\theta)]^2$$
The term $E[T]- \tau(\theta)$ is called the *bias* of $T$. If we know that the bias is zero, then $MSE_T(\tau(\theta)) = \text{Var}(T)$ 

**Def:** An estimator of $T(\underline X)$ of $\tau(\theta)$ is *unbiased* if has bias of zero, meaning $E[T(\underline X)] = \tau(\theta)$ 

## Consistency

This is related to the [[Convergence of Random Variables]]

**Def:** Let $T_1, \dots, T_n$ be a sequence of estimators of $\tau(\theta)$, where $T_n$ is bases on the sample size $n$. This sequence of estimators of $\tau(\theta)$ is *consistent in mean squared error* if $$\lim_{n \to \infty} E[(T_n(\underline X) - \tau(\theta))^2]  = 0$$
This is analogous to the $L^2$ convergence of random variables


**Def:** We say that the sequence of estimators $\{ T_n\}_{n \in \Bbb N}$ is *simply consisten* iff, for every $\varepsilon >0$, then $$\lim_{n \to \infty} P(|T_n - \tau(\theta)| > \varepsilon ) = 0 $$ This is the convergence in probability

## Loss Functions and Estimation
This is related to [[Bayesian Approach to Point Estimators]]

In the Bayesian approach the problem of estimation of parameters is through a loss function $L(\theta, a)$, that measures the loss when the value of the parameter through $a$, being the true value being $\theta$. Then $\hat \theta$ is selected in a way that minimises $E[L(\theta, \hat \theta)]$ where the expected value is considered with respect to $\theta$, using the posteriori distribution $\pi(\theta \mid \underline x)$. 

**Def:** To $L(\theta, a)= (a-\theta)^2$ us called the *squared error loss function*. 

We see that $$E[L(\theta, a) ] = \int (a-\theta)^2 \pi(\theta\mid \underline x)\, d\theta$$
If we differentiate we get that $$2\int(a-\theta) \pi(\theta\mid \underline x)\, d\theta  = 0 \implies a = \int\theta\pi(\theta\mid \underline x)\, d\theta$$Which is the *a posteriori expected value* of $\theta$. 

**Def:** To $L(\theta, a)= |a-\theta|$ us called the *absolute error loss function*. In this case
$$E[L(\theta, a) ] = \int |\theta-a| \pi(\theta \mid \underline x)\, d\theta$$
If we differentiate and do the corresponding algebra it gets to $$\int_{-\infty}^a \pi(\theta \mid \underline x)\, d\theta - \int_a^\infty \pi(\theta \mid \underline x)\, d\theta  =0$$This happens when both integrals are $1/2$, and $\hat \theta$ is the *a posteriori median* of $\theta$. 