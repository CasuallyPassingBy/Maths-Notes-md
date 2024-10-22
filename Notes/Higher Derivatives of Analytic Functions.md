---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]], [[Cauchy's Integral Formula]]

### Differentiability of Cauchy Type integrals

********Th:******** Let $\gamma \subseteq \Bbb C$ be a piecewise smooth curve. For each $n\in \Bbb N$ and each $\varphi:\gamma\to \Bbb C$ continuous on $\gamma$, the function $F_{n, \varphi}:\Bbb C\setminus \gamma \to \Bbb C$ defined as

$$ F_{n, \varphi}(z)= \int_{\gamma}\frac{\varphi(\zeta)}{(\zeta-z)^n}\, d\zeta $$

is continuous in $\Bbb C\setminus \gamma$.

********Th:******** Let $\gamma \subseteq \Bbb C$ be a piecewise smooth curve. For each $n\in \Bbb N$ and each $\varphi:\gamma\to \Bbb C$ continuous on $\gamma$, the function $F_{n, \varphi}:\Bbb C\setminus \gamma \to \Bbb C$ defined as

$$ F_{n, \varphi}(z)= \int_{\gamma}\frac{\varphi(\zeta)}{(\zeta-z)^n}\, d\zeta $$

is analytic in $\Bbb C\setminus \gamma$, and

$$ F'_{n, \varphi}(z)=n \int_{\gamma}\frac{\varphi(\zeta)}{(\zeta-z)^{n+1}}\, d\zeta =n F_{n+1, \varphi} $$

********Cor:******** Let $\gamma \subseteq \Bbb C$ be a piecewise smooth curve, and $\varphi:\gamma\to \Bbb C$ continuous on $\gamma$, the function ${F:\Bbb C\setminus \gamma \to \Bbb C}$ defined as

$$ F(z)= \int_{\gamma}\frac{\varphi(\zeta)}{(\zeta-z)}\, d\zeta $$

then $F^{(n)}$ exists for all $n \in \Bbb N$ and for all $z \in \Bbb C \setminus \gamma$, and

$$ F^{(n)}(z) = n! \int_\gamma \frac{\varphi(\zeta)}{(\zeta-z)^{n+1}}\, d\zeta $$

********Th:******** Suppose $\gamma$ is a curve in $\Bbb C$ and $g$ is a contiuous function defined along the image of $\operatorname{Im} \gamma$. Set

$$ G(z ) = \frac{1}{2\pi i }\int_\gamma \frac{g(\zeta)}{\zeta -z} \, d\zeta $$

Then $G$ is holomorphic on $\Bbb C\setminus \operatorname{Im} \gamma$; in fact $G$, is infinitely differentiable, with the $k$th derivative given by

$$ G^{(k)}(z) = \frac{k!}{2\pi i} \int_\gamma \frac{g(\zeta)}{(\zeta-z)^{k+1}}\, d\zeta $$

this is proven using the differentiation under the integral sign.

We can weaken the constraints of $g$, we just need that $g$ is bounded and integrable over $\gamma$.

### Cauchy Integral Formula for Derivatives

Let $f$ be analyitic on a region $A$. Then all the derivatives exist on $A$. Furthermore, let $\gamma$ be closed curve in $A$ that is homotopic to a point, let $z_0 \in A$ be a point not on $\gamma$. Then

$$ f^{(k)}(z_0) \cdot n(\gamma; z_0) = \frac{k!}{2\pi i}\oint_\gamma \frac{f(\zeta)}{(\zeta-z_0)^{k+1}}\, d\zeta $$

for $k \in \Bbb N$.

### Cauchy’s Inequalities

Let $f$ be analyitic on a region $A$, and let $\gamma$ be a circle with radius $R$ and center $z_0$ that lies in $A$. Assume the the disk $B_R(z_0)$ also lies in $A$. Suppose that $|f(z)| \le M$ for all $z$ on $\gamma$. Then for any $k \in \Bbb N$

$$ |f^{(k)}(z_0)| \le \frac{k!}{R^k} M $$

**********Def:********** We say that if $f:\Bbb C\to \Bbb C$ is holomorphic on $\Bbb C$, then we call $f$ entire

### Liouville’s Theorem
If $f$ is an entire and there is a constant $M$, such that $|f(z)| \le M$ for all $z \in \Bbb C$, then $f$ is constant.

### The Fundamental Theorem of Alegebra
Let $a_0, a_1, \dots, a_n$ be a collection of $n+1$ complex numbers and suppose $n \ge1$ and $a_n \ne 0$. Let $p(z) = a_0 + a_1z +\dots a_n z^n$. Then there exists a point in $z_0 \in \Bbb C$, such that $p(z_0) =0$ .

**********Cor:********** If $P(x)$ is a polynoomial of degree $n \ge1$ with complex coefficients, then there exists constants $x_1, x_2,\dots, x_k$, and unique positive integers $m_1, m_2, \dots, m_k$, such that $\sum_{i = 1}^k m_i = n$, and

$$ P(x) = a \prod_{i = 1}^k (x-x_i)^{m_i} $$

**********Cor:********** Let $P(x)$ and $Q(x)$ be polynomials of degree at most $n$. If $x_1, x_2, \dots, x_k$ with $k >n$, are distinct numbers with $P(x_i) = Q(x_i)$ for $1 \le i \le k$, the $P(x) = Q(x)$ for all values of $x$.

********Cor:******** Let $P \in \Bbb R[x]$, if $z = a+bi$ is root with multiplicity $m$, then $\overline z$ is also a root with multiplicty $m$, and $(x^2+2ax+a^2+b^2)^m$ is a factor of $P(x)$

### Morera’s Theorem
Let $f$ be a continuous function on a region $A$, and suppose that $\oint_\gamma f =0$ for every closed curve in $A$. Then $f$ is holomorphic on $A$, and $f = F'$ for some holomorphic function $F$ on $A$.

**********Cor:********** Let $f$ be a continuous function on $A$ and holomorphic on $A\setminus \{ z_0\}$ for some point $z_0 \in A$. Then $f$ is holomorphic on $A$.

### Logarithms of Functions
Let $f$ be an holomorphic function that is never $0$ on a simply connected domain $A$. Then there is a function $g$ holomorphic on $A$ and unique up to addition of constant multiples of $2\pi i$ such that $\exp(g(z)) =f(z)$ for all $z \in A$.