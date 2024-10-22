---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Statistical Hypothesis Test]]

Suppose that we have a random sample of $f(x; \theta)$ and $\theta \in \Theta$ we would like to test $$H_0:\theta \in \Theta_0 \qquad H_1:\theta \in \Theta_1$$where $\Theta_0, \Theta_1 \subseteq \Theta$ and where $\Theta_0$ and $\Theta_1$ are disjoint. Usually as $\Theta_1 = \Theta\setminus \Theta_0$. 

We like to generalise the ideas of the [[Statistical Test for Simple Hypotheses#Neymann-Pearson Lemma|Neymann-Pearson Lemma]], and get a similar sense of a ratio of likelihoods, we would like to have a quantity that becomes small when $H_0$ is false. 

# Test of Generalised Likelihood Ration

**Def:** Let $X_1, \dots, X_n$ be a random sample of $f(x;\theta)$ and $L(\theta \mid \underline x)$ be the likelihood function, where $\theta \in \Theta$. The *generalised likelihood ratio* is defined as $$\lambda = \dfrac{\max\limits_{\theta \in \Theta_0} L(\theta \mid \underline x)}{\max\limits_{\theta \in \Theta}L(\theta \mid \underline x)}$$
We see that the denominator of the generalised likelihood ratio, is actually just the likelihood function evaluated on the [[Maximum Likelihood estimators|maximum likelihood estimator]]. Meaning that $\max\limits_{\theta \in \Theta} L(\theta\mid \underline x) = L(\hat \theta)$, with $\hat \theta$ is the maximum likelihood estimator.

We see that since they are nonnegative quantities, we see that $0\le \lambda \le 1$. 

We see $\lambda$ is a function of $\underline x$, if we substitute the observation with the random sample $\underline X$ is a statistic and is denoted $\Lambda$.
#### Test of the generalised likelihood ratio or the Principle of the generalised likelihood ratio

This test establishes the following decision rule:
$$\text{Reject } H_0:\theta \in \Theta_0 \iff \lambda \le  \text{for some constant } k\in [0,1] $$
The constant $k$ is specified by the size of the test and test statistic $\Lambda$.

In general, we will have good tests with this method. The problem with this method is to calculate $\max L(\theta)$ or the distribution of $\Lambda$, which is necessary of the evaluation of the power of the test.

### The asymptotic distribution of the likelihood quotient
[[Unbiased Point Estimation]]
[[Convergence of Random Variables#Convergence in distribution|Convergence in distribution]]

**Prop:** Let $X_1, \dots, X_n$ be a random sample of $f(x;\underline \theta)$ where $\underline \theta = (\theta_1, \dots, \theta_k)$. For the hypothesis: $$H_0: \theta_1 =\theta_1', \dots, \theta_r= \theta_r', \theta_{r+1}, \dots, \theta_k$$where $\theta_1', \theta_2', \dots, \theta_r'$ be fixed values and $\theta_{r+1}, \dots, \theta_k$ are not specified, it satisfies $-2 \ln \lambda \stackrel{d}{\longrightarrow} \chi^2(r)$ (converges in distribution) when $H_0$ is true

**Th:** For testing the hypotheses $H_0: \theta = \theta_0$ against $H_1:\theta \ne \theta_0$, where $\theta$ is a parameter, suppose that $X_1, \dots, X_n$ is a random sample of a population of with density function $f(x;\theta)$, which satisfies the regularity conditions, and let $\hat \theta$ be the maximum likelihood estimator of $\theta$. Then under $H_0$, when $n\to\infty$, it satisfies that $-2 \ln \lambda \stackrel{d}{\longrightarrow} \chi^2(1)$ (converges in distribution)