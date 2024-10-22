---
tags:
  - ComplexAnalysis
  - SpecialFunctions
---
Subjects: [[Complex Analysis]], [[Special Functions]]
Links: [[Gamma Function]], [[Dirichlet Series]], [[Prime Numbers]], [[Infinite Product of Functions]], [[Dirichlet Eta Function]]

We see that the zeta function was studied by Euler, and it gave us values for the positive even integers:
$$
	\zeta(2n) = (-1)^{n+1}\frac{(2\pi)^{2n}B_{2n}}{2(2n)!}
$$
where $B_{2n}$ represents the [[Bernoulli numbers]]. We see that $\zeta(3)$ is irrational, and it was proved by Apéry, which is why it is called the Apéry's constant.

Let $U = \{z \in \Bbb C \mid \Re(z) > 1\}$. We define the Riemann zeta function as $\zeta: U \to \Bbb C$, as 
$$
	\zeta(z) = \sum_{n = 1}^\infty \frac{1}{n^z}
$$
**Th:** $\zeta \in \mathcal H(U)$. with $U = \{z \in \Bbb C \mid \Re(z) > 1\}$. Meaning it is analytic on $U$.

If we play with the Gamma function, we get that 
$$
	\frac{1}{n^z}\Gamma(z) = \int_0^\infty u ^{z-1} e^{-nu}\, du
$$
If we sum over $n \in \Bbb N⁺$. We get
$$
	\zeta(z) \Gamma(z) = \sum_{n = 1}^\infty \int_0^\infty u^{z-1}e^{-nu}\, du
$$
We would like to exchange the series and the integral. To do that we need a couple of lemmas, and notation:

We define, the sets $B(a) = \{z \in \Bbb C \mid a \le \Re(z)\}$, and $C(a) = \{z \in \Bbb C \mid \Re(z) \le a\}$. 

**Lemma 1:** Let $a >1$. Then for any $\varepsilon>0$, there's a $\delta>0$, such that if $0 < \alpha < \beta <\delta$, then for every $z \in B(a)$, we have that
$$
	\left|\int_\alpha^\beta \frac{t^{z-1}}{e^t-1}\, dt\right|<\varepsilon
$$
**Lemma 2:** Let $M\in \Bbb R$. It satisfies that every $\varepsilon >0$, there's $N >0$ such that if $N < p < q$, then for every $z \in C(M)$, 
$$
	\left|\int_p^q \frac{t^{z-1}}{e^t-1}\, dt\right|<\varepsilon
$$

We get a couple of corollaries:
1. The following function is analytic when $\Re(z) >1$, $$h(z) = \int_0^1 \frac{t^{z-1}}{e^t-1}\, dt$$
2. The following function is entire $$g(z) = \int_1^\infty \frac{t^{z-1}}{e^t-1}\, dt$$
3. The following function is analytic when $\Re(z) >1$, $$f(z) = \int_0^\infty \frac{t^{z-1}}{e^t-1}\, dt$$
**Lemma 3:** For $a >0$, the series $\sum\limits_{n = 1}^\infty e^{-nt}$ converges uniformly on $[a, \infty)$, and $$\sum_{n = 1}^\infty e^{-nt} = \frac{1}{e^{t}-1}$$
**Th:** If $\Re(z) >1$ , then $$\zeta(z)\Gamma(z) = \int_0^\infty \frac{t^{z-1}}{e^{t}-1}\, dt$$ With this formula, we would like to extend the domain of the $\zeta$ function. 

Let $$f(z) = \frac{1}{e^{z}-1}$$ We see that $f \in \mathcal M(\Bbb C)$, and $P(f) = 2\pi i \Bbb Z$. If we calculate the residue of $f$ at $0$, we get that $$\lim_{z\to 0} zf(z) =\lim_{z\to 0} \frac{z}{e^{z}-1} = 1$$
Meaning $\text{Res}(f, 0) = 1$. We see that $$ g(z) = \frac{1}{e^{z}-1} - \frac{1}{z}$$
then $g \in \mathcal M(\Bbb C)$, and $0 \notin P(g)$.

**Prop:** The following function is analytic for $\Re(z) >0$, $$g(z) = \int_0^1\left[\frac{1}{e^{t}-1} - \frac{1}{t}\right] t^{z-1}\, dt $$

With this we can define an extension for the $\zeta$ function. 

**Def (First Extension):** Let $\Re(z) > 0$ and $z\ne 1$
$$\zeta(z) = \frac{1}{\Gamma(z)}\left[\frac{1}{z-1} + \int_0^1\left[\frac{1}{e^{t}-1}-\frac{1}{t}\right]t^{z-1}\, dt  +\int_1^\infty \frac{t^{z-1}}{e^{t}-1}\, dt\right]$$

If $U = \{z \in \Bbb C \mid \Re(z) >0\}$, then  $\zeta \in \mathcal M(U)$, and $P(\zeta) = \{1\}$, with $\text{Res}(\zeta, 1) = 1$. 

**Prop:** Si $U =\{z \in \Bbb C \mid \Re(z) > 0\}$ , then $\zeta \in \mathcal M(U)$, $P(\zeta) =\{1\}$, and $\text{Res}(\zeta, 1) = 1$. 

**Prop:** If $$g(z) = \int_0^1 
\left[\frac{1}{e^{t}-1}- \frac{1}{t} +\frac{1}{2}\right]t^{z-1}\, dt$$$g$ is analytic on $\Re(z) > -1$. 
**Prop:** $$h(z) = \int_1^\infty \left[\frac{1}{e^{t}-1}- \frac{1}{t}\right]t^{z-1}\, dt$$is analytic on $\Re(z) < 1$

**Def (Extension 2):** For $-1<\Re(z) <1$, we get that $$\zeta(z) = \frac{1}{\Gamma(z)}\left[\frac{-1}{2z}+\int_0^1 \left(\frac{1}{e^{t}-1}-\frac{1}{t}+\frac{1}{2}\right)t^{z-1}\, dt+ \int_1^\infty \left(\frac{1}{e^{t}-1}- \frac{1}{t}\right)\, t^{z-1}\,dt\right]$$
Then $z=0$ is a removable singularity for $\zeta$ and $\zeta(0) = -1/2$. 

**Th:** $\zeta\in \mathcal M(U)$, $U \in \{z \in \Bbb C \mid \Re(z)> -1\}$, and $P(\zeta) =\{1\}$. 

**Lemma:** If $0 < a <1$, then $$\int_{-\infty}^\infty \frac{e^{ax}}{1+e^x}\, dx = \frac{\pi}{\sin(\pi a)}$$
The way we calculate this integral is by using the [[Residue Theorem]], and the clockwise contour of a rectangle with vertices $R, R + 2\pi i, - R + 2\pi i, -R$.

**Cor:** If $0<a<1$, then $$\int_0^\infty \frac{x^{-a}}{1+x}\, dx = \frac{\pi}{\sin(\pi a)}$$
We get that $$\frac{i}{2}\cot\left(\frac{it}{2}\right) = \frac{e^t+1}{2(e^t -1)} = \frac{1}{t}+\sum_{n = 1}^\infty \frac{2t}{t²+4\pi^2 n^2}$$
and $$\frac{1}{e^t-1}+ \frac{1}{2} = \frac{e^t +1}{2(e^t-1)}$$
lastly, if $\Re(z) <0$, then $$\int_1^\infty t^{z-1}\, dt = \frac{-1}{z}$$
With this in hand we can see that for $-1< \Re(z) <0$, we have $$\Gamma(z) \zeta(z) = \int_0^\infty \sum_{n = 1}^\infty \frac{2t^z}{t^2+4\pi^2n^2}\, dt$$
We would like to exchange the series, with the integral but we need to do this carefully. We will prove the equality for $0<x <1$. 

Let $$I = \int_0^\infty \frac{2t^x}{t^2+4\pi^2n^2}\, dt$$
Then we consider the substitution $t = 2\pi n u$, getting the integral $$I = \int_0^\infty \frac{2 (2\pi n)^{x+1} u^x}{4\pi^2n^2 u^2 +4\pi^2n^2}\, du = (2\pi n)^{x-1}\int_0^\infty \frac{2u^x}{u^2+1}\, du$$
Lastly we make the last substitution $v = u^2$, getting that $$I = (2\pi n)^{x-1}\int_0^\infty \frac{v^{(x-1)/2}}{v+1}\, dv$$Which we can calculate using our corollary: $$I = \frac{(2\pi n)^{x-1}\pi}{\cos\left(\frac{\pi}{2} x\right)}$$
Meaning that $$\Gamma(z) \zeta(x) = \sum_{n = 1}^\infty \frac{(2\pi n)^{x-1}\pi}{\cos\left(\frac{\pi}{2} x\right)} = \frac{\pi}{\cos\left(\frac{\pi}{2}x\right)} (2\pi)^{x-1} \sum_{n = 1}^\infty \frac1{n^{1-x}} = \frac{\pi}{\cos\left(\frac{\pi}{2}x\right)} (2\pi)^{x-1} \zeta(1-x)$$
Using Euler's reflection formula, we get the following equation $$\zeta(x) = 2(2\pi)^{x-1}\zeta(1-x)\Gamma(1-x)\sin\left(\frac{\pi}{2}x\right)$$
**Th (Riemann Functional Equation):** For $-1 < \Re(z) < 1$, then $$\zeta(z) = 2(2\pi)^{z-1}\zeta(1-z)\Gamma(1-z)\sin\left(\frac{\pi}{2}z\right)$$
**Def (Third Extension):** For $z <0$, then we define $$\zeta(z) = 2(2\pi)^{z-1}\zeta(1-z)\Gamma(1-z)\sin\left(\frac{\pi}{2}z\right)$$
We also a kind of nice observation that for $n \in \Bbb N^+$, then $$\zeta(-2n) = 0$$Giving us the so called *trivial zeros* of the Riemann zeta function. 

We still have a small kink to check that we could actually interchange the series and the integral. It is a step that we kind of omitted, using [[Interchange of Limits#Some Interchange properties|some interchange properties]], then we can prove that 

**Th:** For $-1< \Re(z) < 0$, $$\zeta(z) = 2(2\pi)^{z-1}\zeta(1-z)\Gamma(1-z)\sin\left(\frac{\pi}{2}z\right)$$
for $-1<x<0$, then 
$$\Gamma(x)\zeta(x) = \int_0^\infty \sum_{n = 1}^\infty \frac{2t^x}{t^2+4\pi^2n^2}\, dt = \sum_{n = 1}^\infty \int_0^\infty \frac{2t^x}{t^2+4\pi^2n^2}\, dt$$
This actually gives us the the most verifies that the third expansion matches with the other one. 

**Cor:** $\zeta \in \mathcal (\Bbb C)$ and $P(\zeta) = \{1\}$.

Let $\{p_n\}_{n \in \Bbb N}$ be the increasing sequence of prime numbers. 

Then we can consider $f_n(z) = 1-p_n^{-z}$, we see that $f_n$ are entire functions. Let $U = \{z \in \Bbb C\mid \Re (z) >1\}$. Then we can check that $$\prod_{n = 1}^\infty f_n \in \mathcal H(U)$$
Similarly, we can check that $f_n(z) = 0$, then this implies that $\Re(z)=0$, meaning that $z \notin U$. Thus $1/f_n \in \mathcal H(U)$, and we get that $$\prod_{n = 1}^\infty \frac1{f_n} \in \mathcal H(U)$$.
### Euler's Theorem

If $Re(z) >1$, then $$\zeta(z) = \sum_{n = 1}^\infty \frac1{n^z} = \prod_{n = 0}^\infty \frac1{1-p_n^{-z}}$$
**Cor:** If $\Re(z) > 1$, then $\zeta(z) \ne 0$

**Cor:** If $\Re(z) < 0$ and $\zeta(z) = 0$, then $z = -2n$ for $n \in \Bbb N^+$

**Cor:** If $\zeta(z) = 0$ and $z\ne -2n$ for all $n \in \Bbb N$, then $0 \le \Re(z) \le 1$

**Th:** For all $z\in \Bbb C\setminus\{1\}$, we have that $$\zeta(z) = 2(2\pi)^{z-1}\zeta(1-z)\Gamma(1-z)\sin\left(\frac{\pi}{2}z\right)$$
We see that the zeros of $\zeta$ is symmetric with respect to the line $\Re(z) = 1/2$, when $0\le \Re(z) \le 1$. 

We also see that $\zeta[\Bbb R\setminus \{1\}]\subseteq \Bbb R$, then by [[Basic Analytic Extension#Schwarz Reflection Principle|Schwarz Reflection Principle]], we have that $$\overline{\zeta({\overline z})} = \zeta(z)$$
Meaning that if $z\in Z(\zeta)$, the n $\overline z \in Z(\zeta)$.

We see that $$\log \zeta (s) = \sum_p \frac1{p^s} + O(1)$$for $\Re(s) >1$

We see that $$\zeta(s) = \frac1{s-1} +O(1) \qquad \text{as } s\to 1^+$$and $$\sum_p \frac1{p^s} = \log\left(\frac1{s-1}\right) + O(1) \text{as } s\to 1^+$$giving us the result that $$\sum_p \frac1p = \infty$$giving us a cute proof that there are infinitely many primes, but also that are not that sparse as they increase

We look at the innocent observation that for all $\theta\in \Bbb R$, then $$4\cos\theta+\cos(2\theta) = 2(1+\cos\theta)^2$$
For $z = a+bi$ and $a>0$, then $$\ln|\zeta(z)| = \ln \left|\prod_p \frac1{1-p^{-z}}\right| = - \sum_p \ln|1-p^{-z}| = -\sum_p \Re(\log(1-p^{-z})$$
With this form we can get that $$\ln|\zeta(z)| = - \sum_p \sum_{n = 1}^\infty  \Re\left(\frac{p^{-nz}}{n}\right) = -\sum_p \sum_{n = 1}^\infty \frac{\cos(b\ln(p^n))}{np^{na}} $$

**Prop:** If $z= a+bi$, and $a>1$, then  $$|\zeta(a)\zeta^4(a+bi)\zeta^3(a+2bi)| \ge 1$$
**Th:** If $\Re(z) = 1$ and $z\ne 1$, then $$\zeta(z) \ne 0$$
This a big result, so we now know that by symmetry of the zeros, then if $\Re(z) = 0$, then $\zeta(z) \ne 0$.

**Def:** The set $$B= \{z \in \Bbb C \mid 0 < \Re(z) < 1\}$$is called the *critical band*, the line $\Re(z) = 1/2$ is the *critical line*

# Riemann Hypothesis
If $z \in Z(\zeta) \cap B$, then $$\Re(z) = \frac1{2}$$