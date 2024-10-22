---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Random Variables]], [[Probability Functions for Random Variables]], [[Riemann-Steiltjes Integral on R]], [[Measuable Functions]]

## Expected Value
Let $X$ be a random variable with a distribution function $F$. The expected value of $X$, denoted as $E[X]$, it is defined as the number 

$$
E[X] := \int_{\Bbb R} x\, dF(x)
$$
when this integral is absolutely convergent, i.e.,  when the integral $\int_\Bbb R |x| \, dF(x)<\infty$ converges, in this case we say that $X$ is integrable or that it has finite expected value 

Let $X$ be discrete random variable with probability mass function $f$. The expected value of $X$ is defined to be 

$$
E[X]= \sum_{x} xf(x)
$$

supposing that the sum is absolutely convergent, meaning, when the sum of the values converges. 
In the particular cases:
Let $X$ be a absolutely continuous random variable with probability density function $f$, then the expected value is 

$$
E[X] = \int_\Bbb R x f(x) \, dx
$$
Let $X$ be a random variable with a distribution function $F_X$, and let $g:\Bbb R \to \Bbb R$ be a Borel measurable function, then $g(X)$ is a random variable, and we if try to calculate its expected value we get: 
$$
E[g(X)] = \int_\Bbb R x \, dF_{g(X)}(x)
$$
## **Law of the unconscious statistician**
Let $X$ be a random variable with a distribution function $F_X$, and let $g:\Bbb R \to \Bbb R$ be a Borel measurable function, such that the random variable $g(X)$ has finite expected value. Then 
$$
E[g(X)] = \int_\Bbb R g(x)\, dF_X(x)
$$
In the particular cases that:
Let $X$ be continuous random variable with probability density function $f$, and $g: \Bbb R \to \Bbb R$ be a function such that $g(X)$ is a random variable with finite expected value then 

$$
E[g(X) ]= \sum_x g(x)f(x)
$$

Let $X$ be discrete random variable with probability mass function $f$, and $g: \Bbb R \to \Bbb R$ be a function such that $g(X)$ is a random variable with finite expected value then 

$$
E[g(X) ]= \int_\Bbb R g(x)f(x)\, dx
$$

Let $(X, Y)$ be a random vector $\phi:\Bbb R^2\to \Bbb R$ be Borel measurable such that $\phi(X, Y)$ be a random variable with finite expected value. Then we define it as
$$
E[\phi(X, Y)] = \int_{\Bbb R} x\, dF_{\phi(X, Y)}(x)
$$
#### Expected Value of a Function of a Random Vector

Let $(X, Y)$ be a random vector $\phi:\Bbb R^2\to \Bbb R$ be Borel measurable such that $\phi(X, Y)$ be a random variable with finite expected value. Then we define it as
$$
E[\phi(X, Y)] = \int_{\Bbb R^2} \phi(x, y)\, dF_{X, Y}(x, y)
$$
using [[Riemann-Stieltjes Integral in Rn]]. In the special case where $X$ and $Y$ are independent. We can actually simplify it to two integrals
$$
E[\phi(X, Y)] = \int_{\Bbb R^2} \phi(x, y)\, dF_X(x)\, dF_Y(y)
$$

************Prop:************ Let $X$and $Y$ be continuous random variables defined over the same probability space with a conjoined probability density function $f(x,y)$. Let $g: \Bbb R^2 \to \Bbb R$ a function such that $g(X, Y)$ is a random variable with finite expected value. Then 

$$
E[g(X,Y)] = \int_\Bbb R \int_\Bbb R g(x,y) f(x,y)\, dy\, dx
$$

If the random variables are discrete with a conjoined probability mass function $f(x, y)$. Let $g: \Bbb R^2 \to \Bbb R$ a function such that $g(X, Y)$ is a random variable with finite expected value. Then 

$$
E[g(X,Y)] = \sum_x \sum _y g(x,y) f(x,y)
$$

************Prop:************ Properties of the expecte value. Let $X$ and $Y$ be random variables with finite expected value and $c$ a constant. Then 

- $E[c] = c$
- $E[cX] = cE[X]$
- If $X \ge0$, then $E[X] \ge 0$
- $E[X+Y] = E[X]+E[Y]$

Then we know that the expected value behaves linearly. 

Let $X$ be a random variable with a distribution function $F$, that admits a decomposition:
$$
F(x) =\alpha F^d(x) + (1-\alpha)F^c(x)
	$$with $0\le \alpha \le 1$, where $F^d$ is a discrete distribution function and  $F^d$ is a continuous one.  Let $X_d$ have the distribution $F^d$ and $X_c$ have the distribution $F^c$. Then, $X$ has a finite expected value, iff, $X_d$ and $X_c$ have finite expected value, and in that case
$$
E[X] = \alpha E[X_d]+ (1-\alpha)E[X_c]
$$

************Prop:************ Let $X$ and $Y$ be independent and both with finite expected values, and let $g, h:\Bbb R^2\to \Bbb R$ be Borel measurable and such that $g(X)$ and $h(Y)$ have a finite expected value. Then 

$$
E[g(X)h(Y)] = E[g(X)]E[h(Y)]
$$
in particular,
$$
E[XY] = E[X]E[Y]
$$

************Prop:************ Let $X$ be a discrete random variable with cumulative probability function $F(x)$, with a finite expected value and possible values in the set $\Bbb N$. Then 

$$
E[X] = \sum_{x \in \Bbb N}(1-F(x))
$$

Similarly, let $X$ be a continuous random variable with a cumulative probability function $F$, with finite expected value and values in the interval $[0, \infty)$. Then 

$$
E[X] = \int_0^\infty (1-F(x)) \, dx
$$
