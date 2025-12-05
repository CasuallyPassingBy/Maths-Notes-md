---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Statistical Hypothesis Test]]

**Def:** Let $T(\underline X)$ be a test statistic that for large values of $T$ give evidence in favor of the alternative hypothesis. For each possible value of $\underline X$, $$\underline x= (x_1, \dots, x_n)\in \frak X$$we define the $p$-value as $$p(\underline x) = \max_{\theta \in \Theta_0}P(T\underline (X)) \ge t(\underline x))$$where $t(\underline x)$ is the value of the statistic $T(\underline X)$ on $\underline x$.  

The inequality of the probability would be inverted if for smaller values of $T$ give evidence in favor of the alternative hypothesis. 

A $p$-value, $p(\underline x)$, satisfies that $0\le p(\underline x) \le 1$ for each value of the sample $\underline x$. Small values of $p(\underline x)$ give evidence in favor of the alternative hypothesis $H_1$ being true. 

It is fairly easy to construct a test with significance $\alpha$ based in $p(\underline X)$. The test is we reject the null hypothesis $H_0$ iff $p(\underline x) \le \alpha$. There's an advantage of reporting the result of the hypothesis test using the $p$-value is that each individual can choose a level $\alpha$, called the *level of significance of the test*, that thinks is adequate, then we can compare $p(\underline x)$ with $\alpha$ and reject or not reject $H_0$. 

If a $p$-value is small, we say that the sample produced an usual result under the null hypothesis. This means that the null hypothesis is likely to be inconsistent with the sample, thus we reject it. On the other hand, if a $p$-value is large, then the sample is consistent with the null hypothesis, and we don't reject the null hypothesis.

If we would like to use the $p$-value to take a decision if $H_0$ will be rejected, then we need to select a value $\alpha$, the level of significance. If the $p$-value is less than or equal to $\alpha$, then we must reject $H_0$, and the test is statistically significant; if this wasn't the case, we don't reject $H_0$, and the test is not statistically significant. The $p$-value gives us not only a way to make the decision of rejecting or not rejecting the null hypothesis, but also an idea on how strong is the evidence against the null hypothesis. 

If we use an asymptotic distribution to calculate the test statistic to find the $p$-value, we call this $p$-value and asymptotic $p$-value.  

**Def:** To calculate the corresponding $p$-value of a region with a bilateral rejection, we define it as $$p(\underline x) := 2\min\{P(T(\underline X) \ge t(\underline x)), P(T(\underline X) \le t(\underline x))\} $$