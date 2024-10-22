---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Statistical Hypothesis Test]], [[Maximum Likelihood estimators]]

We have that two distributions completely specified which will be denoted as $f_0 =f(x; \theta_0)$ and $f_1 = f(x; \theta_1)$, corresponding to the null and alternative hypothesis respectively.

So we would like to test $$H_0 : X_i \sim f_0 \quad \text{and} \quad  H_1: X_i \sim f_1$$
If we only have a single observation $x_1$ and the functions $f_0(x_1) > f_1(x_1)$, then we can decide that observation comes from $f_0$. From this, if we have that the observation comes from $f_1$ if $f_0(x_1) \le f_1(x_1)$ (it is more probable that it comes from $f_1$ than $f_0$, so we reject $H_0$). If we generalise that: reject $H_0$ if  $$P(\underline X \in \underline C\mid H_0) \le P(\underline X \in \mathcal C \mid H_1)$$equivalently, we reject $H_0$ if $$\frac{P(X \in \underline C \mid H_0)}{P(\underline X \in \mathcal C \mid H_1)} \le 1$$
## Most Powerful Tests

We would like to fix the Error type $\text{I}$ , and then we would like to have a test that has minimum Error type $\text{II}$. 

In this case of simple against simple hypothesis, $\Theta = \{\theta_0, \theta_1\}$. We would like to test $$H_0 : \theta = \theta_0 \quad \text{and} \quad  H_1: \theta = \theta_1$$
Since we are doing simple against simple that $$\pi_\gamma(\theta_0) = \text{Size error type I} = \text{Size of th test}$$and we also note that $$ 1- \pi_\gamma(\theta_1) = P(\text{Not reject } H_0 \mid H_1) = \text{Size of error type II}$$
Minimising the size of error type $\text{II}$ is equivalent of maximising the power of the test evaluated on the alternative hypothesis. 

**Def:** The test $\gamma^*$ of $H_0: \theta = \theta_0$ and $H_1 : \theta=\theta_1$ we define *the most powerful test* of size $\alpha$ ($0<\alpha<1$) iff
- $\pi_{\gamma^*}(\theta_0) =\alpha$
- $\pi_{\gamma^*}(\theta_1) \le \pi_\gamma(\theta_1)$, for any test $\gamma$ such that $\pi_\gamma(\theta_0) = \alpha$

We can translate this into critical region having:
A *best critical region* $\mathcal C^*$ of size $\alpha$  to test $H_0: \theta = \theta_0$ against $H_1: \theta = \theta_1$, satisfy that:
- $P(\underline X \in \mathcal C^* \mid H_0) = \alpha$
- $P(\underline X \in \mathcal C^* \mid H_1) \ge P(\underline X \in \mathcal C \mid H_1)$ for any $\mathcal C$ such that $P(\underline X \in \mathcal C \mid H_0) = \alpha$ 

### Neymann-Pearson Lemma
Let $X_1, \dots, X_n$ be a random sample of a population with density function $f(x; \theta)$, where $\theta \in \Theta = \{\theta_0, \theta_1\}$ and let $0 < \alpha< 1$, $k$ be a positive real number and $\mathcal C^*$ such that
- $P(\underline X \in \mathcal C^* \mid H_0) = \alpha$
- $\lambda = \dfrac{L(\theta_0 \mid \underline x)}{L(\theta_1 \mid \underline x)} \le k$ iff $\underline x \in \mathcal C^*$

Then the test $\gamma^*$ associated with $\mathcal C^*$, is a most powerful test for $H_0 : \theta = \theta_0$ against $H_1 : \theta = \theta_1$ (meaning, $\mathcal C^*$ us a best critical region)

The way this is used is that we compute $$\dfrac{L(\theta_0 \mid \underline x)}{L(\theta_1 \mid \underline x)} \le k$$and we try to get a statistic $T(\underline X) \le K$ or $T(\underline X) \ge K$, where $K$ is some constant resulting of the algebra. Then we determine $K$ using that $P(T(\underline X) \le K\mid \theta = \theta_0) = \alpha$ or $P(T(\underline X) \ge K\mid\theta =  \theta_0) = \alpha$, respectively, with that we have our test, being $$\gamma^*: \text{Reject }H_0 \text{ if } T(\underline X) \le K \text{ or } T(\underline X) \ge K \qquad (\text{depends of the case})$$