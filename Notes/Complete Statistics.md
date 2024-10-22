---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Statistics and Sample Distribution]], [[Sufficient Statistics]], [[Minimal Sufficiency for Statistics]]

**Def:** Let $X_1, \dots, X_n$ be a random sample of $f(x;\theta)$, $\theta \in \Theta$. We say that a statistic $T(\underline X)$ is complete iff, for any function $g$ of $T$, we have that if $E(g(T)) = 0$, $\forall \theta \in \Theta$, then $$P(g(T) = 0) = 1, \; \forall \theta \in \Theta$$We also say that the *family of densities of $T$ is complete*

In general, we can say that a parametric family $f(x; \theta)$ is complete if $E[g(X)] = 0$ implies that $g (x) = 0\; a.s.$.  In this context, if $f(x;\theta)$ belongs to the exponential family, then $f(x;\theta)$ is complete. This is partially because the [[Laplace transform]] is unique up to $a.s.$. 

Then if $f(x; \theta)$ is belong in the exponential family, then $\sum\limits_{i  = 1}^n d(X_i)$ is complete. 
**Th**: Let $X_1, \dots, X_n$ be a random sample of a population with pdf $f(x; \theta)$ with $\theta \in \Theta\subseteq \Bbb R$, where $f(x; \theta)$ is part of the exponential family, meaning, $f(x; \theta) = a(\theta)b(x) \exp[c(\theta) d(x)]$. Then the statistic $\sum\limits_{i = 1}^n d(X_i) is minimal sufficient and complete. 

**Th:** Let $X_1, \dots, X_n$ be a random sample with a of a population with a density function $f(x; \theta)$, with $\underline \theta \in  \Theta \subseteq \Bbb R^k$, that belongs to the $k$-parametric exponential family, meaning $$f(x; \underline \theta) = a(\underline \theta) b(x) \exp\left(\sum_{j = 1}^k c_j(\underline \theta) d_j(x) \right)$$
Then the set of statistics $$\left(\sum_{i = 1}^n d_1(X_i), \sum_{i = 1}^n d_2(X_i), \dots, \sum_{i = 1}^n d_n(X_i)\right)$$
