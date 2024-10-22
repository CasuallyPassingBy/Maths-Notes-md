---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Chi-squared Distribution]]

A random variable $X$ is has an $F$ distribution with parameters $a >0$ and $b>0$, written as $X \sim F(a,b)$, if the pdf is

$$ f(x;a,b) = \begin{dcases} 0 & x\le 0 \\ \frac{\Gamma(\frac{a+b}{2})}{\Gamma(\frac{a}{2})\Gamma(\frac{b}{2})}\left(\frac{a}{b}\right)^{a/2} x^{a/2-1}\left(1+\frac{a}{b}x\right)^{-(a+b)/2} & x>0 \end{dcases} $$

We have that the cdf is

$$ F(x; a, b) = I_{\frac{ax}{ax+b}}\left(\frac{a}{2}, \frac{b}{2}\right) $$

where again the $I$ represents the [[Beta Function#Incomplete Beta Function|regularized incomplete beta function]].

We have that

- $E[X] =\dfrac{b}{b-2}$, for $b>2$
- $\operatorname{Var}[X] = \dfrac{2b^2(a+b-2)}{a(b-2)^2(b-4)}$, for $b>4$
- The mode is $\dfrac{a-2}{a} \dfrac{b}{b+2}$, for $a>2$

Let $X\sim \chi^2(a)$ and $Y\sim \chi^2(b)$ be indpendent random variables. Then

$$ \frac{X/a}{Y/b} \sim F(a,b) $$

We can calculate the $n$th moment of $X$, as

$$ E[X^n] = \left(\frac{b}{a}\right)^n\frac{\Gamma(a/2+n)}{\Gamma(a/2)}\frac{\Gamma(b/2-n)}{\Gamma(b/2)} $$

there’s no moment generating function.

And if $X \sim F(a,b)$, then

$$ \frac{1}{X }\sim F(b,a) $$