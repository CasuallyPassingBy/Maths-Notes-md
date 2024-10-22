---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Convergence of Fourier Series]], [[Main definitions for Fourier Analysis]]

# Isoperimetric inequality
Suppose that $\Gamma$ is simple closed curve in $\Bbb R^2$ that is piecewise smooth, with length $\ell$. Then using [[Green's Theorem and Curl in R2]], then we can calculate the [[Jordan measure]] of the set $\Omega$ such that $\partial \Omega = \Gamma$. Then $$J(\Omega) \le \frac{\ell^2}{4\pi}$$
With the equality iff $\Gamma$ is a circle.

The way we do it is through, just supposing that the $\ell = \pi$, and trying to get a simplified as $J(\Omega) \le \pi$. Considering the arc-length parametrization $\gamma: [0, 2\pi]\to \Bbb R^2$, $\gamma(s) =(x(s), y(s))$. Then we can exploit that each $x$ and $y$ is $2\pi$-periodic. 

With this $$\frac1{2\pi} \int_0^{2\pi} (x'(s)^2+ y'(s)^2)\, ds = 1$$and $$x(s) \sim \sum a_n e^{ins} \qquad y(s) \sim b_n e^{ins}$$thus getting that $$x'(s) \sim \sum a_nin e^{ins} \qquad y(s) \sim b_nin e^{ins}$$

Using Parseval's identity is applied and gives us that $$\sum_{n \in \Bbb Z} |n|^2(|a_n|^2+|b_n|^2 ) = 1$$
By Green's Theorem we have that $$J(\Omega) = \frac1{2}\left|\int_0^{2\pi} x(s) y'(s) - y(s)x'(s)\, dx \right| = \pi \left|\sum_{n \in \Bbb Z} n(a_n \overline{b_n} - b_n \overline{a_n})\right|$$Then we get that $$J(\Omega) \le \pi \sum_{n \in \Bbb Z} |n|^2(|a_n|^2+|b_n|^2 )  = \pi$$. 

# Weyl's equidistribution theorem
If $x$ is a real number, and let $\lfloor x \rfloor$ is the greatest integer less than or equal to $x$, and we call $\lfloor x \rfloor$ is the *integer part* of $x$. The *fractional part* of $x$ is defined by $\{ x \} = x - \lfloor x \rfloor$

We can look at the [[Normal Subgroups and Quotient Groups|quotient group]] $\Bbb R/\Bbb Z$, then we can consider that tag each $x + \Bbb Z$, with the representative $\{x\}$.

If we have a real number $\gamma \ne 0$, and we look at the sequence $\gamma, 2\gamma, 3\gamma, \dots$ If we reduce it modulo $\Bbb Z$, that is we look at the sequence of fractional parts $$\{\gamma\}, \{2\gamma\}, \{3\gamma\}, \dots$$
Some trivial stuff is:
- If $\gamma\in \Bbb Q$, then only finitely many numbers appearing in $\{n\gamma\}$ are distinct.
- If $\gamma \in \Bbb R\setminus \Bbb Q$, then the numbers $\{n\gamma\}$ are all distinct. 

**Def:** A sequence of numbers $x_1, x_2, \dots, x_n, \dots$  in $[0, 1)$ is said to be *equidistributed* if for every interval $(a, b) \subseteq [0, 1)$, $$\lim_{n \to \infty} \frac{|\{1 \le k \le n \mid x_n \in (a,b)\}}{n} = b-a$$
We see that a sequence being equidistributed is a stronger condition that the sequence is dense, and the converse is not true, since we can create from an enumeration of the rationals, a not equidistributed. 

We can transform the problem a bit, considering $\chi_{(a,b)}$ where $(a, b) \subseteq [0, 1)$. We extend this function to $\Bbb R$ by periodicity, and we still denoted this extension by $\chi_{(a,b)}(x)$. Then, as a consequence of the definitions, we find that $$|\{1 \le k \le n \mid \{k\gamma\} \in (a,b)\}| = \sum_{k = 1}^n \chi_{(a,b)}(n \gamma)$$Then the theorem can be reformulated as the statement that $$\frac1{N} \sum_{n = 1}^N \chi_{(a, b)}(n \gamma) \to \int_0^1\chi_{(a,b)}(x)\, dx \qquad N \to \infty$$This reduces the number theory to analysis.

**Lemma:** If $f$ is continuous and periodic of period $1$, and $\gamma$ is irrational, then $$\frac1{N} \sum_{n = 1}^N f(n\gamma) \to \int_0^1f(x)\, dx \qquad N \to \infty$$
**Cor:** If $f$ is Riemann integrable in $[0, 1]$, periodic of period $1$ and $\gamma$ irrational, then $$\frac1{N} \sum_{n = 1}^N f(n\gamma) \to \int_0^1f(x)\, dx \qquad N \to \infty$$
With this theorem, we see that $$\frac1{N} \sum_{n = 1}^N \chi_{(a, b)}(n \gamma) \to \int_0^1\chi_{(a,b)}(x)\, dx \qquad N \to \infty$$Thus having $\{\gamma\}, \{2\gamma\}, \dots$ is an equidistributed sequence of points in $[0, 1)$. Trivially, we have that the sequence $\{n\gamma\}$  is dense in $[0, 1)$. 

There is an [[Ergodic Theory]] interpretation of this result, that the simple dynamical system given $\rho: x \mapsto x + \gamma$ being the fractional part, then $\rho^n:x\mapsto x + n \gamma$, where we think that the action $\rho^n$ taking place at the time $t = n$. 

For each Riemann integrable function $f$ on the circle, we also associate the effects of the action $\rho$, and we obtain the sequence of functions $$f(x), f(\rho(x)), f(\rho^2(x)),, \dots, f(\rho^n(x)), \dots $$
In this context, the *ergodicity*of the system is then the statement that the "time average" $$\lim_{n \to \infty} \frac1{n}\sum_{k = 1}^n f(\rho^k(x))$$exists for each $x$ and equals the "space average" $$\int_0 ^1 f(x)\, dx$$whenever $\gamma$ is irrational

### Weyl's Criterion
A sequence of real numbers $x_1, x_2, \dots$ in $[0, 1)$ is equidistributed iff for all integers $k \ne 0$ one has $$\frac1{N}\sum_{n = 1}^N e^{2\pi i k x_n} \to 0 \qquad N \to \infty$$
We can also solve [[The Heat Equation on the Circle]]