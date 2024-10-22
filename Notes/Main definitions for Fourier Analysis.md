---
tags:
  - "#FourierAnalysis"
---
Subjects: [[Fourier Analysis]]
We begin the study of Fourier Analysis

**Def:** Let $f$ be an integrable function on the interval $[a,b]$ of length $L$, then the *$n$th Fourier coefficient* of $f$ is defined as $$\hat f (n) = \frac{1}{L} \int_a^b f(x) e^{-2\pi i nx/L}\, dx \qquad n \in \Bbb Z$$
The *Fourier series* of $f$ is given formally (not caring about convergence) by $$\sum_{n =  -\infty}^\infty \hat f(n) e^{2\pi i nx/L}$$
We shall sometimes write $a_n$ for the Fourier coefficients of $f$, and use the notation $$f(x) \sim \sum_{n = \infty}^\infty a_n e^{2\pi inx/L}$$to indicate that the series on the right-hand side is the Fourier series of $f$. 

We can write the Fourier series of a function $f$, can be written as $$f (\theta) \sim \hat f(0) + \sum_{n \ge 1} [\hat f(n) +\hat f(-n)] \cos\left(\frac{2\pi n \theta}{L}\right) + i[\hat f(n)- \hat f(-n)]\sin\left(\frac{2\pi n\theta}{L}\right) $$
If $f$ is even then $\hat f(n) = \hat f(-n)$, and we get a cosine series
If $f$ is odd, then $\hat f(n) = -\hat f(-n)$, and we get a sine series
We also have that $f$ a periodic function, then $\overline{\hat f(n)} = \hat{\overline f}(-n)$, for all $n$. Then $f$ is real-valued iff $\overline{\hat f(n)} = f(-n)$ for all $n$. 

We can do some algebra, and we can calculate the coefficients directly for the sine and cosines, where it would be of this form $$f(\theta) \sim \hat f(0) + \sum_{n \ge 1} a_n \cos\left(\frac{2\pi n \theta}{L}\right)+b_n \sin\left(\frac{2\pi n \theta}{L}\right)$$, then we can get that $$a_n = \frac{2}{L} \int_a^b f(\theta) \cos\left(\frac{2\pi n \theta}{L}\right)\, d\theta\qquad \quad b_n = \frac{2}{L} \int_a^b f(\theta) \sin\left(\frac{2\pi n \theta}{L}\right)\, d\theta$$
and the factor of two happens because we are adding two coefficients

Fourier series are part of a larger family called the *trigonometric series* which by definition, are expressions of the form $\sum_{n = -\infty}^\infty x_n e^{2\pi i nx/L}$ where $c\in \Bbb C$. If a trigonometric series involves only finitely many nonzero terms, it is called a *trigonometric polynomial*; its *degree* is the larges value of $|n|$, for which $c_n \ne 0$. 

The $N$th partial sum of the Fourier series of $f$, for $N$ positive integer, is a particular example of a trigonometric polynomial, and it is given by $$S_N(f)(x) = \sum_{n = -N}^N \hat f(n) e^{2\pi i nx/L} $$
As a consequence, the convergence of Fourier series can be understood as the "limit" as $N\to \infty$  of the partial of these symmetric sums.

An interesting question is, what sense does $S_N(f)$ converge to $f$ as $N\to \infty$

**Def:** The trigonometric polynomial defined for $x\in [-\pi, \pi]$ by $$D_N(x) = \sum_{n = -N}^N e^{inx}$$is called the $N$th *Dirichlet kernel*. We can get a close formula as $$D_N(x) = \frac{\sin((N+ \frac{1}{2})x)}{\sin(x/2)}$$
**Def** The function $P_r(\theta)$, called the *Poisson kernel* is defined for $\theta \in [-\pi, \pi]$, and $0\le r <1$, by de absolutely and uniformly convergent series $$P_r(\theta) =\sum_{n =-\infty}^\infty r^{|n|}e^{in\theta} $$
We can also find a close form being $$P_r(\theta) = \frac{1-r^2}{1-2r\cos\theta+r^2}$$
## Uniqueness of Fourier Series
**Th:** Suppose that $f$ is an integrable function on the circle with $\hat f(n) = 0$ for all $n \in \Bbb Z$. Then $f(\theta_0) = 0$ whenever $f$ is continuous at the point $\theta_0$. 

**Cor:** If $f$ is continuous on the circle and $\hat f(n) =0$ for all $n \in \Bbb Z$, then $f = 0$

**Cor:** Suppose that $f$ is a continuous function on the circle and that the Fourier series of $f$ is absolutely convergence. Then the Fourier series converges uniformly to $f$, that is $$S_N(f) \rightrightarrows f$$
**Cor:** Suppose that $f$ is $\mathcal C^2$ on the circle. Then $$\hat f(n) = O(1/|n|^2)\qquad |n|\to \infty$$so that the Fourier series of $f$ converges absolutely and uniformly to $f$. 

We also got an important identity proving this corollary $$\widehat{f'}(n) = in \hat f(n) \qquad n \in \Bbb Z$$**Cor:** in general, If $f$ is a periodic function of period $2\pi$ which belongs ti the class $\mathcal C^k$. Then $$\hat f(n) = O(1/|n|^k)\qquad |n|\to \infty$$