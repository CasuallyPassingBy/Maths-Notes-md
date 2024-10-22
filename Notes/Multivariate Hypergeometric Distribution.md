---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]], [[Hypergeometric Distribution]]

As the name implies we are extending the notion of the Hypergeometric distribution.

Let's suppose we have $N$ objects, and we have $k$ types, each type as $N_i$ objects, for $i =1, \dots, k$. Then $N=(N_1, \dots, N_k)$. Let's suppose we take $n$ objects without putting it back, and we define the random variables $X_1, \dots, X_k$ as the number of objects of each type. We have the random vector $X= (X_1, \dots, X_k)$ has a multivariate hypergeometric distribution with a probability mass function of the form 
$$
f(x; N) =\frac{{N\choose x}}{|N| \choose |x|)}
$$
I am using [[Multi-index notation]] to make it easier and simpler to state, but it can be written as

$$
f(x_1, \dots, x_k; N_1, \dots, N_k) = \frac{\prod\limits_{i= 1}^k {N_i\choose x_i}}{N\choose n}
$$
