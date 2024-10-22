---
tags:
  - SpecialFunctions
---
Subjects: [[Special Functions]]
Links: [[Gamma Function]]
## Pi function

The $\Pi$ function defined by Gauss, as $\Pi: \Bbb C\setminus \Bbb Z^- \to \Bbb C$ as

$$ \Pi(z) = \Gamma(z+1) = z\Gamma(z) = \int_0^\infty t^z e^{-t}\,dt $$

and that for $n \in \Bbb N$, we have that

$$ \Pi(n) = n! $$

And we have that if $z \not \in \Bbb Z$, then

$$ \Pi(z) \Pi(-z) = \frac{\pi z}{\sin(\pi z)} = \frac{1}{\operatorname{sinc}(\pi z)} $$

### Incomplete gamma function

We can define two multivariable functions defined as the upper incomplete gamma function as

$$ \Gamma(s, x) = \int_x^\infty t^{s-1}e^{-t}\, dt $$

and the incomplete lower gamma function as

$$ \gamma(s,x) = \int_0^xt^{s-1}e^{-t}\, dt $$

They have the property of $\Gamma(s, x) +\gamma(s, x) = \Gamma(s)$, and that

$$ \Gamma(s, 0) = \Gamma(s) = \lim_{x\to \infty }\gamma(s, x) $$

Using integration by parts we can ge the following results

$$ \Gamma(s+1, x) = s\Gamma(s, x) + x^s e^{-x} \\ \gamma(s+1, x) = s\gamma(s, x) - x^s e^{-x} $$

the lower incomplete gamma function appears when solving the differential equation $xy''+(x+n)y'+ny=0$. The fundamental set of solutions is: $e^x$ and $e^{x}\gamma(n+1, x)$

### Regularized Incomplete Gamma functions

We can define the regularized lower incomplete gamma function as

$$ P(s,x) = \frac{\gamma(s,x)}{\Gamma(s)} $$

and the regularized upper incomplete gamma function as
$$ Q(s,x) = \frac{\Gamma(s,x)}{\Gamma(s)} = 1-P(s,x) $$

It is used a lot in probability theory, in particular for the random varible $X$ with a [[Gamma Distribution|gamma distribution]], then

$$ P(X \le x) = P(s, x) $$

and the cdf of a random variable $X \sim \operatorname{Poi}(\lambda)$ (with [[Poisson Distribution]]), we get that

$$ P(X \le s) = Q(s, \lambda) $$
If we calculate the logarithmic derivative, we get that 
$$
\psi_0 (x)=\frac{d}{dx}\ln (\Gamma (x)) = \frac{\Gamma'(x)}{\Gamma(x)}
$$
Which is the definition of the [[Digamma function]]