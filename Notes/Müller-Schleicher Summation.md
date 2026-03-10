---
tags:
  - "#Miscellaneous"
---
Subjects: [[Umbral calculus]]
Links: [[Discrete Calculus]], [[Series in R]], [[Infinite Products]], [[Digamma function|Harmonic Numbers]]

We define some axioms we would like for any kind of summation to have:
- Continued summation: $$\sum_{\nu = x}^y f(\nu) + \sum_{\nu = y+1}^z f(\nu) = \sum_{\nu = x}^z f(\nu).$$
- Translation Invariance: $$\sum_{\nu = x+s}^{y+s} f(\nu) = \sum_{\nu = x}^y f(\nu +s).$$
- Linearity: for arbitrary constants $\lambda, \mu \in \mathbb C$, $$\sum_{\nu = x}^y (\lambda f(\nu) + \mu g(\nu)) = \lambda \sum_{\nu = x}^y f(\nu) + \mu\sum_{\nu = x}^y g(\nu). $$
- Consistency with Classical Definition: $$\sum_{\nu = 1}^1 f(\nu) = f(1).$$
- Monomials: for every $d\in \mathbb N$, the mapping, $$z \mapsto \sum_{\nu = 1}^z \nu^d$$is entire.

**Prop:** For any polynomial $p: \Bbb C \to \Bbb C$, let $P: \Bbb C \to \Bbb C$ be the unique polynomial with $P(0) = 0$ and $P(z)- P(z-1) = p(z)$ for all $z\in \Bbb C$. Then:
- The possible definition $$\sum_{\nu = x}^y p(\nu) := P(y+1) - P(x),$$satisfies all axioms above.
- Conversely, every summation theory that satisfies the first four axioms and also satisfies the above equation for every polynomial $p$ and $x, y\in\Bbb C$ with rational difference $y-x \in \Bbb Q$.
- Every summation theory that satisfies all of the axioms also satisfies the equation aove for every polynomial $p$ and all $x, y\in  \Bbb C$.

**Def:** Let $U\subseteq \Bbb C$ and $\sigma\in \omega\cup\{-\infty\}$. A function $f: U \to \Bbb C$ will be called a right approximate polynomial of degree $\sigma$ if the following conditions are satisfied:
- if $x\in U$ then $x+1\in U$.
- there exists a sequence of polynomials $(p_n)_{n <\omega}$ of fixed degree $\sigma$ such that for all $x\in U$, $$\lim_{n \to \infty} |f(n+x)-p_n(n+x)| = 0.$$
**Def:** An right approximate polynomial $f: U \to \Bbb C$ of degree $\sigma\in \omega\cup\{-\infty\}$ will be called *right summable* if for every $a, b+1\in U$, the limit $$\lim_{n \to\infty} \left(\sum_{\nu= n+a}^{n+b} p_n(\nu) + \sum_{\nu = 1}^{n} f(\nu+a-1)-f(\nu+b))\right)$$exists. In this case, this limit will be the definition of the *fractional sum of $f$ from $a$ to $b$; we will denote it by*:$$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = a}^b f(\nu) := \lim_{n \to\infty} \left(\sum_{\nu= n+a}^{n+b} p_n(\nu) + \sum_{\nu = 1}^{n} f(\nu+a-1)-f(\nu+b))\right).$$Moreover, we can define *right fractional products by* $$\mathop{\to\!\!\!\!\!\!\!\prod}\limits_{\nu =a }^b f(\nu) := \exp\left(\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = a}^b \ln f(\nu) \right) ,$$whenever $\ln f$ is right summable. 

**Th:** We see that the definition above satisfies all summation axioms, and it also satisfies the following property (by design): *Right shift continuity*, if $\lim_{n \to \infty} f(z+n) = 0$ pointwise for every $z\in \Bbb C$, then $$\lim_{n \to \infty}\sum_{\nu = x}^y f(\nu +n) = 0;$$more generally, if there is a sequence of polynomials $(p_n)_{n <\omega}$ of fixed degree such that as $\lim_{n \to \infty} |f(n+x)-p_n(n+x)| = 0$ for all $z\in \Bbb U$, we requiere that for all $$\lim_{n \to\infty} \left|\sum_{\nu = x}^y f(\nu + n) - \sum_{\nu = x}^y p_n(\nu + n)\right| = 0.$$Additionally, this definition is unique in the space of functions we are considering.

**Lemma:** Let $S: U \to \Bbb C$ be a right approximate polynomial of degree $\sigma \in \omega\cup\{-\infty\}$, such that $0\in U$. Then $\Delta S: U \to \Bbb C$ is a right approximate polynomial of degree $\sigma -1$ ($\Delta S(z) := S(z+1)-S(z)$, the [[Discrete Calculus|forward difference]]); moreover, for all $x\in U$, the right sum $\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 0}^{x-1} \Delta S(\nu)$ exists in $U$ and equals $S(x) - S(0)$.  
Conversely, if $f: U+1 \to \Bbb C$ is a right approximate polynomial of degree $\sigma$ which is right summable, then the function $S(x) := \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 0}^{x-1} f(\nu): U \to \Bbb C$ is right approximately polynomial of degree $\sigma+1$ and satisfies $\Delta S = f$. 

**Lemma:** Let $f, g: U \to \Bbb C$ be right summable functions such that $x\mapsto \left(\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x f(\nu) \right) \cdot \left(\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x g(\nu) \right)$ is a right approximate polynomial. Then every $x\in U$ satisfies $$\left(\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x f(\nu) \right) \left(\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x g(\nu)\right) = \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x \left(f(\nu)g(\nu)+ f(\nu)\ \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{k = 1}^{\nu-1} g(k)  + g(\nu) \ \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^{\nu-1} f(k)  \right) .$$
**Cor:** Suppose $f: U \to \Bbb C$ is a right summable function such that $x \mapsto \left(\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x f(\nu) \right)^2$ is a right approximate polynomial, then $$\left(\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x f(\nu)\right)^2 = \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x \left(f(\nu)^2 +2f(\nu)\ \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^{\nu-1} f(k)\right). $$
**My Prop:** Let $f: U \to \Bbb C$ be a right approximate polynomial of degree $\sigma \in \omega$. Then the sequence of polynomials $$q_n (x) = \sum_{\nu = 0}^\sigma {x \choose \nu} \Delta^\nu f(n)$$also approximates the right polynomial. In the case that $\sigma = -\infty$, then we see that $f$ that is right approximate to $0$. Then we also get the formula to be $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = a}^b f(\nu) := \lim_{n \to\infty} \left(\sum_{\nu= n+a}^{n+b}\sum_{\nu = 0}^\sigma {x \choose \nu} \Delta^\nu f(n)  + \sum_{\nu = 1}^{n} f(\nu+a-1)-f(\nu+b))\right).  $$

In the context of this note (because the article does this, again it is just foul), we will use a helpful definition. Classically, sums $\sum_{\nu = 1}^N$ are defined only for integers $N$ with $N\ge 1$ or $N \ge 0$. If $N \in \Bbb N$, it will be natural for this note to define $$\sum_{\nu = 1}^{-N} f(\nu):=-\sum_{\nu = -N+1}^0 f(\nu); $$this the only way to extended the continued summation axiom, and this works for *every $f$* which is defined on $\{-N+1, \dots, 0\}$. Similarly, if $x-y\in \Bbb N$ we set $$\sum_{\nu = y}^x f(\nu):=- \sum_{\nu= x+1}^{y-1} f(\nu) $$for any $f$ which is defined at the finitely many points $\{x+1, \dots, y-1\}$. 

**Def:** Let $U\subseteq \Bbb C$ and $\sigma\in \omega\cup\{-\infty\}$. A function $f: U \to \Bbb C$ will be called a left approximate polynomial of degree $\sigma$ if the following conditions are satisfied:
- if $x\in U$ then $x-1\in U$.
- there exists a sequence of polynomials $(p_n)_{n <\omega}$ of fixed degree $\sigma$ such that for all $x\in U$, $$\lim_{n \to -\infty} |f(n+x)-p_n(n+x)| = 0.$$
**Def:** A left approximate polynomial $f: U \to \Bbb C$ of degree $\sigma\in \omega\cup\{-\infty\}$ will be called *left summable* if for every $a, b+1\in U$, the limit $$\lim_{n \to-\infty} \left(\sum_{\nu= n+x}^{n+y} p_n(\nu) + \sum_{\nu = 1}^n f(\nu+x-1)-f(\nu+y))\right)$$exists. In this case, this limite will be the definition of the *left fractional sum of $f$ from $a$ to $b$; we will denote it by*:$$\mathop{\leftarrow\!\!\!\!\!\!\!\!\sum}\limits_{\nu = a}^b f(\nu) := \lim_{n \to-\infty} \left(\sum_{\nu= n+a}^{n+b} p_n(\nu) + \sum_{\nu = 1}^n f(\nu+a-1)-f(\nu+b))\right).$$Moreover, we can define *left fractional products by* $$\mathop{\leftarrow\!\!\!\!\!\!\prod}\limits_{\nu =a }^b f(\nu) := \exp\left(\mathop{\leftarrow\!\!\!\!\!\!\!\!\sum}\limits_{\nu = a}^b \ln f(\nu) \right) ,$$whenever $\ln f$ is left summable. 

Let us not that the existence of the two sums $\mathop{\leftarrow\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x f(\nu)$ and $\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x f(\nu)$ is independent, and if both are defined, their values can be different.

**Lemma:** We have $$\mathop{\leftarrow\!\!\!\!\!\!\!\!\sum}\limits_{\nu = a}^b f(\nu) = \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = -b}^{-a} f(-\nu) $$for all $a, b\in \Bbb C$ for which at least one of these sums exists. 

**Prop:** For all $x\in \Bbb C$, we have
$$
\begin{align*}
\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 0}^x q^\nu &= \frac{1-q^{x+1}}{1-q} \qquad \text{for $0\le |q |< 1$, and } \\
\mathop{\leftarrow\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 0}^x q^\nu &= \frac{1-q^{x+1}}{1-q} \qquad \text{for $|q |> 1$}.
\end{align*}
$$

**Th:** Let $c\in \Bbb C \setminus \Bbb Z^{<0}$ we have $$
\begin{align*}
(1+x)^c &= \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 0}^c{c \choose \nu} x^\nu \qquad \text{for $0\le |x |< 1$, and } \\
(1+x)^c &= \mathop{\leftarrow\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 0}^x {c \choose \nu} x^\nu\qquad \text{for $|x |> 1$}.
\end{align*}
$$
**Prop:** If we would like to sum over $\ln z$, we see that the sequence of constants $\ln n$ are a good approximating sequence, and we would get that $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^z \ln \nu = \lim_{n \to \infty}\left(z\ln n + \sum_{\nu = 1}^n \ln \left(\frac{\nu}{\nu +z}\right)\right).$$This, in turn, implies that $$z!:=\mathop{\to\!\!\!\!\!\!\!\prod}\limits_{\nu = 1}^z \nu = \lim_{n\to \infty} \left(n^z \prod_{\nu = 1}^n \frac{\nu}{\nu +z}\right) = \Gamma(z+1).$$This is because it is the Gauss representation of the [[Gamma Function]].  Using this and the [[Gamma Function#Euler’s Reflection Formula|Gamma Functions Reflection's Formula]] we get that: $$\mathop{\to\!\!\!\!\!\!\!\prod}\limits_{\nu = 1}^{-1/2} (\nu^2+1) = \tanh(\pi).$$
An important example is the function $\nu \mapsto \nu^{-1}$. This function is related to the harmonic series and the [[Harmonic Numbers]]. Then we get that $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x \frac1\nu = \sum_{\nu = 1}^\infty\left(\frac1\nu - \frac1{\nu-x}\right).$$Just to be a bit clear, the domain of the function is exactly $\Bbb C \setminus  \Bbb Z^{<0}$. In particular, we get the identity $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^{-1/2}\frac1\nu =-2\ln 2.$$This function is related to the [[Digamma function]], and the [[Euler–Mascheroni Constant]] by the following equation $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x \frac1{\nu} = \gamma + \psi(x+1).$$With this information, and the fact that the Digamma function has a similar reflection formula we have that: $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = x}^{-x}\frac1{\nu} = \pi\cot(\pi x) = \psi(x) - \psi(1-x).$$

# [[Riemann Zeta Function|Riemann]] and [[Hurwirz Zeta Function|Hurwitz]] Zeta Functions

The following Dirchlet series generalises the Riemann $\zeta$ function and is known as the Hurwitz $\zeta$ function: $$\zeta(s, x) := \sum_{\nu = 0}^\infty \frac1{(\nu +x)^s}; $$here $x$ is an arbitrary complex number but not a nonpositive integer. The series converges whenever $\Re(s) > 1$. For the definition of the powers $(\nu + x)^{-s}$, w e use a branch cut at $\Bbb R^-$, and then define the complex logarithm on $\Bbb R^-$ via continuity from above. This way, the function $x \mapsto \zeta(s, x)$ is analytic on $\Bbb C\setminus (-\infty, 0]$. 

For every $x \in \Bbb C\setminus \Bbb Z^{\le 0}$, the Hurwitz zeta function extends to a meromorphic function in $s$ with a single pole at $s = 1$. One way to see this is via the formula $$\frac{\partial}{\partial s} \zeta(s-1, x) = (s-1) \zeta(s, x), \qquad \text{ for every }x\in\Bbb C\setminus (-\infty, 0].$$
The  difference to the Riemann $\zeta$ function is the appearance of $x$, and in fact that the summation starts at $\nu = 0$; hence $\zeta(s, 1) = \zeta(s)$. 

**Lemma (Polynomial Approximation of the Hurwitz Zeta Function):** For every compact $K\subseteq \Bbb C$ and every $s\in \Bbb C\setminus \{1\}$, there is a sequence of complex polynomials $p_n$ of degree $\sigma(s)$ such that $$|\zeta(s, n+z) - p_n(n+z)|\to 0 $$as $n\to \infty$, uniformly for $z\in K$, with  $$\sigma(s) := \begin{cases}
-\infty, & \text{if }\Re(s) > 1, \\
1+ \lfloor\Re(-s)\rfloor & \text{if }\Re(s) \le 1 \text{ and } s\ne 1.
\end{cases} $$In particular, $z\mapsto \zeta(s, z)$ is approximately polynomial of degree $\sigma(s)$. 

**Cor (Extended Riemann-Hurwitz Zeta Function):** For $x\in \Bbb C\setminus\Bbb Z^ñ{\le 0}$ and $a\in \Bbb C\setminus\{-1\}$, the fractional sum $\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x \nu^a$ exists and satisfies $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x\nu^a = \zeta(-a)-\zeta(-a, x+1). $$
**Cor (Zeta Derivatives Identity):** For $x\in \Bbb C\setminus \Bbb Z^{<0}$, all $a\in \Bbb C\setminus\{-1\}$ and $b\in \Bbb N$, we have $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^x \nu^a(\ln \nu)^b = (-1)^b(\zeta^{(b)}(-a) - \zeta^{(b)}(-a,x+1)) $$where $\zeta^{(b)} = (\frac{\partial}{\partial a})^b\zeta$. 

**Cor (Power Sums up to $-1/2$):** For all $n \in \Bbb N^+$ and $a\in \Bbb C\setminus\{-1\}$, we have $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^{-1/2} \nu^a = (2-2^{-a}) \zeta(-a) \qquad \text{and}\qquad \mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^{-1/2}\nu^{2n} = 0. $$
**Power Sums and Zeros of the Zeta Function:** Modify the definition of $\nuẑ$ so that $\nu^z = 0$ for $\nu = 0$. Then for all $z\in\Bbb C\setminus (2\Bbb Z+1)$ with $2^{-z} \neq 2$, we have  $$\mathop{\to\!\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^{-1/2} \nu^z = \mathop{\leftarrow\!\!\!\!\!\!\!\sum}\limits_{\nu = 1}^{-1/2} \nu^z \iff \zeta(-z) = 0.$$
