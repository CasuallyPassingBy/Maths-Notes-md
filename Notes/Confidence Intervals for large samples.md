---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Interval estimation]], [[Asymptotic Properties of Estimators]], [[Unbiased Point Estimation]], [[Maximum Likelihood estimators]]

We have that if $f(x; \theta)$ satisfies the regularity conditions, and $\hat \theta$ be the maximum likelihood estimator, then when $n \to \infty$, $$\hat \theta \sim N\left(\theta, \frac{1}{I_{\underline X}(\theta)}\right)$$
in a more general aspect we have that $$\widehat{\tau(\theta)} = \tau(\hat \theta) \sim N(\tau(\theta), \text{CRLB}(\tau(\theta))$$
Meaning that $$\frac{\tau(\hat \theta) -\tau(\theta)}{\text{CRLB}(\tau(\theta))} \sim N(0,1)$$
The main problem we usually have is that $\text{CRLB}(\tau(\theta))$ is dependent on the parameter $\theta$. What we can do is consider that, if we substitute $\hat \theta$ on with $\theta$ on the expression of lower bound, and with the notation $\widehat{\text{CRLB}(\tau(\theta))}$, then we get that $$Q= \frac{\tau(\hat \theta)-\tau(\theta)}{\widehat{\text{CRLB}(\tau(\theta))}} \sim N(0,1)$$
Then we can do similar things as [[Confidence Intervals for normal samples]], and get that the interval of $(1-\alpha)$ confidence is $$\left(\tau(\hat\theta)- z_{1-\alpha/2} \frac{\widehat{\text{CRLB}(\tau(\theta))}}{n}, (\tau(\hat\theta)+ z_{1-\alpha/2} \frac{\widehat{\text{CRLB}(\tau(\theta))}}{n} \right)$$where $z_{1-\alpha/2}$ the the $1-\alpha/2$ quantile of the normal $N(0,1)$. 