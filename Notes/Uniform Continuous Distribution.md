---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]]

Let $X$ be a radom variable with uniform distribution on the interval $(a,b)$, and we write ${X \sim \operatorname{unif}(a,b)}$, when the pdf is of the form

$$ f(x) \begin{dcases} \dfrac{1}{b-a} & x \in (a,b) \\ \\ 0 \end{dcases} $$

We have the pdf of the form

$$ F(x) = \begin{dcases} 0 & x \le a \\ \frac{x-a}{b-a} & x \in[a,b] \\ 1 & x \ge b \end{dcases} $$

We have that

- $E[X] = (b+a)/2$
- $\operatorname{Var}[X] = (b-a)^2/12$
- The mode is the interval $(a,b)$
- The median is $\dfrac{b+a}{2}$

We can actually calculate the $n$th moment

$$ E[X^n] = \frac{b^{n+1}-a^{n+1}}{(n+1)(b-a)} $$

and the moment generating function we get that

$$ M(t) = \frac{e^{bt}-e^{at}}{t(b-a)} $$
And the characteristic function is $$ \phi(t) = \frac{e^{bit}-e^{ait}}{it(b-a)} $$