---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Convergence of Random Variables]], [[Important Probability Inequalities]], [[Weak Topology on the Space of Radon Measures]]

# Weak Law of Large Numbers 

Let $X_1, X_2, \dots$ be independent and identically distributed random variables with mean $\mu$. Then $$\frac{1}{n}\sum_{i = 1}^n X_i \stackrel{\Bbb P}{\longrightarrow} \mu$$
**Def:** Suppose that $(\Omega, {\scr A}, \Bbb P)$ is a probability space and let $(A_n)_{n<\omega}$ is a sequence of events in $\scr A.$ Then $$\{\omega\in\Omega\mid \omega\in A_n \text{ for infinitely many }n\}  $$is equal to $\limsup_{n \to \infty} A_n :=\bigcap_{n = 1}^\infty \bigcup_{k =n }^\infty A_k$; it is the even that infinitely many of the events $A_n$ occur, and it is often written as $\{A_n \text{ i.o.}\}$, where i.o. means "infinitely often". 

**Borel-Cantelli Lemmas:** Let $(\Omega, {\scr A}, \Bbb P)$ be a probability space, and let $(A_n)_{n<\omega}$ be a sequence of events in $\scr A$.
- If $\sum_{n<\omega} \Bbb P(A_n)<\infty$, then $\Bbb P_n(\{A_n \text{ i.o.}\}) = 0$.
- If the events $A_n$, $n<\omega$, are independent and if $\sum_{n<\omega} \Bbb P(A_n) =\infty$, then $\Bbb P(\{A_n \text{ i.o.}\}) = 1$. 

**Kolmogorov Zero-One Law:** Suppose that $(X_n)_{n<\omega}$ is a sequence of independent random variables. Then each event that belongs to the $\sigma$-algebra  $$\bigcap_{n<\omega} \sigma(X_n , X_{n+1}, \dots) $$has probability $0$ or $1$.

The intersection of the $\sigma$-algebras $\sigma(X_n, X_{n+1}, \dots)$ is called the *tail $\sigma$-algebra*of the sequencce $(X_n)_{n<\omega}$, and its members are called *tail elements*. 

**Prop:** Suppose that $(X_n)_{n<\omega}$ is a sequence of independent random variables and that $\scr T$ is the $\sigma$-algebra of tail events $(X_n)_{n<\omega}$. Then every $\overline{\Bbb R}$-valued random variable that is $\scr T$-measurable is almost surely constant. 

**Lemma:** Let $(X_n)_{n<\omega}$ be a sequence of independent random variables that have mean $0$ and satisfy $\sum_{n<\omega} \Bbb E[X_n^2]<\infty$. Then $\sum_{n<\omega} X_n$ converges almost surely.

# Strong Law of Large Numbers
Let $X_1, X_2, \dots$ be independent and identically distributed random variables with finite mean $\mu$. Then $$\frac{1}{n}\sum_{i = 1}^n X_i \stackrel{a.s.}{\longrightarrow} \mu$$
**Converse of the Strong Law of Large Numbers:** Let $(X_n)_{n<\omega}$ be a sequence of independent identically distributed random variables that do not have finite expected values. For each $n<\omega$ let $S_n = X_1+ \dots+X_n$. Then  $$\limsup_{n\to \infty}\left|\frac{S_n}n\right|=\infty \quad  \text{almost surely.} $$
**Def:** Let $b$ be an integer such that $b\ge 2$. The digits that can occur in base $b$ expansion of a number are $0, \dots, b-1$. A number $x$ in $[0, 1]$ is *normal to base $b$* if each value in $\{0, \dots, b-1\}$ occurs the expected fraction, namely $1/b$, of the time in the base $b$ expansion of $x$, that is,  $$\lim_{n \to \infty} \frac{\text{number of times }k \text{ occurs the first }n \text{ digits of }x}{n} =\frac1b$$holds $k\in \{0, \dots, b-1\}$. The value $x$ is *normal* if it is normal to base $b$ for every $b$. 

**Prop:**
- For a given base $b$, then almost every number in $[0, 1]$ is normal to base $b$.
- Almost every number in $[0, 1]$ is normal.

**Def:** Let $(\Omega, {\scr A},\Bbb P)$ be a probability space, let $\mu$ be a probability distribution on $(\Omega, {\scr A},\Bbb P)$, let $F$ be its distribution function, and let $(X_n)_{n\in \Bbb N}$ be a sequence of independent random variables on $(\Omega, {\scr A}, \Bbb P)$, each of which has distribution $\mu$. For each $\omega\in \Omega$, $(X_n(\omega))_{n\in \Bbb N}$ is a sequence of real numbers, and we can define $(\mu_n^\omega)_{n\in \Bbb N}$ of measures on $( \Bbb R, \mathcal B(\Bbb R))$ by letting $\mu_n := (1/n) \sum_{k<n} \delta_{X_k(\omega)}$. Also, let $F_n^\omega$ be the distribution function of the measure $\mu_n^\omega$; thus,  $$F^\omega_n (x) = \frac1n \sum_{k = 1 ^n} \chi_{(-\infty, x]}\circ X_k(\omega) = \frac{\text{number of }1\le k \le n\text{ for which }X_k(\omega) \le x}{n} $$holds for all $n, \omega \in \Omega$, and $x$. Such functions $F^\omega_n$ are called *empirical distribution functions*. 

**Glivenko-Cantelli Theorem:** Let $(\Omega, {\scr A},\Bbb P)$ be a probability space, let $\mu$ be a probability distribution on $(\Omega, {\scr A},\Bbb P)$, let $F$ be its distribution function, and let $(X_n)_{n\in \Bbb N}$ be a sequence of independent random variables on $(\Omega, {\scr A}, \Bbb P)$, each of which has distribution $\mu$. The empirical distribution functions converge uniformly to the theoretical distribution function almost surely. That is, there exists a measurable set $\Omega_0\in \scr A$ with $\Bbb P(\Omega_0) = 1$ such that for every $\omega\in \Omega_0$:  $$\lim_{n\to\infty}\sup_{x\in \Bbb R} |F^\omega_n(x) - F(x)| = 0. $$
**Lemma:** Let $X_1, X_2, \dots$ be independent random variables on $(\Omega, {\scr A}, \Bbb P)$, each of which has mean $0$, and for each $i$ let $\sigma^2_i$ be the variance of $X_i$. If there is a a constant $c$ such that $|X_i|\le c$ holds almost surely for each $i$ and if the series $\sum_{i = 1}^\infty X_i$ is almost surely convergent, then $\sum_{i = 1}^n \sigma^2_i <\infty$. 

**Th:** Let $X_1, X_2, \dots$ be independent random variables on $(\Omega, {\scr A}, \Bbb P)$, and for each $i$ let $\sigma^2_i$ be the variance of $X_i$. If there is a a constant $c$ such that $|X_i|\le c$ holds almost surely for each $i$ and if the series $\sum_{i = 1}^\infty X_i$ is almost surely convergent, then $\sum_{i = 1}^n \sigma^2_i <\infty$. 

We define $Y_i(\omega_1, \omega_2) = X_i(\omega_1)- X_i(\omega_2)$, and apply the above lemma to $(Y_i)_{i= 1}^\infty$. 

**Cor:** Let $(X_n)_{n<\omega}$ be a sequence of independent random variables such that $P(X_n= 1) = P(X_n= -1) = 1/2$ holds for each $n<\omega$, and let $(a_n)_{n<\omega}$ a sequence of real numbers. The series $\sum_{n<\omega}a_n X_n$ converges almost surely iff $(a_n)_{n<\omega}\in \ell^2$. 

**Def:** Let $c > 0$ and $X$ is an random variable on $(\Omega, {\scr A}, \Bbb P)$. We define a new random variable, the truncation $X^{(c)}$ of $X$ by $c$, as follows: $$X^{(c)}(\omega) := \begin{cases} X(\omega) & \text{ if }|X(\omega)|\le c, \\ 0 & \text{otherwise}.\end{cases} $$
**The Three Series Theorem:** Let $X_0, X_1, \dots$ be independent random variables on $(\Omega, {\scr A}, \Bbb P)$, let $c> 0$. The series $\sum_{n<\omega} X_n$ converges almost surely iff the series
- $\sum_{n<\omega} \Bbb P(|X_n|> c)$,
- $\sum_{n<\omega} \Bbb E[X^{(c)}]$, and
- $\sum_{n <\omega} \text{Var}(X^{(c)})$
all converge. 

# Central Limit Theorem

Let $X_1, \dots$ be a sequence of independent and identically distributed random variables, such that $E[X_n] = \mu$ and $\text{Var}(X_n) = \sigma^2<\infty$. Then $$\frac{X_1+\dots + X_n- n \mu}{\sqrt n \sigma} \stackrel{d}{\longrightarrow} N(0, 1).$$If we consider the averages as $$\bar X_n := \frac{1}{n}\sum_{k = 1}^n X_k.$$
Then we can rewrite it as $$\frac{(\bar X_n - \mu )}{\sigma/\sqrt n } \stackrel{d}{\longrightarrow} N(0, 1).$$
# Slutsky's Theorem
Let $X_n, Y_n$ be sequences of random variables. If $X_n \stackrel{d}{\longrightarrow} X$, and $Y_n \stackrel{d}{\longrightarrow} c$ where $c$ is a constant, then
- $X_n + Y_n \stackrel{d}{\longrightarrow} X + c$
- $X_n Y_n \stackrel{d}{\longrightarrow} Xc$
- $X_n/Y_n \stackrel{d}{\longrightarrow} X/c$ provided that $c \neq 0$.

This gives us the following version of the of central limit theorem: $$\frac{\sqrt n (\bar X_n - \mu )}{S_n} \stackrel{d}{\longrightarrow} N(0, 1),$$where $$\bar X_n := \frac1{n}\sum_{k = 1}X_k, \qquad S^2_n := \frac{1}{n-1} \sum_{k = 1}^n (X_k - \bar X_n)^2.$$

# De Moivre-Laplace Theorem

Let $X_1, \dots$ be a sequence of independent and identically distributed random variables with Bernoulli distribution with parameter $p \in (0,1)$. For any two real numbers $a<b$ $$\lim_{n \to \infty} \Bbb P\left(a <\frac{X_1 + \dots+ X_n -np}{\sqrt{np(1-p)}}<b\right) = \frac{1}{2\pi} \int_a^be^{-x^2/2}\, dx$$ 