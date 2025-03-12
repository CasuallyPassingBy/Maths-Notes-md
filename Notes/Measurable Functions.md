---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measure Spaces and Measurable Spaces]], [[Rings and Algebras of Sets]]

**Def:** Suppose that $(X, \mathcal S)$ is a measurable space. For every $f: X \to \Bbb R$, we shall write $N(f) := f^{-1}[\Bbb R\setminus\{0\}]$; if a real valued function such that, for every Borel subset $M$ of the real line the set $N(f) \cap f^{-1}[M]$ is measurable, then $f$ is called a *measurable function.*

If $f$ is a measurable function on $X$ and if we take $M = \Bbb R$, then it follows that $N(f)$ is a measurable set. Hence if $E$ is measurable subset of $X$ and if $M$ is Borel subset of the real line, then it follows that $E \cap f^{-1}[M]$ is measurable. 

In other words, if we say that real valued function defined on a measurable set $E$ is to be called a *measurable on $E$* whenever $E \cap f^{-1}[M]$ is measurable for every set $M$, then we have proved that a measurable function is measurable on every measurable set. If in particular, the entire space $X$ happens to measurable, measurable function is one whose inverse maps the sets of one prescribed $\sigma$-ring into the sets of another prescribed $\sigma$-ring. 

It is clear that the concept of measurabilty for a function depends on the $\sigma$-ring $\cal S$ and therefore, we shall say that a function is measurable with respect to $\cal S$, or, more concisely that is measurable ($\cal S$).

If in particular $X = \Bbb R$, and $\mathcal B(\Bbb R)$ and $\overline{\mathcal B(\Bbb R)}$ are the Borel sets and the family if Lebesgue measurable sets respectively, then we shall call a function measurable with respect to $\mathcal B(\Bbb R)$ a *Borel measurable function*, and a function that is measurable with respect to $\overline{\mathcal B(\Bbb R)}$ a *Lebesgue measurable function.*

This concept is quite close to [[Continuous Functions and Homeomorphims|topological continuity]].

We need to extend the concept of measurability for extended real functions also. We define the concept by making the convention that one-point sets $\{\infty\}$ and $\{-\infty\}$ of the extended real line are to be regarded as Borel sets. Accordingly a possibly infinite valued function $f$ is measurable, if, for every Borel set $M$, each of the three sets $$f^{-1}\{\infty\}, \qquad, f^{-1}\{-\infty\}, \qquad N(f)\cap f^{-1}[M]$$is measurable. 

**Th:** Let $f$ be a real valued function on a measurable space $(X, \mathcal S)$. The following statements are equivalent:
- $f$ is measurable.
- For every $c \in \Bbb R$, the set $N(f) = \{x \mid f(x) < c\} = N(f) \cap f^{-1}[(-\infty, c)].$
- For every $c \in \Bbb R$, the set $N(f) = \{x \mid f(x) \le c\} = N(f) \cap f^{-1}[(-\infty, c]].$
- For every $c \in \Bbb R$, the set $N(f) = \{x \mid f(x) > c\} = N(f) \cap f^{-1}[(c, \infty)].$
- For every $c \in \Bbb R$, the set $N(f) = \{x \mid f(x) \ge c\} = N(f) \cap f^{-1}[[c, \infty)].$

**Cor:** Let $f$ be a real valued function on a measurable space $(X, \mathcal S)$, and $D\subseteq \Bbb R$ dense. The following statements are equivalent:
- $f$ is measurable.
- For every $c \in D$, the set $N(f) = \{x \mid f(x) < c\} = N(f) \cap f^{-1}[(-\infty, c)].$
- For every $c \in D$, the set $N(f) = \{x \mid f(x) \le c\} = N(f) \cap f^{-1}[(-\infty, c]].$
- For every $c \in D$, the set $N(f) = \{x \mid f(x) > c\} = N(f) \cap f^{-1}[(c, \infty)].$
- For every $c \in D$, the set $N(f) = \{x \mid f(x) \ge c\} = N(f) \cap f^{-1}[[c, \infty)].$

**Prop:** If $f$ is a measurable function and $c\in \Bbb R$, then $cf$ is measurable. 

**Prop:** Let $E \subseteq X$ and $(X,\mathcal S)$ is measurable space. $E$ is measurable iff $\chi_E$ is measurable.

**Prop:** A nonzero constant function is measurable iff $X$ is measurable.

**Prop:** If $f: \Bbb R \to \Bbb R$ is increasing then $f$ is Borel measurable.

**Prop:** Let $(X, \tau)$ be a topological space. If $f: X \to \Bbb R$ is continuous, then $f$ is Borel measurable. 

**Prop:** Suppose that $f$ is a real valued function on a measurable space $(X, \mathcal S)$, and for every $t\in \Bbb R$, write $B(t) = \{x\mid f(x) \le t\}$. Then 
- $s< t$ implies $B(s) \subseteq B(t)$.
- $\bigcup_{t\in \Bbb R} B(t) = X$ and $\bigcap_{t\in \Bbb R} B(t) = \varnothing$.
- $\bigcap_{s < t} B(t) = B(s)$.
Conversely, if $\{B(t)\mid t\in \Bbb R\}$ with the properties above, then there exists a unique, finite, real valued function $f$ such that $\{x\mid f(x) \le t\} = B(t)$. The unique function is $f(x) = \inf\{t\mid x\in B(t)\}$. 

**Obs:** If $f$ is a measurable function on a totally finite measure space $(X, \mathcal S, \mu)$ and if, for every Borel set $M$ on the extended real line, we write $\nu(M) = \mu(f^{-1}[M])$, then the $\nu$ measure on the family of Borel sets, and it is commonly referred as the *pushforward measure* or the *image measure* of $\mu$ under the function $f$. The pushforward measure is often denoted as $f_*\mu.$

**Def:** If $f$ is finite valued, then the function $g: \Bbb R \to \Bbb R$, defined by $g(t) = \mu(\{x\mid f(x)< t\})$, then $g$ is called the *distribution* of $f$. 

**Prop:** If $f$ is finite valued, then the $g$ is the distribution of $f$, is increasing, continuous on the left, and such that $g(-\infty) = 0$ and $g(\infty) = \mu(X)$.

**Prop:** Let $f$ be finite valued, and $g$ is the distribution of $f$. If $g$ is continuous, then the [[Lebesgue-Stieltjes Measures|Lebesgue-Stieltjes measure]] $\mu_g$ is the completion of $\nu$. 

**Prop:** If $E$ is a measurable set and its characteristic function $\chi_E$, then $(\chi_{E})_* \mu(M) = \chi_M(1)\mu(E)+ \chi_M(0)\mu(X\setminus E)$

**Def:** A complex valued function $f: X \to \Bbb C$ is measurable if $\Re(f), \Im(f): X \to \Bbb R$ are measurable.

**Prop:** A complex valued function $f$ is measurable iff for every open set $M$ in the complex plane, the set $N(f)\cap f^{-1}[M]$ is measurable. 

# Combinations of Measurable Functions

**Th:** If $f$ and $g$ are extended real measurable functions on a measurable space $(X, ¸\mathcal S)$, and if $c \in\Bbb R$, then each of the three sets: $$A = \{x\mid f(x) < g(x) + c\}, \qquad B = \{x\mid f(x) \le g(x) + c\}, \qquad C = \{x\mid f(x) = g(x) + c\},$$has measurable intersection with every measurable set. 

**Th:** If $\phi$ is an extended real valued Borel measurable function on the extended real line such that $\phi(0) )= 0$, and if $f$ is an extended real valued measurable function on a measurable space $X$, then the function $\tilde f$, defined by $\tilde f(x) := \phi(f(x))$, is a measurable function on $X$. 

**Obs:** For each $\alpha > 0$, the function $\phi(x) = |x|^\alpha$, is Borel measurable. 

**Cor:** If $\phi$ is an extended real valued Borel measurable function on the extended real line, if $f$ is an extended real valued measurable function on a measurable space $X$ with $X$ is measurable, then the function $\tilde f$, defined by $\tilde f(x) := \phi(f(x))$, is a measurable function on $X$. 

**Cor:** Let $f$ be an extended real valued measurable function on a measurable space $X$, and $\alpha > 0$, then $|f|^{\alpha}$ is measurable.

**Prop:** If $f$ and $g$ are extended real valued measurable functions on a measurable space $X$, then so also are $f+g$ and $fg$. 

**Cor:** If $f$ and $g$ are extended real valued measurable functions on a measurable space $X$, then so also are $\min\{f, g\}$ and $\max\{f, g\}$. 

**Def:** Let $f$ is an extended real valued measurable function on a measurable space $X$, then we define the functions $f^+:= \max\{f, 0\}$ and $f^- := - \min\{f, 0\}$ are called the *positive part* and the *negative* part of $f$, respectively. Both are measurable.

