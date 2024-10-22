---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Gamma Distribution]]

We have a random variable $X$ has a beta distribution with parameters $a>0$ and $b>0$, denoted as $X \sim \text{B}(a,b)$ or $X \sim \operatorname{beta}(a,b)$, when its pdf is

$$ f(x; a,b) = \begin{dcases} \frac{1}{\text{B}(a,b)}x^{a-1}(1-x)^{b-1} &0\le x \le 1 \\ 0 \end{dcases} $$

Where in this context, $\text{B}(a,b)$ represents the beta function.

We can calulate the cdf as

$$ F(x) = \begin{dcases} 0 & x \le 0 \\ \frac{1}{\text{B}(a,b)}\int_0^xu^{a-1}(1-u)^{b-1}\, du & 0<x<1 \\ 1 & x\ge1 \end{dcases} $$

where the integral above can be simplified into

$$ F(x) = \begin{dcases} 0 & x \le 0 \\ I_x(a,b) & 0<x<1 \\ 1 & x\ge1 \end{dcases} $$

where $I$ is the regularised incomplete beta function

We can get that

- $E[X] = \dfrac{a}{a+b}$
    
- $\operatorname{Var}[X] = \dfrac{ab}{(a+b+1)(a+b)^2}$
    
- The mode is $\dfrac{a-1}{a+b-2}$
    
- The median is $I^{[-1]}_{1/2}(a,b)$, where this is the inverse of the regularised incomplete beta function, this is dumb, but we can estimate it if $a, b\ge 1$, then
    
    $$ \operatorname{median} \approx \frac{a-\frac{1}{3}}{a+b-\frac{2}{3}} $$
    

Let $X$ and $Y$ be independent random variables with distribution $\Gamma(a,\lambda)$ and $\Gamma(b,\lambda)$, respectively. Then

$$ \frac{X}{X+Y} \sim \text{B}(a,b) $$

We can calculate the $n$th moment of $X$ as

$$ E[X^n] = \frac{\text{B}(a+n, b)}{\text{B}(a,b)} = \frac{a^{\overline n}}{(a+b)^{\overline n}} $$

where $a^{\overline n}$ represents the rising factorial of $a$