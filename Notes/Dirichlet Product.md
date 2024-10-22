---
tags:
  - NumberTheory
  - AnalyticNumberTheory
---
Subjects: [[Elementary Number Theory]], [[Analytic Number Theory]]
Links: [[Dirichlet Series]]
**********Def:********** A real/complex valued function defined on the positive integers is called an _**********arithmetic function**********_ or ****************number theoretic function****************.

**********Def:********** Let $f$ and $g$ are arithmetic functions we can define their **Dirichlet product** or ****Dirichlet convolution**** as

$$ (f*g)(n) =\sum_{d\mid n}f(d)g\left(\frac{n}{d}\right) = \sum _{a \cdot b =n} f(a)g(b) $$

************Th:************ Dirichlet multiplication is commutative and associative:

$$ f_g = g_f \\ f*(g_h)=(f_g)*h $$

********Th:******** Dirichlet multiplication is distributive over the sum of functions, in other words

$$ f _(g+h) = f_g+f*h $$

**********Def:********** Let $\varepsilon$ or $I$ be a function defined as for a $n\ge 1$

$$ I(n) = \begin{cases} 1 & \text{if } n = 1\\ 0 & \text{otherwise} \end{cases} $$

********Th: $I$** is a completely multiplicative function.

********Th:******** The function $I$ behaves as the identity using the Dirichlet product, in other words, if $f$ is an arithmetic function then

$$ f * I =I*f = f $$
**********Def:********** Let $f$ and $g$ be arithmetic functions the if

$$ f*g = I $$

then $g$ is called the ********************_Dirichlet Inverse of $f$, and denoted $f^{-1}$_

****Prop:**** Let $f$ and $g$ be arithmetic functions then

$$ (f*g)^{-1} = f^{-1} * g^{-1} $$

********Th:******** Let $f$ be an arithmetic function. If $f(1) \ne 0$ then has a unique arithmetical function $f^{-1}$, being the Dirichlet Inverse, in other words

$$ f*f^{-1} = f^{-1} * f = I $$

Moreover, $f^{-1}$ is given by the recursion formulas

$$ f^{-1}(1) =\frac{1}{f(1)}, \quad

f^{-1} (n) = \frac{-1}{f(1)} \sum_{\substack{d\mid n \\ d < n}} f\left(\frac{n}{d}\right)f^{-1}(d) \quad \text{for }n >1 $$


**********Th:********** Given this we can conclude that the set of arithmetic functions, with pointwise addition and the Dirichlet product form a commutative ring, with $I$ being the multiplicative identity, and the $0$ function being the additive one. This is called the **************Dirichlet ring************** ********************