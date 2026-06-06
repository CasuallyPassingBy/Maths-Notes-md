---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Probability Measure]], [[Probability Functions for Random Variables]], [[Measurable Functions]]

**Def:** A *real-valued random variable* on a probability space $(\Omega.{\scr A}, \Bbb P)$ is an $\scr A$-measurable function from $\Omega$ to $\Bbb R$. Such a variable represents a numerical observation or measurment whose value depends on the outcome of the random experiments represented by $(\Omega.{\scr A}, \Bbb P)$. More generally, a *random variable* with values in a measurable space $(S, {\scr B})$ is a measurable function from $(\Omega.{\scr A}, \Bbb P)$ to $(S, {\scr B})$. 

**Def:** Let $X$ be a random variable with values in $(S, {\scr B})$. The *distribution*of $X$ is the measure $X_*\Bbb P$ defined on $(S, {\scr B})$ by $X_*\Bbb P(A) := P(X^{-1}[A])$. We often write $\Bbb P_X$ for the distribution of a random variable $X$. If $X_1, \dots, X_d$ are $(S, {\scr B})$-valued random variables on $(\Omega, {\scr A}, \Bbb P)$, then the formula $X(\omega) = (X_1(\omega), \dots, X_d(\omega))$ defines an $S^d$-valued random variable $X$; the distribution of $X$ is called the *joint distribution* of $X_1,\dots, X_d$. 

**Obs:** Let $X$ be a random variable with values in $(S, {\scr B})$. We see that $(S, {\scr B}, \Bbb P_X)$ is a probability space.

**Def:** Let $X: \Omega \to \Bbb R$, then we we denote $\sigma(X)$ as the smallest $\sigma$-algebra of subsets of $\Omega$ such that $X$ is a random variable, and we define it as 
$$ \sigma(X) :=\sigma(\{X^{-1}[B] \mid B \in {\scr B}(\Bbb R)\}). $$ Let $\{X_i\}_{i \in I}$ be an indexed family of random variables on a probability space $(\Omega, {\scr A}, \Bbb P)$. Then $\sigma(X_i, i\in I)$ is the smallest $\sigma$-algebra on $\Omega$ that makes all of these variables measurable. Likewise. if $\{X_n\}_{n<\omega}$ is a countable collection of random variables on $(\Omega, {\scr A}, \Bbb P)$, then we often write $\sigma(X_1, X_2,\dots)$ for the smallest $\sigma$-algebra on $\Omega$ that makes each $X_n$ measurable.

The constant function $X = c$ is a random variable

If $X$ is a random variable and $c$ is a constant, then $cX$ is also a random variable

If $X$ and $Y$ are random variables, then so is $X+Y$, $XY$ and if $Y \ne 0$ so is $X/Y$

If $X$ and $Y$ are random variables, then so is $\max\{X, Y\}$, $\min\{X, Y\}$

If $X$ is a random variable, then so is $|X|$

Let $X_0, X_1, X_2,\dots$ be an infinite sequence of random variables such that for every $\omega \in \Omega$, the numbers
$$
\sup_{n \in \Bbb N} X_n(\omega) \qquad\text{ and }\qquad \inf_{n \in \Bbb N} X_n(\omega)
$$
are finite. Then the functions $\sup\limits_{n \in \Bbb N}X_n$ and $\inf\limits_{n \in \Bbb N}X_n$ are random variables

Let $X_0, X_1, X_2,\dots$ be an infinite sequence of random variables such that for every $\omega \in \Omega$, the numbers
$$
\limsup_{n \in \Bbb N} X_n(\omega) \qquad\text{ and }\qquad \liminf_{n \in \Bbb N} X_n(\omega)
$$
are finite. Then the functions $\limsup\limits_{n \to \infty}X_n$ and $\liminf\limits_{n \to \infty}X_n$ are random variables


Let $X_0, X_1, X_2,\dots$ be an infinite sequence of random variables such that for every $\omega \in \Omega$, the limit $\lim\limits_{n \to\infty} X_n(\omega)$ exists and it is finite. Then the function $\lim\limits_{n \to \infty} X_n$ is a random variable.

Let $X$ be a random variable, and let $g: \Bbb R \to \Bbb R$ be a Borel measurable function, then $g(X)$ is a random variable. 

**Def:** Let $X$ be a real-valued random variable. Since $X$ induces a finite measure on $(\Bbb R, \mathcal B(\Bbb R))$, then if we define the function $F_X: \Bbb R\to \Bbb R$ by $$F_X(x) :=\Bbb P_X((-\infty, x]),  $$then $F_X$ is  bounded, non decreasing, and right-continuous and satisfies $\lim_{x\to -\infty} F_X(x) = 0$. We call $F_X$ the *cumulative distribution function* of $X$ or just the *distribution function* of $X$. 

# Types
### Discrete Random Variables
A real random variable $X$ is called *discrete* if its distribution is [[Measures#^dba93d|discrete]]. 

In other words, the random variable $X$ is called discrete if the corresponding distribution function $F$ is a piecewise constant function. Let $x_1, x_2\dots$ the points of discontinuity of $F$. At each of this points of discontinuity we get that $\Bbb P(X = x_i) = F(x_i) - F(x_i -)>0$. The function $f$ the denotes those increments it is called the probability mass function of $X$, and it is defined as 
$$
f(x)=
\begin{cases}
\Bbb P(X = x_i) & x = x_1, x_2\dots \\
0 & \text{otherwise}
\end{cases}
$$

### Continuous Random Variables
A real-random variable $X$ is *continuous* if its distribution is absolutely continuous with respect to the Lebesgue measure, $\Bbb P_X \ll \lambda$.

$X$ is a continuous real-random variable, then we can calculate the Radon-Nykodim derivative of $\Bbb P_X$ with respect to $\lambda$, let  $$f_X(x) := \frac{d\Bbb P_X}{d\lambda}(x).$$We see that  $$\Bbb P_X(A) = \int_A \, d\Bbb P_X = \int_A f_X\, d\lambda $$which is an integral we know how to do. In this context we see why $f_X$ is called the *probability density function* of $X$.  

In other words, a continuous random variable $X$ with a distribution function $F_X$ is called absolutely continuous, if there exists a nonnegative integrable function $f_X$ such that for every value of $x$ it is satisfied 
$$
F_X(x) = \int_{-\infty}^x f_X(u)\, du
$$
In this case $f_X$ is called the probability density function of $X$. 

### [[Absolute Continuity of Measures#Singularity|Singular]] Random Variables
The random variable $X$, or its corresponding distribution $\Bbb P_X$ is [[Absolute Continuity of Measures#Singularity|singular]] with respect [[Lebesgue Measure|Lebesgue measure]].

### Mixed Random Variables
A random variable such that is not continuous nor discrete is called mixed

# Equality of Random Variables

Let $X$ and $Y$ be random variables. Then we can just simply say that $X = Y$ if for every $\omega\in \Omega$ it follows that $X(\omega) = Y(\omega)$. This is too restrictive, and we can make two weaker versions. 

We say that two random variable $X$ and $Y$ are equal almost surely, denoted as $X \stackrel{\text{a.s.}}{=} Y$, if $\Bbb P(X = Y) =1$ or $\Bbb P(X\ne Y) = 0$. Apparently this is basically the same as equality in Probability theory. 

We say that two random variable $X$ and $Y$ are equal ins distribution, denoted as $X \stackrel{d}{=} Y$  if they have the same distribution functions: $F_X(x) = F_Y(x)$ for all $x\in \Bbb R$. 
