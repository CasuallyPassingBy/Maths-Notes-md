---
tags:
  - OrdinaryDifferentialEquations
  - "#SpecialFunctions"
---
Subjects: [[Ordinary Differential Equations]], [[Special Functions]]
Links: [[Frobenius Method]], [[Bessel Functions]]

The Bessel Functions are defined to be the solutions to the second order linear differential equation, with $\Re(\alpha) \ge 0$:

$$ x^2 y'' + xy' +(x^2-\alpha^2) y = 0 $$

We have that $x = 0$ is a regular singular point of the Bessel equation. The indicial polynomial $I$ is given by
$$ I(r) = r^2 - \alpha^2 $$
## $\alpha = 0$
The first case, is when $\alpha = 0$. Since we have repeated roots we have there are two linearly solutions $\phi_1$, $\phi_2$ of the form

$$ \phi_1(x) = \sigma_1(x) \qquad \phi_2(x) = x\sigma_2(x)+ (\ln x)\phi_1(x) $$

If we let
$$ \sigma_1(x) = \sum_{k = 0}^\infty c_k x^k $$

and we plug it on the differential equation we can get the expression:

$$ L[\sigma_1](x) =c_1 x + \sum_{k = 2}^\infty [(k(k-1) +k)c_k + c_{k-2}]x^k = 0 $$

then we get

$$ c_1 = 0 $$

and the recurrence relation

$$ [k(k-1) + k]c_k + c_{k-2}= 0 \qquad k =0, 1, \dots $$

Then simplifying it we get that

$$ c_{2k} = \frac{(-1)^k}{(2k!!)^2} \qquad c_{2k+1} = 0 \qquad k =0,1,2, \dots $$

we get that the solution is called

$$ \phi_1(x)=J_0(x) = \sum_{k = 0}^\infty \frac{(-1)^kx^{2k}}{(2k!!)^2} = \sum_{k =0}^\infty \frac{(-1)^k}{(k!)^2}\left(\frac{x}{2}\right)^{2k} $$

We define $\phi_2(x)$ as

$$ \phi_2(x) = \sum_{k = 1}^\infty c_k x^k + J_0(x) \ln x $$

Then we calculate for $L [\phi_2]$, then we get it simplifies as

$$ c_1 x + 2^2 c_2x^2 + \sum_{k = 3}^\infty [k^2 c_k + c_{k-2}]x^k = -2 x J_0'(x) $$

We can calculate that

$$ c_1 = 0, \qquad c_2 = \frac{1}{2^2} $$

finally we get the recurrence relations

$$ k^2 c_k + c_{k-2} = (-2xJ_0'(x))_k $$

and get that

$$ c_{2k+1} = 0 $$

and the recurrence relation for the evens terms looking like this:

$$ (2k)^2 c_{2k} + c_{2k-2} = \frac{(-1)^{k+1}k }{2^{2k-2}(m!)^2} $$

This simplifies to

$$ c_{2k}= \frac{(-1)^{k+1}H_k}{(2k!!)^2} $$

where $H_k$ represents the $k$th harmonic number. Getting

$$ \phi_2 (x) = \sum_{k = 1}^\infty \frac{(-1)^{k+1}H_k}{(2k!!^2)}x^{2k} + J_0(x) \ln x $$

We define the _********Bessel function of the second kind********_, then

$$ Y_0(x) = \frac{2}{\pi}\left([\ln\left( \frac{x}{2}\right)+\gamma]J_0(x) + \sum_{k=1}^\infty (-1)^{k+1}H_k\frac{\left(\frac{z^2}{4}\right)^k}{(k!)^2}\right) $$


We can show that $J_0(x)$ has infinitely many zeros. This zeros are enumerable.
## $\alpha \ne 0$
Then we solve the for the general Bessel function, from the differential equation
$$ L[y] =x^2 y'' +xy' + (x^2-\alpha^2) y =0 $$

We get that the indicial polynomial is

$$ I(r) = r^2 -\alpha ^2 $$

We know that one of the solutions will be of the form

$$ \phi_1 (x) = x^\alpha \sum_{k = 0}^\infty c_k x^k $$

Calculating $L[\phi_1]$ we get that

$$ [(\alpha+1)^2 + \alpha]c_1 x +\sum_{k = 2}^\infty ([(\alpha + k)^2 - \alpha^2]c_k + c_{k-2})x^k = 0 $$

We get that

$$ c_1 = 0, \qquad [(\alpha + k)^2 - \alpha^2]c_k + c_{k-2} = 0 $$

We get that

$$ c_{2k+1} =0,\qquad k \in \Bbb N $$

and

$$ c_{2k} = \frac{(-1)^k c_0}{2^{2k }k ! (\alpha +1)^{\overline k} } $$

We can choose the value of $c_0$, that is most convenient, then

$$ c_0 = \frac{1}{2^{\alpha}\Gamma(\alpha +1)} $$

$\Gamma(z)$ is the [[Gamma Function]]. We can finally define, the *******Bessel function of order $\alpha$ of the first kind:

$$ J_{\alpha}(x) = \sum_{k = 0}^\infty \frac{(-1)^k}{k!\Gamma(k + \alpha +1)}\left(\frac{x}{2}\right)^{2k +\alpha} $$
If $\alpha$ is not a positive integer the, we get that
$$ J_{-\alpha}(x) = \sum_{k = 0}^\infty \frac{(-1)^k}{k!\Gamma(k - \alpha +1)}\left(\frac{x}{2}\right)^{2k -\alpha} $$

Then $J_\alpha$ and $J_{-\alpha}$ form a basis for the solutions to the Bessel equation of order $\alpha$ for $x>0$. For the case where $\alpha =n \in \Bbb N^+$, we must do the other case where the other solution is of the form

$$ \phi_2(x) = x^{-n} \sum_{k = 0}^\infty c_k x^k + c(\ln x)J_n(x) $$

Ngl, finding a solution for $c_k$ and $c$ seems like a lot, the procudure is on Coddignton, An Introduction to ODEs, page 175 (186 on the pdf). We still have a pressing issue since we have that

$$ J_{-n}(x) = (-1)^n J_n(x) $$

making them linearly dependent. And the Bessel function $J$ are entire functions in $x$.

For the other solution we usually use the *******Bessel function of order $\alpha$ of the second kind. We define it as

$$ Y_\alpha (x) = \frac{J_{\alpha}(x) \cos(\alpha \pi)- J_{-\alpha}(x)}{\sin(\alpha\pi)} $$

Which for $\alpha \not \in \Bbb N$, we get that is just a linear combination of $J_\alpha$ and $J_{-\alpha}$. In the case where $\alpha\in \Bbb N$, we get that we must take the limit, then

$$ Y_n(x)=\lim_{\alpha\to n} Y_n(x) $$

We get that for an $n$ ,$Y_n$ is of the form
$$ Y_n(z) =-\frac{\left(\frac{z}{2}\right)^{-n}}{\pi}\sum_{k=0}^{n-1} \frac{(n-k-1)!}{k!}\left(\frac{z^2}{4}\right)^k +\frac{2}{\pi} J_n(z) \ln \frac{z}{2} -\frac{\left(\frac{z}{2}\right)^n}{\pi}\sum_{k=0}^\infty (\psi(k+1)+\psi(n+k+1)) \frac{\left(-\frac{z^2}{4}\right)^k}{k!(n+k)!} $$

We also get a similar relation for the Bessel function of the second kind
$$ Y_{-n}(x) =(-1)^n Y_n(x) $$
Where $\psi$ is the [[Digamma function]] and $\gamma$ is the [[Euler–Mascheroni Constant]]. Using this definition we get why

$$ Y_0(x) = \frac{2}{\pi}\left([\ln\left( \frac{x}{2}\right)+\gamma]J_0(x) + \sum_{k=1}^\infty (-1)^{k+1}H_k\frac{\left(\frac{z^2}{4}\right)^k}{(k!)^2}\right) $$