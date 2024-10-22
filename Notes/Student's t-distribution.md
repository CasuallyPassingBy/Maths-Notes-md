---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Chi-squared Distribution]], [[Hypergeometric Function]], [[Normal Distribution]]

A random variable $X$ has a $t$ distribution with parameter $n>0$, written as $X\sim t(n)$, if the pdf is

$$ f(x;n ) = \frac{\Gamma((n+1)/2)}{\sqrt{n\pi}}(1+x^2/n)^{-(n+1)/2} = \frac{1}{\sqrt n \text{B}(\frac{1}{2}, \frac{n}{2})}(1+x^2/n)^{-(n+1)/2} $$

We can get the cdf for $x>0$, as

$$ F(x;n ) = 1-I_{y(x)} \left(\frac{n}{2}, \frac{1}{2}\right) $$

where $y(x) = \dfrac{n}{x^2+n}$, and $I$ is the regularized incomplete beta function, and the use of symmetry we can find it all. The complete formula is

$$ F(x;n)=\dfrac{1}{2} + t\frac{\Gamma \left( \dfrac{1}{2}(n+1) \right)} {\sqrt{\pi n}\,\Gamma \left(\dfrac{n}{2}\right)} \, {}_2F_1 \left( \dfrac{1}{2}, \dfrac{1}{2}(n+1); \dfrac{3}{2}; -\dfrac{t^2}{n} \right), $$

where $_2 F_1$ is a particular case of the hypergeometric function, which is also a mess

We can see that

- $E[X] =0$, for $n >1$
- $\operatorname{Var}[X] = \dfrac{n}{n-2}$ for $n >2$, $\infty$ for $1 < n \le 2$, otherwise undefined
- The mode is $0$
- The median is $0$

Let $X \sim N(0,1)$ and $Y \sim \chi^2(n)$ are two independent random variables, then

$$ \frac{X}{\sqrt{Y/n}}\sim t(n) $$

Let $X_1, \dots, X_n$ be independent random variables each distriburtd as $N(\mu, \sigma^2)$. In addition we define

$$ \bar X = \frac{1}{n}\sum_{i = 1}^n X_i \qquad S^2 = \frac{1}{n-1}\sum_{i = 1}^n(X_i -\bar X)^2 $$

with this we get that

$$ \frac{\bar X-\mu}{S/\sqrt n} \sim t(n) $$

We can calculate the $m$th moments of $X$,

$$ E[X^m]=\begin{dcases}0 & m \text{ odd},\quad 0<m< n\\ \frac{1}{\sqrt{\pi}\Gamma\left(\frac{n}{2}\right)}\left[\Gamma\left(\frac{m+1}{2}\right)\Gamma\left(\frac{n-m}{2}\right)n^{m/2}\right] & m \text{ even}, \quad 0<m< n\\ \end{dcases} $$

with $m<n$, if $m\ge n$, then the moment doesn't exist. For this reason there’s no moment generating function. We can calculate the characteristic function is $$\phi(t) = e^{|t|} \qquad n = 1$$

We have that the median and mode of $t(n)$, are both $0$

### Convergence to the Standard normal

Let $f(x;n)$ be the pdf of $t(n)$, then

$$ \lim_{n\to \infty} f(x;n) = \frac{1}{\sqrt{2\pi}}e^{-x^2/2} $$