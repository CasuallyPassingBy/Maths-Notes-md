---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Bayesian Approach to Point Estimators]]

In the Bayesian approach to interval approximation for the unknown parameter(s), $\theta$, of a model is based on the posterior distribution $\pi(\theta \mid \underline x)$. 

The interval of $(1-\alpha)$ of credibility is any interval $(L, U)$ that satisfies $$\int_L^U \pi(\theta\mid \underline x) \, d\theta = 1-\alpha$$
the intervals of probability are not unique. We can choose, for example, an interval where the tails do this $$\int_{-\infty}^L \pi(\theta\mid \underline x)\, d\theta =\int_U^\infty \pi(\theta\mid \underline x)\, d\theta = \alpha/2 $$
or a unilateral where $L = -\infty$ or $U = \infty$. in the cases where the posterior distribution is unimodal, it is possible to adopt a *high posterior density* (HPD), where $\pi(L\mid \underline x) = \pi (U\mid \underline x)$. In this case this the minimum length interval. 