---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Statistics and Sample Distribution]]

We can say that a statistic $S(\underline X)$ is *sufficient* if it conserves all the information that the random sample $\underline X$ has about $\theta$. In other words it is *sufficient* to know about the statistic $$S(\underline X)$$
to know about the same parameter of the random sample. 

**Def:** Let $X_1, \dots, X_n$ be a random sample of a population with pdf $f(x; \theta)$. The statistic $S(\underline X)$  is *sufficient* iff the conditional density function of $X_1, \dots, X_n$ given $S(\underline X) =s$, doesn't depend on $\theta$. The set of all possible values of $\theta$ is denoted $\Theta$, and is called *parameter space*

### Factorisation Theorem
Let $X_1, \dots, X_n$ be a random sample of a population with pdf $f(x;\theta)$; $S(\underline X)$ is sufficient iff, joint pdf of $X_1, \dots, X_n$ can be factored as $$f_{X_1, \dots, X_n} (x_1, \dots, x_n) = g(S(\underline x); \theta) \cdot h(x_1, \dots, x_n)$$
where $g$ and $h$ are nonnegative function such that $g(S(\underline x); \theta)$ depends on the sample only through $S(\underline x)$, and the parameter $\theta$; and $h(x_1, \dots, x_n)$ doesn't depend on $\theta$. 

## The exponential family

We say that $f(x; \theta)$ is part of the exponential family, or exponential class, if it can be factored as $$f(x; \theta) = a(\theta)b(x) e^{c(\theta )d(x)} $$Where $a(\theta)$ and $c(\theta)$ are function of $\theta$, and $b(x)$ and $d(x)$ are functions of $x$. 

Some of the distributions that are more well known that are part of the exponential family:
- Binomial
- Geometric
- Negative Binomial
- Poisson
- Gamma
- Normal
- Beta
- Rayleigh

**Prop:** Let $X_1, \dots, X_n$ be a random sample from a population with pdf $f(x; \theta)$ is of the form $$f(x; \theta) = a(\theta)b(x) \exp(c(\theta) d(x))$$meaning that $f(x; \theta)$ is part of the exponential family. Then $$\sum_{i = 1}^n d(X_i)$$ is a sufficient statistic. 

**Prop:** Let $X_1, \dots, X_n$ be a random sample from a population with a pdf $f(x; \underline \theta)$, where $\theta$ is a parameter vector. The statistics $S_1(\underline X), \dots, S_r(\underline X)$, $r \ge k$, are jointly sufficient statistics iff there exist two functions: $g(S_1, \dots, S_r; \underline \theta)$ that only depends on the sample through the statistics, and $\underline \theta$; and $h(\underline X)$ is any nonnegative function that only depends on the samples, which for the joint density function $$f_{\underline X}(\underline x, \underline \theta)$$can be factored as $$f_{\underline X}(\underline x; \underline \theta) = g(S_1, \dots, S_r; \underline \theta) h(\underline x) $$
### $k$-parametric Exponential families

When the parametric famiky has more than one paramenter, meaning that its densiity function is of the form $f(x; \underline \theta)$ with $\underline \theta \in \Bbb R^k$, we say that belongs the the $k$-parametric family iff it can be expressed of the form 
$$f(x; \underline \theta) = a(\underline \theta) b(x) \exp\left(\sum_{j = 1}^k c_j(\underline \theta) d_j(x) \right)$$