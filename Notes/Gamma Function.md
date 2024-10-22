---
tags:
  - SpecialFunctions
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]], [[Special Functions]]
Links:[[Related Functions to the Gamma Function]], [[Poles of Analytic Functions]], [[Infinite Product of Functions]]

What we want $f: U \to \Bbb C$ such that
1. $U$ is the biggest region possible
2. $f\in \mathcal H(U)$
3. $f(1) =1$ and $zf(z) = f(z+1)$

We see that $0\not \in U$ since $1 = f(1) = 0 \cdot f(0) = 0$, which brings problems. Similarly we need that $P(f) = \Bbb Z^{\le 0}$, and we get $$f(z+n+1) = f(z)\prod_{k = 1}^n (z+k)$$and we get that the residues at each nonnegative integers is of the form $$ \text{Res}(f, -n) = \frac{(-1)^n}{n!}$$ with $n\in \Bbb N$. Let suppose $Z(f) = \varnothing$, and $f\in \mathcal M(\Bbb C)$, with $P(f) = \Bbb Z^{\le 0}$, with $U = \Bbb C \setminus \Bbb Z^{\le 0}$. Then there's $h\in \mathcal H(U)$ such that $f =1/h$. Then $Z(h) = P(f)$. Using [[Infinite Product of Functions|Weierstrass Factorization Theorem]], and consider that
$$
\sum_{n = 1}^\infty \frac{1}{(-n)²}<\infty 
$$
Then we can there's $g\in \mathcal H(U)$ such that:$$h(z) = z e^{g(z)} \prod_{n = 1}^\infty E_1(-z/n)=  z e^{g(z)} \prod_{n = 1}^\infty\left(\frac{z+n}{n}\right)e^{-z/n}$$
Exploiting the recurrence relation to with the $h$, we can find out who is $g$, the problem is that there are many, but the $g$ must satisfy$$\gamma = g(z+1)-g(z)$$with $\gamma$ being the [[Euler–Mascheroni Constant]], and the 'simplest' is $g(z) = \gamma z$. 

**Def:** Let $h \in \mathcal H(\Bbb C)$ as $$ h(z) =  z e^{\gamma z} \prod_{n = 1}^\infty\left(\frac{z+n}{n}\right)e^{-z/n} $$
and we define $\Gamma: \Bbb C \setminus \Bbb Z^{\le 0}\to \Bbb C$ as$$\Gamma(z) = \frac{1}{h(z)} =\frac{e^{\gamma z}}{z}\prod_{n = 1}^\infty  \left(\frac{n}{z+n}\right)e^{z/n}$$
This is known as the **Weierstrass product Formula of the Gamma Function**

**Th:** $\Gamma \in \mathcal M(\Bbb C)$ and $P(\Gamma) = \Bbb Z^{\le 0}$ and satisfies this conditions:
- for all $n \in \Bbb N$, we get that $\text{Res}(\Gamma, -n) = (-1)^n/n!$ 
- for every $z\in \Bbb C\setminus \Bbb Z^{\le 0}$, $\Gamma(z+1) = z\Gamma(z)$ and $\Gamma(1) =0$. 
- $\Gamma(n+1) = n!$ for every $n \in \Bbb N$ 
#### Euler’s Reflection Formula
for $z\not \in \Bbb Z$, then$$ \Gamma(1-z)\Gamma(z) = \frac{\pi}{\sin(\pi z)} $$
#### Gauss Product Formula
Gauss rewrote it as **Gauss’s product formula**:$$ \Gamma(z)= \lim_{n \to \infty}\frac{n^z n!}{z(z+1) \cdots (z+n)}= \lim_{n \to \infty}\frac{n^z n!}{z^{\overline{ n+1}}} $$
### Bohr-Mollerup Theorem
There’s a unique positive function $f$ defined on $x \ge 0$ satisfying
- $f(1)=1$
- $f(x+1)= xf(x)$
- $\ln(f(x))$ is convex

Now we want to check that the usual definition of the gamma function actually matches with the definition by Legendre as the integral:
$$ \Gamma(s) = \int_0^\infty t^{s-1} e^{-t} \,d t $$
but we need a little constraints to make the integral converge, having that $\Re(z)>0$, then have that $$ \Gamma(z) = \int_0^\infty t^{z-1} e^{-t} \,d t $$
To actually do this, it is done by a couple of tricks, and a lot of steps:

Some notation, given $0<a<M$ we define$$S(a, M) =\{z\in \Bbb C\mid a \le \Re(z) \le M\} $$
**Lemma 1:** Let $0<a <M$, then 
- for every $\varepsilon>0$, there's a $\delta>0$ such that every $z\in S(a, M)$ if  $0<\alpha <\beta <\delta$, then $$ \left|\int_\alpha^\beta t^{z-1} e^{-t}\, dt \right|<\varepsilon$$
- for every $\varepsilon>0$, there's a $N>0$ such that every $z\in S(a, M)$ if $N < p< q$, then $$\left|\int_p^q t^{z-1}e^{-t}\, dt \right| < \varepsilon$$
**Lemma 2:** Let $U = \{z \in \Bbb C \mid \Re (z) >0\}$. For each $n \in \Bbb N$, let $f_n:U \to \Bbb C$ as $$f_n(z) = \int_{1/n}^n t^{z-1}e^{-t}\, dt $$Then, $f_n$ converges to $$f(z) = \int_0^\infty t^{z-1} e^{-t} \,d t$$
in $\mathcal H(U)$. 

**Lemma 3:** Let $h_n (z) = \left(1-\dfrac{z}{n}\right)^n$, with $h_n \in \mathcal H(\Bbb C)$
- $h_n \to e^{-z}$ in $\mathcal H(U)$ 
- if $t\ge 0$, and $n > t$, then $\left(1-\dfrac{z}{n}\right)^n \le e^{-t}$ 

**Lemma 4:** For $x>0$, and $n \in \Bbb N$, we get that 
$$\int_0^n \left(1-\frac{t}{n}\right)^n t^{x-1}\, dt = \frac{n! n^x}{x(x+1)\cdots (x+n)}$$
**Cor of Lemma 4:** For $x >0$, and $$g_n(x) = \int_0^n \left(1-\frac{t}{n}\right)^n t^{x-1}\, dt$$ Then $$\lim\limits_{n \to \infty }g(x) = \Gamma (x) $$
**Th:**  Let $U = \{z \in \Bbb C \mid \Re (z) >0\}$ Then for $z\in U$ we have that $$ \Gamma(z) = \int_0^\infty t^{z-1} e^{-t} \,d t $$
### Miscellaneous 
We can also have new forms of the gamma function

$$ \begin{align*} \Gamma(s) &= a^s \int_0^\infty y^{s-1} e^{-ay} \, dy\\ &= 2 \int_0^\infty y^{2s-1}e^{-y^2}\, dy \\ &= (m+1)^s\int_0^1y^m (-\ln y)^{s-1}\, dy \end{align*} $$

We also have that another definition namely, the **Euler’s product formula:****$$ \Gamma(z) = \frac{1}{z} \prod_{n = 1}^\infty \left[\frac{1}{1+\frac{z}{n}}\left(1+\frac{1}{n}\right)^z\right] $$

### Legendre’s Duplication Formula
Let $z \in \Bbb C$, then

$$ \Gamma(z)\Gamma\left(z +\frac{1}{2}\right) = 2^{1-2z}\sqrt{\pi}\, \Gamma(2z) $$

### Particular Values
for nonnegative integers $n$, we have that

$$ \Gamma\left(\frac{1}{2}+n\right)= \frac{(2n-1)!!}{2^n}\sqrt\pi$$$$ \Gamma\left(\frac{1}{2}-n\right)= \frac{(-2)^n}{(2n-1)!!}\sqrt\pi\\ $$

### Raabe’s Identity

$$ \int_{t}^{t+1} \ln(\Gamma(t)) \, dt = \frac{\ln(2\pi)}{2}+t\ln t-t $$

