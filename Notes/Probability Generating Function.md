---
tags:
  - ProbabilityTheory
  - "#GeneratingFunctions"
---
Subjects: [[Probability Theory]]
Links:, [[Probability Functions for Random Variables#Discrete Random Variable|Discrete Random Variables]]

Let $X$ be a discrete random variable with possible values in the set $\Bbb N$. The function $G(t)$, defined as 

$$
G(t) = E[t^X]= \sum_{x \in \Bbb N}t^x P(X = x)
$$

is called the probability generating function of $X$

**Prop:** Let $X$ be a discrete random variable with values in $\Bbb N$ and probability generating function $G(t)$. For $x \in \Bbb N$ 

$$
P(X =x) \frac{1}{x!}G^{(x)}(0)
$$

**Prop:** Let $X$ be a discrete random variable with values in $\Bbb N$ and probability generating function $G(t)$. If the $k$th moment of $X$ exists, then 

$$
G^{(k)}(1-)= E[X(X-1)(X-2)\cdots(X-k+1)] = E[X^{\underline k}]
$$

with $X^{\underline k}$ referring to the the falling factorial of $X$.

**Prop:** Let $X$ and $Y$ be independent discrete random variables with probability generating functions $G_X(t)$ and $G_Y(t)$. Then 

$$
G_{X+Y}(t) = G_X(t) G_Y(t)
$$

**Prop (Characterization):** Let $X$ and $Y$ be discrete random variables with the same set of values $\Bbb N$ and with probability generating functions $G_X$ and $G_Y$, such that $G_X (t) = G_Y(t)$ for ${t \in (-s,s)}$ for some $s>0$. Then $X$ and $Y$ have the pmf.