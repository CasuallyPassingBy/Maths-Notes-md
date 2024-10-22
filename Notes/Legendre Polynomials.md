---
tags:
  - SpecialPolynomials
  - SpecialFunctions
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]], [[Special Functions]], [[Special Polynomials]]
## Via Differential Equation

A way to retrieve the Legendre polynomials is by solving the [[Important Differential Equations|Legendre Differential Equation]]:

$$ L[y] = (1-x^2) y'' -2xy' +\alpha(\alpha +1) y =0 $$

If we try to do with a [[Series Solutions of Linear Equations around Ordinary Points|series solution]] we get that

$$ y = \sum_{k \in \Bbb N} c_k x^k $$

we get that following recurrence relation

$$ (k+2)(k+1)c_{k+2} + (\alpha+k+1)(\alpha-k) c_k =0 $$

We get two cases, for even and odds respectively, then

$$ c_{2m} = (-1)^m \frac{(\alpha+1)_{m,2}(\alpha)_{m,-2}}{(2m)!} c_0 $$$$ c_{2m+1} = (-1)^m \frac{(\alpha+2)_{m,2}(\alpha-1)_{m,-2}}{(2m+1)!} c_1 $$

using the [[Falling and Rising Factorials and Pochhamer Symbols#Pochhammer $k$-symbol|Pochhamer k-symbol]].

We can split the general solution $y = c_0 \phi_0 + c_1 \phi_1$, where $\phi_0(0)= 1$, and $\phi_0'(0)=0$; $\phi_1(0)= 0$, and $\phi_1'(0)=1$. Then

$$ \phi_0(x) = 1+\sum_{m = 1}^\infty (-1)^m \frac{(\alpha+1)_{m,2}(\alpha)_{m,-2}}{(2m)!} x^{2m} $$$$ \phi_1(x)= x+\sum_{k =1}^\infty (-1)^m \frac{(\alpha+2)_{m,2}(\alpha-1)_{m,-2}}{(2m+1)!} x^{2m+1} $$

This are in general called Legendre Functions
From these we can see the the Legendre functions can be expressed using the [[Hypergeometric Function|hypergeometric function]]

$$ \phi_0(x) = {}_2F_1\left(-\frac{1}{2}, \frac{1}{2}(\alpha+1); \frac{1}{2}; x^2\right) $$$$ \phi_1(x) = x \left({}_2F_1\left(\frac{1}{2}(\alpha+2), \frac{1}{2}(1-\alpha);\frac{3}{2}; x^2\right)\right) $$

If we let $\alpha \in \Bbb N$, either $\phi_0$ or $\phi_1$ must be a polynomial while $(\alpha)_{m, -2}$ or $(\alpha-1)_{m,-2}$ must be eventually be zero. This polynomial that solve this differential equation, when $\alpha \in \Bbb N$, and with $P_\alpha(1) = 1$, is called the Legendre Polynomial. Then, we will denote it as $P_n$. Meaning that

$$ (1-x^2)P_n'' -2xP'_n +n(n+1)P_n = 0 $$

We can use some of Sturm-Louville Theory we can formulate the same differential equation as, an eigenvalue problem

$$ \frac{d}{dx}\left((1-x^2)\frac{d}{dx}\right)P(x) = \lambda P(x) $$

If we demand that the solution to be regular at $x = \pm 1$, then it is Hermitian. The eigenvalues found are of the form $n (n+1)$ for $n \in \Bbb N$, and the eigenfunctions are the $P_n$. he orthogonality and completeness of this set of solutions follows at once from the larger framework of Sturm–Liouville theory.

With induction we can check that each $x^n$ can be expressed as a linear combination of Legendre Polynomials. Meaning they form a base in the space of polynomials.

Additionally, we can check that

$$ \int_{-1}^1 P_n(x) P_m(x)\, dx = \frac{2}{2n+1}\delta_{n,m} $$

with $\delta_{n,m}$ being the Kronecker delta, meaning they are orthogonal in $L^2[-1,1]$.

Additionally, we can get that if $P$ is a $n$th degree polynomial, then

$$ P= \sum_{k = 0}^n c_k P_k $$

where
$$ c_k = \frac{2k+1}{2} \int_{-1}^1P(x)P_k(x) \, dx $$
## Rodrige’s Formula and other explicit formulas
We have an explicit, and especially compact expression of the Legendre Polynomials

$$ P_n(x) = \frac{1}{2^n n!}\frac{d^n}{dx^n}(x^2-1)^n $$

This enables us to have multiple other formulas
$$ \begin{align*}
P_n(x) & = [t^n] \frac{((t+x)^2-1)^n}{2^n} = [t^n] \frac{(t+x+1)^n(t+x-1)^n}{2^n}\\
P_n(x)&= \frac{1}{2^n} \sum_{k=0}^n \binom{n}{k}^2 (x-1)^{n-k}(x+1)^k\\
P_n(x)&=\sum_{k=0}^n \binom{n}{k} \binom{n+k}{k} \left( \frac{x-1}{2} \right)^k\\
P_n(x)&=\frac1{2^n}\sum_{k=0}^{\left\lfloor\frac n2\right\rfloor}(-1)^k\binom nk\binom{2n-2k}n x^{n-2k}\\
P_n(x)&= 2^n \sum_{k=0}^n x^k \binom{n}{k} \binom{\frac{n+k-1}{2}}{n}
\end{align*}$$

If we add this restriction of $P_n (1)=1$, then we get that the leading coefficients is ${a_n =\dfrac{(2n)!}{2^n(k!)^2}}$, we can calculate the other coefficients of the polynomial using the recurrence relation backwards, then we get

$$ a_{n-2m} =(-1)^m\frac{(2n-2m)!}{(m!)(2^n)(n-m)!(n-2m)!} \quad \text{for }0 \le m \le \left\lfloor\frac{n}{2}\right\rfloor $$

Meaning we can calculate an explicit formula for the Legendre Polynomial

$$ P_n(x) = \sum_{m= 0}^{\lfloor n/2\rfloor} (-1)^m\frac{(2n-2m)!}{(m!)(2^n)(n-m)!(n-2m)!} x^{n-2m} $$

which is equivalent to one above, but I derived it so it’s special.
## Generating Function

The generating function of the Legendre Polynomials can also be defined as the coefficients in a formal expansion in powers of $t$ of the generating function t

$$ \frac{1}{\sqrt{1-2xt+t^2}} = \sum_{n =0}^\infty P_n(x)t^n $$

It is usually kinda cumbersome using it, but we get that

$$ P_0(x) =1 \qquad P_1(x)=x $$

we can differnatiang we get that

$$ \frac{x-t}{\sqrt{1-2xt+t^2}}=(1-2xt+t^2)\sum_{n = 1}^\infty nP_n(x) t^{n-1} $$

from this we get the recurrence relation

$$ (n+1)P_{n+1}(x) = (2n+1)xP_n(x) -nP_{n-1}(x) $$

with seeds being $P_0$ and $P_1$.