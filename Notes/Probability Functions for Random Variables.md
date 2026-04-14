---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Random Variables]]
### Discrete Random Variable

Let $X$ be a discrete random variable with values $x_0, x_1, x_2, \dots$. The function of probability of $X$, denoted as $f_X : \Bbb R \to \Bbb R$ and defined as

$$ f_X(x) = \begin{cases} \Bbb P(X = x) & \text{if }x =x_0, x_1, x_2,\dots \\ 0 & \text{otherwise} \end{cases} $$

With this definition we can get that

$$ \Bbb P(X \in A) = \sum_{x \in A} f(x) $$

We call $f_X$ the probability mass function of $X$

### Continuous Random Variable
Let $X$ be a continuous random variable. We say that nonnegative integrable function $f: \Bbb R \to \Bbb R$ is the density function of $X$ if for any $[a,b]$ of $\Bbb R$, satisfies that

$$ \Bbb P(a \le X \le b) = \int_a^b f(x)\, dx $$

$f$ is called a the probability density function of $X$, and satisfies the following properties
- $f \ge 0$
- $\int_\Bbb R f =1$

We say that $f$ is symmetric with respect to $a$, if $f(a+x) = f(a-x)$

We can define the *support of the pdf/pmf* $$\text{Sup}_f = \{x \mid f(x) > 0\}$$

## **Cumulative distribution function**

Let $X$ be a random variable. The cumulative distribution function of $X$, denoted as $F_X: \Bbb R \to \Bbb R$, is defined as $$ F_X(x) = \Bbb P(X \le x) $$In the discrete case we get that $$ F(x) = \sum_{u \le x}f(u) $$In the continuous case we get that $$ F(x) = \int_{-\infty}^x f(u)\, du $$

**Prop:** Let $F$ and $G$ be cpd, then any linear convex combination is a cpd

**************Def:************** We say that random variable $X$ is continuous if its cumulative distribution function $F_X$ is continuous.

We can get the probability density function, from $F_X$.

In the continuous case, by the FTC, we get that
$$ f(x) = F'(x) $$

and in the discrete case we get that
$$ f(x) = F(x+) -F(x-) $$

with
$$ F(x+) := \lim_{h \to 0^+}F(x+h) \quad \text{ and } \quad F(x-) := \lim_{h \to 0^-}F(x+h) $$

**Prop:** Any cumulative distribution function $F$ satisfies:
- $\lim\limits_{x \to \infty} F(x) = 1$
- $\lim\limits_{x \to -\infty} F(x) = 0$
- If $x_1 \le x_2$, then $F(x_1) \le F(x_2)$
- $F(x) = F(x+)$

********Def:******** Any function $F:\Bbb R \to \Bbb R$ that satisfies the $4$ properties above is called a cumulative distribution function.

Let $F:\Bbb R \to [0, 1]$ be distribution function. Then there's a probability space $(\Omega, {\scr F}, P)$ and a random variable such that $F$ is the its distribution function.

**Prop:** Probability of events in terms of $F(x)$

$$ \begin{aligned}\Bbb P(X<a) & =F(a-) . \\\Bbb P(a<X \leqslant b) & =F(b)-F(a) . \\\Bbb P(a \leqslant X \leqslant b) & =F(b)-F(a-) . \\\Bbb P(a<X<b) & =F(b-)-F(a) . \\\Bbb P(a \leqslant X<b) & =F(b-)-F(a-) .\end{aligned} $$

Every distribution function has at most a countable number of discontinuities. This is because it is bounded and monotone.

The distribution function $F$ it can be written as a convex linear combination of a discrete distribution function $F^d$ and a continuous one $F^d$, i.e., admits the following representation $$
F(x) =\alpha F^d(x) + (1-\alpha)F^c(x)
$$with $0\le \alpha \le 1$. 

We can see that a continuous distribution function $F$ can be written as a convex linear combination of a absolutely continuous distribution function $F^a$ and a singular one $F^s$, i.e., admits the following representation

$$
F(x) =\alpha F^a(x) + (1-\alpha)F^s(x)
$$with $0\le \alpha \le 1$. 

Thus we can make a decomposition of any distribution function as the a convex linear combination of the three basic types.

**Def:** If the cdf $F$ is strictly inpcreasing and continuous, then $F^{-1}(p)$, for $p\in [0, 1]$, is the unique real number $x$ such that $F(x) = p$. This defined the *inverse distribution function* of *quantile function*. 

Some distributions do not have a unique inverse. In this case, one may use the *generalized inverse distribution function*, which is defined as $$F^{-1}(p) = \inf\{x \in \Bbb R\mid F(x) \ge p\}, \qquad p\in [0, 1].$$


^a5f289
