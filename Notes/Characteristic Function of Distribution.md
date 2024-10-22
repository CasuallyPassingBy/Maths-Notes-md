---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Probability Generating Function]], [[Moment Generating Function]], [[Convergence of Random Variables]]

**Def:** The *characteristic function* of a random $X$ is a function $$\phi(t) = E\left[ e^{itX}\right]$$defined over every real $t$. 

Then this transforms into $$\phi(t) = E(\cos tX) + i\sin tX)$$
and we have that $M$ is the moment generating function, $\phi(t) = M(it)$. 
Then $G$ be the probability generating function $G$, then $\phi(t) = G(e^{it})$. 

We see that the characteristic function is the [[Fourier Transform in R]] of the probability distribution.

**Existence:** For any $t\in \Bbb R$, the $|\phi(t)| \le 1$. In particular $\phi(0) = 1$

**Prop:** If $X$ has finite $n$th moment, then 
- $$\left.\frac{d^n}{dt^n}\right|_{t = 0} = i^nE[X^n]$$
- When $t\to 0$, then $$\phi(t) = \sum_{k = 0}^{n-1}\frac{(it)^k}{k!} E[X^k] + \frac{(it)^n}{n!}(E[X^n] + o(1))$$

**Prop**: Let $X$ and $Y$ be independent, the $\phi_{X+Y}(t) = \phi_X(t) \phi_Y(t)$, and $$\phi_{XY} (t) = \int_{-\infty}^\infty \phi_Y(tx) \, dF_X(x)\int_{-\infty}^\infty \phi_Y(ty) \, dF_Y(y)$$
### Lèvy Inversion Formula

Let $X$ be random variable with distribution $F(x)$, the with characteristic function $\phi(t)$. If $x < y$, then $$\frac{1}{2}(F(y)+F(y-) )-\frac{1}{2}(F(x)+F(x-)) = \lim_{T\to \infty} \frac{1}{2\pi} \int_{-T}^t \frac{e^{-itx}-e^{-ity} }{it} \phi(t)\, dt$$
if $x$ and $y$ are continuity points then it turns into $$F(y) - F(x) = \lim_{T\to \infty} \frac{1}{2\pi} \int_{-T}^t \frac{e^{-itx}-e^{-ity} }{it} \phi(t)\, dt$$
**Unicity**: If $X$ and $Y$ are such that $\phi_X(t) = \phi_Y(t)$ for all $t\in \Bbb R$, then $X$ and $Y$ have the same distribution. 

#### Inversion for the absolutely continuous case
Let $X$ be absolutely continuous with a pdf $f(x)$, and characteristic function $\phi(t)$. Then $$f(x) = \frac{1}{2\pi }\int_{-\infty}^\infty e^{-itx} \phi(t)\, dt $$
**Continuity:** Let $X_1, \dots$ be sequence of random variables. Then $X_n \stackrel{d}{\longrightarrow} X$ iff $\phi_{X_n}(t) \to \phi_X(t)$. 