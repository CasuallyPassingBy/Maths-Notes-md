---
tags:
  - ProbabilityTheory
  - GeneratingFunctions
---
Subjects: [[Probability Theory]]
Links: [[Random Variables]], [[Probability Functions for Random Variables]], [[Moments of Random Variable]], [[Convergence of Random Variables]]
## Moment Generating Function

The moment generating function $M$ of a random variable $X$ is the function $M(t)$ defined as 

$$
M(t) = E[e^{tX}]
$$

for the real values of $t$ where the expected value exists.

********Prop:******** Let $X$ be a random variable with a moment generating function $M$, defined for the values of $t$ on the interval $(-s, s)$ for some $s>0$. Then every moment of $X$ exists and $M(t)$ gets the form of the exponential power series 

$$
M(t) = \sum_{n \in \Bbb N} \frac{t^n}{n!}E[X^n]
$$

**Prop:** Let $X$ be a random variable with a moment generating function $M$ that is finite in the interval $(-s,s)$ for some $s>0$. Then for each $n  \in \Bbb N$

$$
\lim_{t\to 0}M^{(n)}(t) = E[X^n]
$$

**Prop:** Let $X$ and $Y$ be independent random variables with moment generating functions $M_X$  and $M_Y$. Then 

$$
M_{X+Y}(t) = M_X(t) M_Y(t)
$$

**Prop (Characterisation):** Let $X$ and $Y$ be discrete random variables with the same set of values $\Bbb N$ and with probability generating functions $M_X$ and $M_Y$, such that $M_X (t) = M_Y(t)$ for ${t \in (-s,s)}$ for some $s>0$. Then $X$ and $Y$ have the same distribution.

**Prop (Continuity of the Moment Generating Function):** Let $X_1, X_2, \dots$ be sequence of random variables such that $X_n$ has a Moment Generating Function $M_{X_n}(t)$. Let $X$ be another random variable with a moment generating function $M_X(t)$. If for every $t \in(-s,s)$ for some $s>0$,

$$
\lim_{n \to \infty} M_{X_n} (t)= M_X(t)
$$
iff $$X_n \stackrel{d}{\longrightarrow} X$$
