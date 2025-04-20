---
tags:
  - Miscellaneous
---
Subjects: [[Umbral calculus]]
Links: [[Delta Operators]], [[Falling and Rising Factorials and Pochhamer Symbols]], [[Digamma function|Harmonic Numbers]]

Let $f$ be a function, we define the forward difference or the discrete derivative as $$\Delta f(n) := f(n+1) - f(n).$$It has the following properties:
- $\Delta(\lambda f+ g)(n) = \lambda \Delta f(n) + \Delta g(n)$ for any $\lambda$.
- $\Delta(fg)(n) = f(n+1) \Delta g(n) + \Delta f(n) g(n) = f(n) \Delta g(n) + \Delta f(n) g(n) +\Delta f(n) \Delta g(n).$
- $\Delta(f/g)(n) = \dfrac{\Delta f(n) g(n) - f(n)\Delta g(n)}{g(n)g(n+1)}$, when the denominator is nonzero. 

Let us see that $\Delta = E + I$, where $E$ is the right shift operator, from this we see that $E^a\Delta = \Delta E^a$ for any $a$. Thus $\Delta$ is a *delta operator*.

The sequence of basic polynomials of $\Delta$ are the falling factorial of $x$. Meaning that $$\Delta x^{\underline n} = n x^{\underline{n-1}}$$
We also have what is called the *backward difference* $\nabla$, and it is defined as $$\nabla f(n) := f(n) - f(n-1).$$It has the following properties:
- $\nabla(\lambda f+ g)(n) = \lambda \nabla f(n) + \nabla g(n)$ for any $\lambda$.
- $\nabla(fg)(n) = f(n-1) \nabla g(n) + \nabla f(n) g(n) = f(n) \nabla g(n) + g(n) \nabla f(n) - \nabla f(n)\nabla g(n)$
- $\nabla(f/g)(n) = \dfrac{\nabla f(n) g(n-1) - f(n-1)\nabla g(n)}{g(n)g(n-1)}$, when the denominator is nonzero. 

We also see that the backward difference is a delta operator. The falling factorial almost behaves like the basic sequence of polynomials of $\nabla$, since $$\nabla x^{\underline n} = n(x-1)^{\underline n}.$$$The true basic polynomials of $\nabla$ are the *rising factorial*, and we get that $$\nabla x^{\overline n} = nx^{\overline n}.$$Similarly, we get that $$
\Delta x^{\overline n} = n(x+1)^\overline n.
$$
Let's see how powers behave under this delta operators. $\Delta a^n = (a-1) a^n$. With this in mind, we can see that $\Delta 2^n = 2^n$. In this context, we say that $2$ is the discrete equivalent of $e$. We also see the following $$\Delta(1+\lambda)^n = \lambda (1+\lambda)^n. $$This behaves even more like $e^{\lambda x}$. 

If we try to do the same on the backward difference, we actually see that is not possible, and the only value that is acceptable is $0$, but we can get something similar $$\nabla \left(\frac{1}{(1-\lambda)^n}\right) = \frac{\lambda}{(1-\lambda)^n}.$$This shows that there would be no constant that behaves like $e$ for $\nabla$. 

We also have a discrete analogue of integration.  For the forward difference from $a$ to $b$ is defined as $$\sum_{n : a\to b} f(n) := \sum_{n = a}^{b-1} f(n)$$This is because we have the identity $$\sum_{n :a\to b}\Delta f(n) = f(b) - f(a).$$Meaning that we have a discrete analogue of the fundamental theorem of calculus. With this theorem we have the following  identity for $m \ne -1$ $$\sum_{n : 0 \to x} n^\underline m = \frac1{m+1} x^{\underline{m+1}}.$$
Just as $\frac1{x}$ has a complicated integral, we also have that $\sum n^{\underline {-1}}$ is non trivial. We get that $$H_m := \sum_{n : 0 \to m} n^{\underline{-1}},\qquad \text{where }n^{\underline {-1}} := \frac1{n+1},  $$we call $H_m$ is called the $m$th harmonic number. We can get an extension of this sum using [[Fractional Adding]]. 

We can even get a similar result to integration by parts, called *summation by parts*: $$\sum_{n : a\to b} f(n) \Delta g(n) = f(b)g(b) - f(a)g(a) - \sum_{n : a\to b}g(n+1)\Delta f(n).$$
We also have an analogue for the backward difference: $$\sum_{n:a\leftarrow b} f(n) := \sum_{n = a+1}^b f(n).$$Thus we have the analogue of the fundamental theorem of calculus by $$\sum_{n: a\leftarrow b }\nabla f(n) = f(b) - f(a).$$With this theorem we have the following  identity for $m \ne -1$ $$\sum_{n : 0 \leftarrow x} n^\overline m = \frac1{m+1} x^{\overline{m+1}},$$and we have the a similar as the harmonic numbers $$H_{m-1} = \sum_{n: 1 \leftarrow m}n^{\overline{-1}},\qquad \text{where }n^{\overline {-1}} := \frac1{n-1}.$$We also have summation by parts for the backward difference $$\sum_{n : a\leftarrow b} f(n) \nabla g(n) = f(b)g(b) - f(a)g(a) - \sum_{n : a\leftarrow b}g(n-1)\nabla f(n).$$
Finally, we can consider the equivalent to [[Taylor Series in R]], called *Gregory-Newton interpolation formula*: $$f(x) = \sum_{k = 0}^\infty \frac{\Delta^kf(a)}{k!}{(x-a)^{\underline k}} = \sum_{k = 0}^\infty {x-a\choose k}\Delta^kf(a)$$which holds for any polynomial $f$ and for many (but not all) analytic functions. 