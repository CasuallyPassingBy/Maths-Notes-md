---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measure Spaces and Measurable Spaces]], [[Measurable Functions]]

**Def:** A simple function $f = \sum_{k = 1}^n a_k \chi_{E_k}$ on a measure space $(X, \mathcal S, \mu)$ is *integrable* if $\mu(E_k) <\infty$ for every $k \in \{1, \dots, n\}$ which $a_k \ne 0$. the *integral*, is $$\int f(x) \, d\mu(x) = \int f \, d\mu := \sum_{k = 1}^n a_k \mu(E_k).$$
We see that the value of is independent of the representation of $f$ and is therefore unambiguously defined. 

**Obs:** We see that if $f, g: X \to \Bbb R$ are integrable simple functions, and $\lambda \in \Bbb R$, then the following are true:
- $|f|$ is integrable.
- $\lambda f$ is integrable.
- $f+g$ is integrable.

**Prop:** If one of two simple functions is integrable, then so is their product, 

**Def:** If $E$ is a measurable set and $f$ is an integrable simple function, then it is easy to see that the function $\chi_E f$ is an integrable simple function; we also define the *integral of $f$ over $E$* by: $$\int_E f\, d\mu := \int \chi_E f \, d\mu.$$
**Prop:** If $f$ and $g$ are integrable simple functions and $\alpha, \beta \in \Bbb R$, then $$\int (\alpha f + \beta g)\, d \mu = \alpha \int f\, d\mu + \beta \int g\, d\mu.$$
**Prop:** If an integrable simple function $f$ is non negative a.e., then $$\int f\, d\mu \ge 0$$
**Cor:** If $f$ and $g$ are integrable simple functions such that $f\ge g$ a.e., then $$\int f\, d\mu \ge \int g \, d\mu.$$
**Cor:** If $f$ and $g$ are integrable simple functions, then $$\int |f+g| \, d\mu \ge \int|f| \, d\mu + \int|g| \, d\mu.$$
**Cor:** If $f$ is an integrable simple function, then $$\left|\int f\, d\mu\right| \le \int|f|\, d\mu.$$
**Cor:** If $f$ is an integrable simple function, $\alpha, \beta \in \Bbb R$ and $E$ is measurable set such that for $x\in E$, $\alpha \le f(x) \le \beta$, then $$\alpha \mu(E) \le \int_E f\, d\mu \le \beta\mu(E).$$
**Def:** The *indefinite integral* of an integrable simple function $f$ is the set function $\nu$, defined for every measurable set $E$ by $$\nu(E) := \int_E f\, d\mu.$$
**Cor:** If an integrable simple function $f \ge 0$ a.e., then its indefinite integral is monotone.

**Def:** A finite valued set function $\nu$ defined on the family of all measurable sets of a measure space $(X, \mathcal S, \mu)$ is *absolutely continuous* if for every positive $\varepsilon >0$ there's a $\delta>0$, such that for every $E$ is measurable set if $\mu(E) < \delta$, then $|\nu(E)|<\varepsilon$. 

**Prop:** If $\nu$ is an absolutely continuous set function on the family of all measurable sets of a measure space $(X, \mathcal S,\mu)$, if $\mu(E) =0$ then $\nu(E) = 0$.  

**Th:** The indefinite integral of an integrable simple function is absolutely continuous.

**Prop:** The indefinite integral of an integrable simple function is countable additive. 

# Sequences

**Def:** If $f$ and $g$ are integrable simple functions, we define the *distance between them* as $$d(f, g) := \int |f-g|\, d\mu$$
**Def:** A sequence $\{f_n \mid  n <\omega\}$ of integrable simple functions is *fundamental in the mean* or *mean fundamental*, if $$d(f_n, f_m) \to 0 \qquad \text{as }n, m \to \infty.$$
**Th:** A mean fundamental sequence $\{f_n \mid n <\omega\}$ of integrable simple functions is fundamental in measure. 

**Th:** If $\{f_n\mid n <\omega\}$ is a mean fundamental sequence of integrable simple functions, and if the indefinite integral of $f_n$ is $\nu_n$, $n <\omega$, then $$\nu(E) = \lim_{n \to \infty} \nu_n(E)$$exists for every measurable sets $E$, and the set function $\nu$ is finite valued and countably additive. 

**Def:** If $\{\nu_n \mid n <\omega\}$ is a sequence of finite valued set functions defined for all measurable sets, we say that the terms of the sequence are *uniformly absolutely continuous* whenever for every $\varepsilon > 0$ there exists a $\delta>0$ such that if $\mu(E) <\delta$, then $|\nu_n(E)| < \varepsilon$ for every $n <\omega$. 

This concept reminded me to [[Equicontinuity#^3024b9|uniform equicontinuity]]. 

**Th:** If $\{f_n \mid n <\omega\}$ is a mean fundamental sequence of integrable simple functions, and if the indefinite integral of $f_n$ is $\nu_n$, then the set functions are uniformly absolutely continuous. 

**Th:** If $\{f_n \mid n<\omega\}$ and $\{g_n \mid n <\omega\}$ are mean fundamental sequences of integrable simple functions which converge in measure to the same function $f$, if the indefinite integrals of $f_n$ and $g_n$ are $\nu_n$ and $\lambda_n$, respectively, and if, for every measurable set $E$, $$\nu(E) := \lim_{n \to \infty} \nu_n(E) \qquad \lambda(E) :=\lim_{n \to \infty} \lambda_n(E),$$then the set functions $\nu$ and $\lambda$ are identical.  ^3830db