---
tags:
  - Statistics
---
Links: [[Point Estimation]], [[Evaluation of Point Estimators]], [[Complete Statistics]], [[Sufficient Statistics#The exponential family|The exponential family]]

We are gonna restrict ourselves to unbiased estimators, meaning estimators that belong to the class $$\mathcal C_{\tau(\theta)} = \{ T(\underline X) \mid E[T(\underline X) = \tau(\theta)\}$$
**Def:** Let $T^*(\underline X)$ be *Uniformly Minimum Variance Unbiased Estimator (UMVUE)* for $\tau(\theta)$ if it satisfies:
- $T^*(\underline X) \in \mathcal C_{\tau(\theta)}$
- For all $\theta \in \Theta$, $\text{Var}(T^*(\underline X)) \le \text{Var}(T(\underline X))$, for any $T(\underline X) \in \mathcal C_{\tau(\theta)}$

The UMVUE is then referred as the best unbiased estimator for $\tau(\theta)$ in the sense that is the one with the least mean squared error for all $\theta\in \Theta$. 

**Def:** Let $X_1, \dots, X_n$ be a random sample of $f(x; \theta)$ and $T(\underline X)$ is an unbiased estimator of $\tau(\theta)$. The following are considered the *regularity conditions*:
- The support of $f(x;\theta)$ is defined as $sup(f) = \{x \mid f(x) > 0\}$ and this is the same for all $\theta$
- For all $x\in sup(f)$, $\dfrac{\partial}{\partial \theta}\ln f(x;\theta)$ exists and is finite
- $$\frac{\partial}{\partial \theta} \int T(\underline x) f(\underline x;\theta)\, d\underline x =  \int \frac{\partial}{\partial \theta}T(\underline x) f(\underline x;\theta)\, d\underline x $$
- $$\frac{\partial}{\partial \theta} \int f(\underline x;\theta)\, d\underline x =  \int \frac{\partial}{\partial \theta}f(\underline x;\theta)\, d\underline x $$
- $$0 < E\left[\left(\frac{\partial }{\partial \theta} \ln f(x;\theta)\right)^2\right]<\infty$$
looking around i found that the only two important are:
- $$\frac{\partial}{\partial \theta} \int T(\underline x) f(\underline x;\theta)\, d\underline x =  \int \frac{\partial}{\partial \theta}T(\underline x) f(\underline x;\theta)\, d\underline x $$
- For all $x\in sup(f)$, $\dfrac{\partial}{\partial \theta}\ln f(x;\theta)$ exists and is finite

We need bit of auxiliary functions

**Def:** The *Score function*is is defined as $$Sc(\underline x; \theta) = \frac{\partial}{\partial \theta} \ln f(\underline x; \theta)$$
**Def**: The *Fischer Information* is defined as $$I_{\underline X} (\theta) = E\left[\left(\frac{\partial}{\partial \theta} \ln f(\underline X; \theta)\right)^2\right] = E[(Sc)^2]$$
**Lemma:** If the regularity conditions are satisfied then:
- $E[Sc] = 0$
- $\text{Var}(Sc) = I_{\underline X}(\theta)$

**Def:** If $X$ is a random variable, then to $$I_{ X} (\theta) = E\left[\left(\frac{\partial}{\partial \theta} \ln f( X; \theta)\right)^2\right] $$is know as the *sample's unit Fischer Information*

**Lemma:** If the regularity conditions are met, then 
- $I_{\underline X}(\theta) = n I_X(\theta)$
- $I_{\underline X}(\theta) = - E\left[\dfrac{\partial^2}{\partial \theta^2} \ln f(\underline X; \theta)\right]$ 
- $I_{\underline X}(\theta) = -n E\left[\dfrac{\partial^2}{\partial \theta^2} \ln f(X; \theta)\right]$ 
### Cramér-Rao Lower Bound
Let $X_1, \dots, X_n$ be a random sample of $f(x; \theta)$ and $T(\underline X)$ be an unbiased estimator of $\tau(\theta)$. If the regularity conditions are met, then $$\text{Var}(T) \ge \frac{(\tau'(\theta))^2}{I_{\underline X}(\theta)}$$This inequality is known as the *Cramér-Rao inequality* or the information inequality, and the quantity $$\text{CRLB}(\tau(\theta))=\frac{(\tau'(\theta))^2}{I_{\underline X}(\theta)}$$is known as the Cramér-Rao Lower Bound (CRLB). The equality holds iff $$\sum_{i = 1}^n \frac{\partial }{\partial \theta} \ln f(x_i;\theta) = k(\theta; n) [T(\underline x) - \tau(\theta)] $$where $k$ can depend on $\theta$ and on $n$.

We have that if an unbiased estimator that coincides with the CRLB, then that estimaor is an UMVUE, but there can be an UMVUE that doesn't coincide with the CRLB

If the random sample is of some member of the exponential family, then there always exists of $\theta$ for which there's a unbiased estimator which variance coincides with the CRLB

**Def:** Let $T(\underline X)$ be an unbiased estimator of $\tau(\theta)$, then the *efficiency of of the estimator*, is defined as $$\text{Eff}(T) = \frac{\text{CRLB}(\tau(\theta))}{\text{Var}(T)}$$We see that $0 \le \text{Eff}(T)\le 1$. We say that an estimator is *efficient* if its efficiency is $1$. Meaning that it matches with CRLB

#### Multivariate case

A generalisation of the theory made by Cramér and Rao is when distributions have two or more parameters. In this case, the Fishcer information, is actually the *Fischer Information matrix* for a distribution with $N$ parameters defined as $$[I_{\underline X}(\theta)]_{i, j} = E\left[\left(\frac{\partial}{\partial \theta_i} \ln  f(\underline X; \underline \theta)\right)\left(\frac{\partial}{\partial \theta_j} \ln  f(\underline X; \underline \theta)\right)\right]$$
Which makes it symmetric. 

### Rao-Blackwell Theorem
Let $T(\underline X)$ be an unbiased estimator for $\tau(\theta)$ and $S$ be a sufficient statistic. Let $T^*(\underline X) = E(T\mid S)$. Then 
- $T^*$ is a function of $S$
- $T^*$ be an unbiased for $\tau(\theta)$, meaning $E(T^*) = \tau(\theta)$
- $\text{Var}(T^*) \le \text{Var}(T)$ for all $\theta \in \Theta$

#### Lehmann-Scheffé Theorem
 Let $X_1, \dots, X_n$ be a random sample of $f(x;\theta)$ and let $S$ be a complete and sufficient statistic. Let $T^*(\underline X)$ be a function of $S$, such that $E[T^*] = \tau(\theta)$, $T^*$ is unbiased for $\tau(\theta)$, then $T^*$ is the UMVUE for $\tau(\theta)$. 