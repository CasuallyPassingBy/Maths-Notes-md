---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Riemann Integral in R]]

## Equal Partitions

Let $\mathcal{P}_n$ be uniform partitions of $n$ elements. Evaluating the Reimann sums at left or right endpoints is an important construction. They receive a particular notation, where $h_n = \frac{b-a}{n}$:

$$ L_n(f)= h_n\sum_{k=0}^{n-1} f\left(a + kh_n\right)  
$$

$$ R_n(f)= h_n\sum_{k=1}^{n} f\left(a +k h_n\right) $$

If we don’t have a reason to prefer either one of them, it’s reasonable to take the mean we get:

$$ T_n(f) = \frac{L_n(f)+R_n(f)}{2}= h_n\left(\frac{f(a)}{2}+\sum_{k=1}^{n-1}f\left(a + kh_n\right) + \frac{f(b)}{2}\right) $$

In particular, if $f$ is monotonic then the integral will be trapped between the two, and we will get that the average will differ of the integral by a small amount:

$$ \left| \int_a^bf - T_n(f) \right| \leq \frac{b-a}{n}\left|\frac{f(b)-f(a)}{2} \right| $$

## Trapezoidal Rule

Continue to work with equal partitions, $\mathcal{P_n}$ and a width of $h_n = \frac{b-a}{n}$ . Let’s consider the function $g_n$ is a piecewise function, of a linear approximation of $f$ at the interval $[a +(k-1)h_n,a +kh_n ] = I_k$. In other words:

$$ \int_{I_k} g_n = \frac{1}{2}h_n\left[ f({a+(k-1)h_n}) + f({a+kh_n})\right] $$

Then the integral along all $[a, b ]$ will be equal to:

$$ \int_a^b g_n = \sum_{k = 1}^n\int_{I_k}g_n =\frac{1}{2}h_n \sum_{k=1}^n f(a+(k-1)h_n) + f(a+kh_n) = h_n\left( \frac{f(a)}{2}+\sum_{k=1}^n f(a+kh_n) + \frac{f(b)}{2}\right) = T_n(f) $$

$T_n(f)$ is the **n-th Trapezoidal Approximation.**

_**Theorem:**_ If $f \in \mathcal{C^2}[a,b]$, then there’s a $c\in[a,b]$:

$$ T_n(f) -\int_a^bf = \frac{(b-a)h_n^2}{12}f''(c) $$

_**Corollary:**_ If $f \in \mathcal{C^2}[a,b]$ and let $|f''| \leq B_2$, then:

$$ \left|\int_a^bf - T_n(f) \right| \leq \frac{(b-a)^3}{12n^2}B_2 $$

## Midpoint Rule

$$ M_n(f) = h_n\sum_{k = 1}^nf\left(a +\left(k-\frac{1}{2} \right)h_n\right) $$

_**Theorem:**_ if $f \in\mathcal{C^2[a,b]}$, then there’s a $c \in[a,b]$ that:

$$ \int_a^bf - M_n(f) = \frac{(b-a)h_n^2}{24}f''(c) $$

_**Corollary:**_ If $f \in \mathcal{C^2}[a,b]$ and let $|f''| \leq B_2$, then:

$$ \left|\int_a^bf - M_n(f) \right| \leq \frac{(b-a)^3}{24n^2}B_2 $$

How to transform knowledge of $T_n(f)$ and $M_n(f)$ into a type of $T_n(f)$:

$$ T_{2n}(f) = \frac{1}{2}M_n(f)+\frac{1}{2}T_n(f) $$

## Simpson’s Rule

Given a $n \in \mathbb{2N}$, the Simpson Sum is defined as follows:

$$ {S_n(f) = \frac{h_n}{3} \left(\sum_{k=1}^{n/2}f(a+(2k-2)h_n)+4f(a+(2k-1)h_n)+f(a+2kh_n)\right)} $$

_**Theorem:**_ If $f\in\mathcal{C^4}[a,b]$, there’s a $c\in[a,b]$ that:

$$ S_n(f) - \int_a^b f = \frac{(b-a)^5}{180n^4}f^{(4)}(c) $$

_**Corollary:**_ If $f\in\mathcal{C^4}[a,b]$, and $|f^{(4)}| \leq B_4$, then:

$$ \left|\int_a^bf - S_n(f) \right| \leq \frac{(b-a)^5}{180n^4}B_4 $$

How to transform knowledge of $T_n(f)$ and $M_n(f)$ into a type of $S_n(f)$:

$$ S_{2n}(f)= \frac{2}{3}M_n(f) + \frac{1}{3}T_n(f) $$