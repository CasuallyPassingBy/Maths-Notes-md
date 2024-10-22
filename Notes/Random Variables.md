---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Probability Measure]], [[Probability Functions for Random Variables]], [[Measuable Functions]]

A random variable is a function $X$ from $\Omega$ to the set of real numbers, meaning

$$ X: \Omega \to \Bbb R $$

Such that for any real number $x$

$$ \{ \omega \in \Omega \mid X(\omega ) \le x\} = X^{-1}[(-\infty, x]] \in \mathscr F $$

with $(\Omega, \mathscr F)$ being a measurable space. Meaning $X$ is a measurable function from $\Omega$ to $\Bbb R$

We usually abuse notation, meaning that

$$ (X \in A) = X^{-1}[A] $$

We can induce a probability measure on $(\Bbb R, \mathscr B(\Bbb R)$, by defining it as, with $A \in \mathscr B(\Bbb R)$, then

$$ P_X(A) = P(X \in A) $$

meaning we transform $A$, into a measurable set by $P$, and then applying our probability. We know that $X^{-1}[A] \in \mathscr F$, by properties of the inverse image. Meaning we have a new probability space ${(\Bbb R, \mathscr B(\Bbb R), P_X)}$.

Let $X: \Omega \to \Bbb R$, then we we denote $\sigma(X)$ as the smallest $\sigma-$algebra of subsets of $\Omega$ such that $X$ is a random variable, and we define it as 
$$
\sigma(X) :=\{X^{-1}[B] \mid B \in {\scr B}(\Bbb R)\}
$$

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
# Types
### Discrete Random Variables

The random variable $X$ is called discrete if the corresponding distribution function $F$ is a piecewise constant function. Let $x_1, x_2\dots$ the points of discontinuity of $F$. At each of this points of discontinuity we get that $P(X = x_i) = F(x_i) - F(x_i -)>0$. The function $f$ the denotes those increments it is called the probability mass function of $X$, and it is defined as 
$$
f(x)=
\begin{cases}
P(X = x_i) & x = x_1, x_2\dots \\
0 & \text{otherwise}
\end{cases}
$$
### Continuous Random Variables
A random variable $X$ is called continuous if its corresponding distribution function is continuous

A continuous random variable $X$ with a distribution function $F$ is called absolutely continuous, if there exists a nonnegative integrable function $f$ such that for every value of $x$ it is satisfied 
$$
F(x) = \int_{-\infty}^x f(u)\, du
$$
In this case $f$ is called the probability density function of $X$

### Singular Random Variables

The random variable $X$, or its corresponding distribution function $F$, is called singular if $F' =0$ almost everywhere, using [[Lebesgue Measure|Lebesgue measure]].

### Mixed Random Variables

A random variable such that is not continuous nor discrete is called mixed

# Equality of Random Variables

Let $X$ and $Y$ be random variables. Then we can just simply say that $X = Y$ if for every $\omega\in \Omega$ it follows that $X(\omega) = Y(\omega)$. This is too restrictive, and we can make two weaker versions. 

We say that two random variable $X$ and $Y$ are equal almost surely, denoted as $X \stackrel{\text{a.s.}}{=} Y$, if $P(X = Y) =1$ or $P(X\ne Y) = 0$. Apparently this is basically the same as equality in Probability theory. 

We say that two random variable $X$ and $Y$ are equal ins distribution, denoted as $X \stackrel{d}{=} Y$  if they have the same distribution functions: $F_X(x) = F_Y(x)$ for all $x\in \Bbb R$. 
