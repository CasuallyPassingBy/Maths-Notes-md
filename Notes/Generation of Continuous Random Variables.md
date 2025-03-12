---
tags:
  - StochasticSimulation
---
Subjects: [[Stochastic Simulation]]
Links: [[Pseudo-random number generator]]

Since we can generate a random number $U \sim \text{Unif}(0, 1)$, a natural progression is to transform it into another continuous random variable. There are different methods.

# Method of the Inverse Transform

Let $U \sim \text{Unif}(0, 1)$ and $Y$ be a random variable independent of $U$, with continuous cdf $F_Y$. If $Z = F^{-1}(U)$, then $Z \stackrel{d}{=}Y$, i.e., $F_Z = F_Y$. 

The main problem with this method is that finding an inverse can be really complicated, or there can be cases where there is no inverse. 

The inverse transform sampling method works as follows:
- Generate a random number $u$ from the standard uniform distribution in the interval $[0, 1]$, i.e. from $U \sim \text{Unif}[0, 1]$.
- Find the [[Probability Functions for Random Variables#^a5f289|generalised inverse]] of the desired cdf, i.e. $F_X^{-1}(u)$
- Compute $X'(u) = F_X^{-1}(u)$. The computed random variable $X'(U)$ has distribution $F_X$ and thereby the same law as $X$.

```python
import micropip
await micropip.install('numpy')
import numpy as np

def inverse_transform_sampling(inverse_cdf):
	u = np.random.uniform()
	return inverse_cdf(u)

mean = 2
inverse_exponential_cdf = lambda p: -np.log(1-p)*mean
sampling = lambda : inverse_transform_sampling(inverse_exponential_cdf)
print(sampling())
```

# Method of Rejection Sampling

The rejection sampling method generates sampling values from a target distribution $X$ with an arbitrary pdf $f(x)$ by using a proposal distribution $Y$ with pdf $g(x)$. The idea is that one can generate a sample value from $X$ by instead sampling $Y$ and accepting the sample from $Y$ with probability $\dfrac{f(x)}{M(g(x)}$, repeating the draws from $Y$ until a value is accepted. $M$ here is a constant, finite bound on the likelihood ration $\dfrac{f(x)}{g(x)}$; in other words $M$ must satisfy $f(x) \le Mg(x)$ for all values of $x$. This implies that if $f(x) > 0$, then $g(x) >0$.

The algorithm is as follows: Let $X$ be a random variable with pdf $f$, and $Y$ be a random variable with density $g$:
- Obtain a sample $y$ from the distribution $Y$ and a sample $u$ from $\text{Unif}(0, 1)$,
- Check if $u < \dfrac{f(y)}{Mg(y)}$.
	- If this holds, accept $y$ as sample drawn from $f$.
	- If not, reject the value of $y$ and return to the sampling step.

```python
def rejection_sampling(goal_pdf, M, auxiliary_pdf, auxiliary_sample):
	while True:
		u = np.random.uniform()
		y = auxiliary_sample()
		if u < goal_pdf/(M*auxiliary_pdf):
			return y
```


# Ratio of Uniforms

Given that is easy to generate uniform random variables, the idea of the method of uniform ratios is to transform two variables $U$ and $V$, uniformly distributed on some range, into a random variable $X$ with the desired distribution.

**Th:** Let $h(x)$ be a nonnegative function with $\int h(x)\, dx < \infty$. We define $$R_h := \left\{(u, v)\in [a, b] \times [c, d] \mid 0 \le u \le \sqrt{h\left(\frac{v}{u}\right)}\right\},$$ for $a,b, c, d \in \Bbb R$, and $$f(x) := \frac{h(x)}{\int h(x)\, dx}.$$If $(U, V)$ is a bivariate random vector uniformly distributed over $R_h$, then $X := V/U$ has density $f$.

From this theorem we get the following algorithm:
- We generate $U\sim \text{Unif}(a, b)$ and $V \sim \text{Unif}(c, d)$.
- Check if $0 \le U^2 \le {h(V/U)}$
	- if it is true, then accept the value $X = V/U$.
	- If not, then go back to the generation step. 

This is particularly useful for generating a target density that is only known *up to a normalising constant*, i.e. $f(x) = ch(x)$ for $h(x)$ known but not $c = (\int h(x)\, dx)^{-1}$. 

The following result may be useful:

**Th:** Suppose $h(x)$ and $x^2h(x)$ are bounded. Then $R_h \subseteq [0, a] \times [b, c]$ where $$a := \sup_x \sqrt{h(x)}, \quad b := \inf_{x\le 0} x \sqrt{h(x)}, \quad c = \sup_{x\ge 0} x \sqrt{h(x)}$$
This helps us get the most efficient $a$, $b$ and $c$. 

```python
def uniform_ratio(bounding_function, a_bound, b_bound, c_bound):
	while True:
		u1, u2 = np.random.uniform(size = 2)
		u = a_bound * u
		v = b_bound + v *(c_bound - b_bound)
		if u*u <= bounding_function(v/u):
			return v/u
```
