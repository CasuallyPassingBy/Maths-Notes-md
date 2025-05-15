---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measure Spaces and Measurable Spaces]], [[Measurable Functions]], [[Integration of Simple Functions]],[[Normed Vector Spaces]]

**Def:** If $f$ and $g$ are integrable simple functions, we define the *distance between them* as $$d(f, g) := \int |f-g|\, d\mu.$$
**Def:** A sequence $\{f_n \mid  n <\omega\}$ of integrable simple functions is *fundamental in the mean* or *mean fundamental*, if $$d(f_n, f_m) \to 0 \qquad \text{as }n, m \to \infty.$$
**Def:** An a.e. finite valued measurable function $f$ on a measure space $(X, \mathcal S, \mu)$ is *integrable* if there exists a mean fundamental sequence $\{f_n \mid n <\omega\}$ of integrable simple functions which converges in measure to $f$. The *integral* of $f$, $$\int f(x)\, d\mu(x) = \int f\, d\mu := \lim_{n \to\infty} \int f_n \, d\mu.$$
It follows from [[Integration of Simple Functions#^3830db|this]] result, that value fo the integral of $f$ is uniquely determined by any particular such sequence. 

**Obs:** We see that if $f, g: X \to \Bbb R$ are integrable functions, and $\lambda \in \Bbb R$, then the following are true:
- $|f|$ is integrable.
- $\lambda f$ is integrable.
- $f+g$ is integrable.
- $f^+$ and $f^-$ are integrable. 

**Def:** If $E$ is a measurable set and if $\{f_n \mid n <\omega\}$ is a mean fundamental sequence of integrable simple functions converging in measure to the integrable function $f$, then it is easy to see that the sequence $\{\chi_E f_n \mid n <\omega\}$ is mean fundamental and converges in measure to $\chi_E f$. We define the *integral of $f$ over $E$* by $$\int_E f\, d\mu := \int \chi_E f\, d\mu.$$
**Def:** The space of all integrable integrable functions is denoted as $\mathcal L^1(X, \mu)$ or $\mathcal L^1(X, \mathcal S, \mu)$.  
We see that $\mathcal L^1(X, \mathcal S, \mu)$ is vector space. 
# Properties

**Prop:** If $f$ and $g$ are integrable functions and $\alpha, \beta \in \Bbb R$, then $$\int (\alpha f + \beta g)\, d \mu = \alpha \int f\, d\mu + \beta \int g\, d\mu.$$
**Prop:** If an integrable function $f$ is non negative a.e., then $\displaystyle\int f\, d\mu \ge 0$

**Cor:** If $f$ and $g$ are integrable functions such that $f\ge g$ a.e., then $\displaystyle\int f\, d\mu \ge \displaystyle\int g \, d\mu.$

**Cor:** If $f$ and $g$ are integrable functions, then $\displaystyle\int |f+g| \, d\mu \le \int|f| \, d\mu + \int|g| \, d\mu.$
**Cor:** If $f$ is an integrable function, then $\left|\displaystyle\int f\, d\mu\right| \le \displaystyle\int|f|\, d\mu.$

**Cor:** If $f$ is an integrable function, $\alpha, \beta \in \Bbb R$ and $E$ is measurable set such that for $x\in E$, $\alpha \le f(x) \le \beta$ a.e., then $$\alpha \mu(E) \le \int_E f\, d\mu \le \beta\mu(E).$$We can generalise further to the *mean value theorem for integrals*, and If $f$ is a measurable function, $g$ is an integrable function. and $\alpha, \beta \in \Bbb R$ such that $\alpha \le f(x) \le \beta$ a.e., then there exists a real number $\gamma$ such that $\alpha \le \gamma \le \beta$, such that $$\int f|g| \, d\mu = \gamma  \int |g| \, d\mu. $$

**Def:** The *indefinite integral* of an integrable function $f$ is the set function $\nu$, defined for every measurable set $E$ by $$\nu(E) := \int_E f\, d\mu.$$
**Cor:** If an integrable function $f \ge 0$ a.e., then its indefinite integral is monotone.

**Def:** A finite valued set function $\nu$ defined on the family of all measurable sets of a measure space $(X, \mathcal S, \mu)$ is *absolutely continuous* if for every positive $\varepsilon >0$ there's a $\delta>0$, such that for every $E$ is measurable set if $\mu(E) < \delta$, then $|\nu(E)|<\varepsilon$. This condition can be written as $\nu \ll \mu,$ and it is read as $\nu$ is *dominated* by $\mu$. 

**Prop:** If $\nu$ is an absolutely continuous set function on the family of all measurable sets of a measure space $(X, \mathcal S,\mu)$, if $\mu(E) =0$ then $\nu(E) = 0$.  

**Th:** The indefinite integral of an integrable function is absolutely continuous.

**Prop:** The indefinite integral of an integrable function is countable additive. 

**Th:** If $f$ is an a.e. non negative integrable function, then a necessary and sufficient condition that $\int f\, d\mu = 0$ is that $f = 0$ a.e.

**Prop:** If $f$ is an integrable function and $E$ is a set of measure zero, then $\displaystyle\int_E f\, d\mu  =0.$

**Prop:** If $f$ is an integrable function which is positive a.e. on a measurable set $E$, and if $\displaystyle\int_E f\,d\mu = 0$, then $\mu(E) = 0$.

**Prop:** If $f$ is an integrable function such that $\displaystyle\int_F f\, d\mu =0$ for every measurable set $F$, then $f = 0$ a.e.

**Th:** If $f$ is an integrable function, then the set $N(f) = f^{-1}[\Bbb R^\times]$ has a $\sigma$-finte measure. 

**Prop:** If $f$ is integrable, then, for every $\varepsilon > 0$, $$\mu(\{x\in X \mid |f(x)| \ge \varepsilon\}) <\infty.$$
**Prop:** If $f$ is a non negative integrable function, then its indefinite integral is a finite measure on the family of all measurable sets. 

**Obs:** If $X = \Bbb N$ with $\mathcal S = P(\Bbb N)$, and $\mu(E) = |E|$. Then $f: X \to \Bbb R$ is integrable iff $\displaystyle\sum_{n <\omega} |f(n)|$ converges. 
# Sequences

**Def:** If $f$ and $g$ are integrable functions, we define the *distance between them* as $$\|f-g\|_1 := \int |f-g|\, d\mu.$$With this in mind, then the space $(\mathcal L^1(X, \mathcal S, \mu), \|\cdot\|_1)$ is a seminormed vector space. 

**Def:** A sequence $\{f_n \mid  n <\omega\}$ of integrable functions *converges in the mean*, or *mean converges*, to an integrable function $f$ if $$\|f_n- f\|_1 = \int |f_n -f| \, d\mu \to 0 \quad \text{as } n\to \infty. $$Similarly, we say that the sequence is *fundamental in the mean* or *mean fundamental*, if $$\|f_n- f_m\| \to 0 \qquad \text{as }n, m \to \infty.$$
**Th:** A mean fundamental sequence $\{f_n \mid n <\omega\}$ of integrable functions is fundamental in measure. 

**Th:** If $\{f_n \mid n <\omega\}$ is a sequence of integrable functions which converges in mean to $f$, then $\{f_n \mid n <\omega\}$ converges to $f$ in measure. 

**Th:** If $\{f_n\mid n <\omega\}$ is a mean fundamental sequence of integrable functions, and if the indefinite integral of $f_n$ is $\nu_n$, $n <\omega$, then $$\nu(E) = \lim_{n \to \infty} \nu_n(E)$$exists for every measurable sets $E$, and the set function $\nu$ is finite valued and countably additive. 

**Def:** If $\{\nu_n \mid n <\omega\}$ is a sequence of finite valued set functions defined for all measurable sets, we say that the terms of the sequence are *uniformly absolutely continuous* whenever for every $\varepsilon > 0$ there exists a $\delta>0$ such that if $\mu(E) <\delta$, then $|\nu_n(E)| < \varepsilon$ for every $n <\omega$. 

This concept reminded me to [[Equicontinuity#^3024b9|uniform equicontinuity]]. 

**Th:** If $\{f_n \mid n <\omega\}$ is a mean fundamental sequence of integrable functions, and if the indefinite integral of $f_n$ is $\nu_n$, then the set functions are uniformly absolutely continuous. 

**Th:** If $\{f_n \mid n <\omega\}$ is a mean fundamental sequence of integrable functions which converges in measure to the integrable function $f$, then $$\|f_n - f\|_1 = \int |f_n - f|\,d\mu \to 0 \qquad \text{as } n \to\infty;$$hence, to every integrable function $f$ and every positive number $\varepsilon> 0$, there corresponds an integrable simple function $g$ such that $\|f- g\| < \varepsilon$. 

**Th:** If $\{f_n \mid n <\omega\}$ is a mean fundamental sequence of integrable functions, then there exists an integrable function $f$ such that $\|f_n-f\|_1 \to 0$, and $\displaystyle\int f_n \, d\mu \to \int f\, d\mu$ as $n\to \infty$. 

Meaning that every fundamental sequence of integrable functions converges in mean to some function. Meaning that $(\mathcal L^1(X, \mathcal S, \mu), \|\cdot\|_1)$ is [[Complete Metric Spaces|complete]] seminormed space. 

We remember the notion of [[Measures#^d64f4b|continuity of measures]], in particular the notion of continuity above $\varnothing$. If $\{\nu_n \mid n <\omega\}$ is a sequence of finite valued set functions on $\mathcal E$, we shall say the terms of the sequence are *equicontinuous* from above at $\varnothing$ if, for every decreasing sequence $\{E_n \mid n <\omega\}\subseteq \mathcal E$ for which $\lim_{n \to \infty} E_n = \varnothing$, and for every $\varepsilon >0$, there exists a positive $N < \omega$ such that if $m \ge N$, then $|\nu_n(E_m)| <\varepsilon$ for every $n<\omega$.

**Th:** A sequence $\{f_n \mid n <\omega\}$ of integrable functions converges in the mean to the integrable function $f$ iff $\{f_n \mid n <\omega\}$ converges in measure to $f$ and the indefinite integrals of $\{f_n \mid n <\omega\}$ are uniformly absolutely continuous and equicontinuous from above at $\varnothing$. 

**Lemma:** If $\{f_n \mid n <\omega\}$ us a uniformly fundamental sequence of functions, integrable over a measurable set $E$ of finite measure, then the function $f$, defined as $f(x) := \lim_{n \to \infty} f_n(x)$, is integrable over $E$ and $\displaystyle \int_E| f - f_n| \, d\mu \to 0$ as $n \to \infty$.

**Th:** Let $(X, \mathcal A, \mu)$ is a totally finite measure space and a sequence $\{f_n \mid n <\omega\}$ of integrable functions converges in the mean to the integrable function $f$ iff $\{f_n \mid n <\omega\}$ converges in measure to $f$ and the indefinite integrals of $\{f_n \mid n <\omega\}$ are uniformly absolutely continuous. 

# Properties of Integrals

**Lebesgue's Dominated Convergence Theorem:** If $\{f_n\mid n <\omega\}$ is a sequence of integrable functions which converges in measure to $f$ (or else converges to $f$ a.e.), and if $g$ is integrable function such that $|f_n(x)| \le |g(x)|$ a.e., for every $n<\omega$, then $f$ is integrable and the sequence $\{f_n \mid n <\omega\}$ converges to $f$ in the mean.

**Th:** If $f$ is measurable, $g$ is integrable, and $|f|\le |g|$ a.e., then $f$ is integrable.

**Monotone Convergence Theorem:** If $\{f_n \mid n <\omega\}$ is an increasing sequence of extended real valued non negative measurable functions and if $\lim_{n\to \infty} f_n = f$ a.e., then $$\lim_{n \to \infty} \int f_n\, d\mu = \int f\, d\mu.$$
**Cor:** A measurable function is integrable iff its absolute value is integrable.

**Cor:** If $f$ is integrable and $g$ is an essentially bounded measurable function, then $fg$ is integrable. 

**Cor:** If $f$ is an essentially bounded measurable function and $E$ is measurable set of finite measure, then $f$ is integrable over $E$. 

**Fatou's Lemma:** If $\{f_n\mid n <\omega\}$ is a sequence of non negative integrable functions for which $\liminf_{n \to \infty} \int f_n \, d\mu <\infty$, then the function $\liminf_{n \to \infty} f_n(x)$ is integrable and $$\int\liminf_{n\to\infty} f\, d\mu \le \liminf_{n \to \infty}\int f_n \, d\mu.$$
