---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Statistical Hypothesis Test]], [[Statistical Test for Simple Hypotheses]], [[Sufficient Statistics]]

**Def:** A test $\gamma^*$ is a *uniformly most powerful test* to prove that $$H_0 : \theta \in \Theta_0 \qquad H_1:\theta\in \Theta_1$$if: 
- $\max\limits_{\theta\in \Theta_0} \pi_{\gamma^*}(\theta) = \alpha$
- $\pi_{\gamma^*}(\theta) \ge \pi_\gamma(\theta)$, for all $\theta\in \Theta_1$ and any other test $\gamma$ such that $\max\limits_{\theta\in \Theta_0} \pi_{\gamma}(\theta) = \alpha$

Meaning that among all test of size $\alpha$, the uniformly most powerful test is the one that maximises the power *for all* $\theta\in\Theta_1$. 

# A Simple Hypothesis against a Compound one
For unilateral hypothesis, meaning $$\begin{align*}
H_1: \theta > \theta_0 \\
H_1: \theta \ge \theta_0 \\
H_1: \theta < \theta_0 \\
H_1: \theta \le \theta_0 \\
\end{align*}
$$where $H_0: \theta = \theta_0$, this can be done using the [[Statistical Test for Simple Hypotheses#Neymann-Pearson Lemma|Neymann-Pearson Lemma]] to get a uniformly most powerful test taking a representative value of the alternative hypothesis, and testing two simple hypothesis. 

We have a problem if we try Neymann-Pearson Lemma and the critical region is not determined uniquely, this a case where we can't use it.

# Monotonous Likelihood Ratios

**Def:** A family of densities $\{f(x;\theta) \mid \theta\in \Theta\}$, where $X$ is univariate random variable, has a *monotonous likelihood ratio* is a statistic $T(\underline X)$, if for all $\{\theta^*, \theta\} \subseteq \Theta$ and $\underline x\in \frak X$, we have that $$\frac{L(\theta^*\mid \underline x)}{L(\theta \mid \underline x)} = \frac{L(\theta^*)}{L(\theta )}$$is a monotonous function of $t(\underline x)$, when $\theta^* > \theta$ with $f(x; \theta^*)$ and $f(x;\theta)>0$

The members of the exponential family $$f(x; \theta) = a(\theta) b(x) e^{c(\theta)d(x)}$$has a *monotonous likelihoods ratio*. If $c(\theta)$ is a strictly monotonous function of $\theta$, then $\{f(x;\theta) \mid \theta \in \Theta \subseteq \Bbb R\}$ has a non increasing likelihood quotient on $T(\underline X) = \sum_{i = 1}^n d(X_i)$

**Lemma:** If the family of densities $\{f(x; \theta) \mid \theta \in \Theta\}$ has a monotone likelihood ratio on $S(\underline X)$, where $S(\underline X)$ is a sufficient statistics, then the function $$V(s, \theta^*, \theta) = \frac{f_S(s; \theta^*)}{f(s;\theta)}$$is monotone on $s$, where $f_S(s; \theta)$ is the density function of the statistic $S$. 

### Karlin-Rubin theorem
Let $X_1, \dots, X_n$ be a random sample from a population with density $f(x; \theta)$ and we would like to test the hypotheses $$H_0 : \theta \le \theta_0 \qquad H_1:\theta > \theta_0$$if the family of densities $\{f(x;\theta)\}_{\theta \in \Theta}$ has the property of non-decreasing likelihood ratio on $S = S(\underline X)$, which is a sufficient statistic for $\theta \in \Theta$, then the test: $$\gamma: \text{Reject }H_0 \text{ if } S > k$$defined by the function $$\Psi(\underline X) = \begin{cases} 1 & S(\underline X) > k \\ 0 & S(\underline X) \le k \end{cases}$$where $k$ is such that $$E[\Psi(\underline X)] = P(S(\underline X)>k) = \alpha$$is a uniformly most powerful test of size $\alpha$ for the hypotheses proposed. 

We have several variations for this theorem, mainly if the the hypothesis we want to test are: $$H_0 : \theta \ge \theta_0 \qquad H_1:\theta < \theta_0$$
and the the family of densities $\{f(x;\theta)\}_{\theta \in \Theta}$ has the property of non-decreasing likelihood ratio on $S = S(\underline X)$, which is a sufficient statistic for $\theta \in \Theta$, then the test: $$\gamma: \text{Reject }H_0 \text{ if } S < k$$
Lastly, there are other two variations are when the family of densities $\{f(x;\theta)\}_{\theta \in \Theta}$ has the property of non-increasing likelihood ratio on $S = S(\underline X)$. Then if we have the hypotheses $$H_0 : \theta \le \theta_0 \qquad H_1:\theta > \theta_0$$the uniformly most powerful test is $$\gamma: \text{Reject }H_0 \text{ if } S < k$$
if the hypotheses we are comparing are $$H_0 : \theta \ge \theta_0 \qquad H_1:\theta < \theta_0$$and the uniformly most powerful test is $$\gamma: \text{Reject }H_0 \text{ if } S > k$$

By the observation that the exponential family members, we only need to check if $c(\theta)$ is a increasing or decreasing function of $\theta$,