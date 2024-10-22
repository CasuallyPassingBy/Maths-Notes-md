---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Sufficient Statistics]]

While sufficiency is important to not lose information about the parameter. We would like the one that condenses the most the information.  The statistic is *minimal sufficient* if we reduce even more the information then any other statistic that is not sufficient. This also relate is also associated with the notion of equivalence classes or partitions of the sample space induced by a statistic. 

**Def:** We say that the statistic is minimal sufficient iff 
- it is sufficient
- Is the function of any other sufficient statistic; i.e., $S'(X)$ is a minimal sufficient iff there's $\varphi$ such that $S'(X) = \varphi[S(X)]$, where $S(X)$ is any other sufficient statistic.

Note that it this can be redescribed as an alternative way. Let $\{A_{S'}\}$ the elements of the partition associated with $S'(X)$ and $\{A_S\}$ the elements of the partition associated with $S(X)$, it has that 
- $S'(X)$ is minimal sufficient if for each $A_S$ is a subset of some $A_{S'}$, where $S(X)$ is sufficient, or
- $S'(X)$ is minimal sufficient if for any other sufficient statistic $S(X)$ induces a finer partition than $S'(X)$. This is also can be said that $S'(X)$ induces a partition that is more coarse than $S(X)$.

The minimal sufficient statistics are not unique, since given a sufficient minimal statistic, any bijective we can generate another one.

**Def:** Let $S(X)$ and $S'(X)$ be two statistics. WE say that $S'(X)$ is function of $S(X)$ if for any two $\underline x = (x_), \dots, x_n)$ and $\underline x' = (x_1', \dots, x_n')$ in the sample space $\frak X$, that satisfy $S(\underline x) = S(\underline x')$, it follows that $S'(\underline x) = S'(\underline x')$. 

**Def:** Two values $\underline x = (x_1, \dots, x_n)$ and $\underline x' = (x_1', \dots, x_n')$ in $Sup_f$, we say that $\underline x$ and $\underline x'$ are likelihood equivalent if there exists a constant $H(\underline x, \underline x')>0$, such that for all $\theta \in \Theta$, $$f_{X_1,\dots, X_n} (\underline x; \theta) = H(\underline x, \underline x') f_{X_1, \dots, X_n}(\underline x'; \theta)$$
Meaning $$L(\theta\mid \underline x) = H(\underline x, \underline x') L(\theta\mid \underline x')$$The $L$ represents the [[Maximum Likelihood estimators|Likelihood function]]
This relation is denoted as $$\underline x \sim_{\text{lik}} \underline x'$$
**Lemma:** Let $S(X)$ be a sufficient statistic and $\underline x$ and $\underline x'$ in $Sup_f$. If $S(\underline x) = S(\underline x') =s$, then $\underline x \sim_{\text{lik}} \underline x'$. 

**Th:** Let $X_1, \dots, X_n$ be a random sample of a population with a pdf $f(\underline x; \theta)$ and let $S'(X)$ be a sufficient statistic for $\theta$. Suppose that for two sample values $\underline x = (x_1, \dots, x_n)$ and $\underline x' = (x_1', \dots, x_n')$ in $Sup_f$ that are likelihood equivalent, i.e.,  $\underline x \sim_{\text{lik}} \underline x'$, it has that $S'(\underline x) = S'(\underline x')$. Then $S'(\underline X)$ is minimal sufficient. 

This result let's us have a systematic method for finding a minimal sufficient statistics. What we need to do is: for values $\underline x =(x_1, \dots, x_n)$ and $\underline x' =(x_1', \dots, x_n')$ in $Sup_f$, verifying the implication that that are likelihood equivalent over the or the implied statistic on the joint pdf. This is equivalent to calculate $$\frac{f_{X_1, \dots, X_n}(\underline x; \theta)}{f_{X_1, \dots, X_n}(\underline x'; \theta)}$$
and look under the condition (over the implied statistics) this quotient doesn't depend on $\theta$.  If if satisfies the hypothesis of theorem above, meaning, $$\frac{f_{X_1, \dots, X_n}(\underline x; \theta)}{f_{X_1, \dots, X_n}(\underline x'; \theta)} \text{ doesn't  depend on }\theta \implies S'(\underline x) = S'(\underline x')$$
Then $S'$ is minimal sufficient. 

**Cor:** Let $X_1, \dots, X_n$ be a random sample from a population with pdf $f(x; \theta)$ is of the form $$f(x; \theta) = a(\theta)b(x) \exp(c(\theta) d(x))$$meaning that $f(x; \theta)$ is part of the exponential family. Then $$\sum_{i = 1}^n d(X_i)$$ is a minimal sufficient statistic. 
