---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Random Variables]], [[Random Vectors]], [[Finite Product of Measures]], [[Pi-System]]

**Def:** Let $\{X_i\}_{i \in  I}$ be an indexed family of random variables, defined on $(\Omega, {\scr A}, \Bbb P)$ and with values in the measurable space $(S, {\scr B})$. The random variables $X_i$, $i\in I$, are called *independent* if for each choice of sets $A_i$ in $\scr B$, $i\in I$, the events $X_i^{-1}[A_i]$ are independent.

**Def:** Let $(\Omega, {\scr A}, \Bbb P)$ be a probability space and let $\{A_i\}_{i\in I}$ be an indexed family of sub-$\sigma$-algebras of $\scr A$. The $\sigma$-algebras ${\scr A}_i$, $i\in I$, are *independent* if for each choice of sets $A_i\in {\scr A}_i$, $i\in I$, the events $A_i$ are independent. 

**Obs:** If $\{X_i\}_{i \in I}$ is an indexed family of random variables on a probability space $(\Omega, {\scr A}, \Bbb P)$, then the random variables $X_i$, $i\in I$, are independent iff the $\sigma$-algebras $\sigma(X_i)$, $i\in I$, are independent. 

**Prop:** Let $(\Omega, {\scr A}, \Bbb P)$ be probability space, let $\{A_i\}_{i\in I}$ be an indexed family of independent sub-$\sigma$-algebras of $\scr A$, let $\{S_j\}_{j \in J}$ be a partition of $I$, and for each $j\in J$ let ${\scr B}_j := \sigma(\bigcup_{i \in S_j}{\scr A}_i)$. Then the $\sigma$-algebras ${\scr B}_j$ are independent. 

**Prop:** Let $(\Omega, {\scr A}, \Bbb P)$ be a probability space, let $(S, {\scr B})$ be a measurable space, let $X_1, \dots X_d$ be $S$-valued random variables on $\Omega$ and let $X$ be the $S^d$-valued random variable with components $X_1, \dots, X_d$. Let $\Bbb P_{X_1},\dots, \Bbb P_{X_d}$, and $\Bbb P_X$ be the distributions of $X_1,\dots, X_d$ and $X$, respectively. Then $X_1, \dots, X_d$ are independent iff the joint distribution $\Bbb P_X$ is the product measure $\Bbb P_{X_1}\times \dots \times \Bbb P_{X_d}$.  

### Discrete case
We say that the random variables $X$ and $Y$ are independent iff all real values of $x$ and $y$, we have that 
$$
\Bbb P(X = x, Y= y) = \Bbb P(X = x) \Bbb P(Y = y)
$$

### Continuous case
We say that the random variables $X$ and $Y$ are independent iff all real values of $x$ and $y$, we have that 
$$
f_{X, Y}(x,y) = f_X(x) f_Y(y)
$$

**Prop:** Let $(\Omega, {\scr A}, \Bbb P)$ be a probability space, and let $X_1,\dots, X_n$ be independent real-valued random variables on $(\Omega, {\scr A}, \Bbb P)$, each of which has a finite expectation. Then the product $\prod_{i= 1}^n X_i$ has a finite expectation, and $$\Bbb E\left[\prod_{i = 1}^n X_i\right] = \prod_{i = 1}^n \Bbb E[X_i]. $$

**Cor:** Let $X_1, X_2, \dots, X_n$ be independent real-valued random variabels with finite second moments, and let $S = X_1 + \dots + X_n$. Then $$\text{Var} (S) = \sum_{i = 1}^n \text{Var}(X_i) $$
We define the *[[Convolution on Locally Compact Groups|convolution]]* $\nu_1*\nu_2$ of finite measures on $\nu_1$ and $\nu_2$ on $(\Bbb R^d, \mathcal B(\Bbb R^d))$ by $$(\nu_1*\nu_2)(A) := (\nu_1\times \nu_2)(\{(x_1, x_2) \mid x_1+x_2\in A\}).$$We see that the distribution of the sum of two independent random variables is the convolition of their distributions: $\Bbb P_{X_1+X_2}=\Bbb P_{X_1}*\Bbb P_{X_2}$. 

**Prop:** Let $\nu_1$ and $\nu_2$ be probability measures on $(\Bbb R^d, \mathcal B(\Bbb R^d))$.
- The convolution $\nu_1* \nu_2$ satisfies $$(\nu_1* \nu_2)(A) = \int \nu_1(A-y)\, d\nu_2(y)=\int \nu_2(A -x)\, d\nu_1(x) $$for each $A\in \mathcal B(\Bbb R^d )$.
- If $\nu_1$ is absolutely continuous, with density $f$, then $\nu_1*\nu_2$ is absolutely continuous with density $$x\mapsto \int f(x-y)\, \nu(dy).$$
- If $\nu_1$ and $\nu_2$ are absolutely continuous, with densities $f$ and $g$, then $\nu_1*\nu_2$ is absolutely continuous with density  $$x\mapsto \int f(x-y)g(y)\, d\lambda(y) .$$

**Prop:** Let $(\Omega, {\scr A}, \Bbb P)$ be a probability space.
- Suppose that $X$ is a random variable on $(X, {\scr A}, \Bbb P)$ that is uniformly distributed on $[0, 1]$, and define a sequence $(Y_n)_{n<\omega}$ on $(\Omega, {\scr A}, \Bbb P)$ by letting $(Y_n(\omega))_{n<\omega}$ be the sequence of $0$'s and $1$'s in the binary expansion of $X(\omega)$. Then $(Y_n)_{n<\omega}$ is a sequence of independent random variables, each of which has a Bernoulli distribution with parameter $1/2$. 
- Conversely, suppose that $(Y_n)_{n<\omega}$ is a sequence of independent random variables on $(\Omega, {\scr A},\Bbb P)$, each of which has a Bernoulli distribution with parameter $1/2$. Then the random variable $X$ defined by  $$X = \sum_{n <\omega} \frac{Y_n}{2^{n+1}} $$is uniformly distributed on the interval $[0, 1]$. 

**Cor:** There is an infinite sequence of independent random variables, each of which uniformly distributed on $[0, 1]$. Such a sequence can be constructed on the probability space $([0, 1], \mathcal B([0, 1]), \lambda)$. 

**Prop:** Let $\mu$ be a probability measure on  $(\Bbb R, \mathcal B(\Bbb R))$ with cumulative distribution function $F$, and let $X$ be a random variable that is uniformly distributed on the interval $(0, 1)$, then the function $F^{-1}: (0, 1) \to \Bbb R$ defined by  $$F^{-1}(t) := \inf \{x\in\Bbb R\mid t\le F(x)\} $$is Borel measurable, and $F^{-1}\circ X$ has distribution $\mu$. 

**Cor:** Let $\mu$ be a probability distribution on $(\Bbb R, \mathcal B(\Bbb R))$. Then there is an infinite sequence of independent random variables, each of which has distribution $\mu$, Such a sequence of random variables can be constructed on the probability space $([0, 1], \mathcal B([0, 1]), \lambda)$. 

# Using Random Vectors

We say that the random variables $X_1, \dots, X_n$ are independent if for any for Borels sets $A_1, \dots, A_n$ of $\Bbb R$ it follows that:
$$
\Bbb P(X_1\in A_1, X_2\in A_2, \dots,X_n\in A_n) = \prod_{i = 1}^n\Bbb P(X_i\in A_i)
$$
We say that the random variables $X_1, \dots, X_n$ are independent if for any real numbers $x_1, \dots, x_n$ it is satisfied that:
$$
F(x_1, \dots, x_n) = \prod_{i = 1}^n F_{X_i}(x_i)
$$
We say that the random variables $X_1, \dots, X_n$ are independent with conjoined probability function $f(x_1, \dots, x_n)$ are independent if for any real numbers $x_1, \dots, x_n$ it is satisfied that
$$
f(x_1, \dots, x_n) = \prod_{i = 1}^n f_{X_i}(x_i)
$$
We say that an infinite set of random variables is independent if any finite subset of it is independent.

Let $X$ and $Y$ be independent random variables, and $g$ and $h$ be functions from $\Bbb R$ to $\Bbb R$, Borel measurable. Then the random variables $g(X)$ and $h(Y)$ are also independent.

We have two random vectors $X = (X_1, \dots, X_n)$ and $Y= (Y_1, \dots, Y_m)$ are independent if for any $A\in {\scr B}(\Bbb R^n)$ and $B\in {\scr B}(\Bbb R^m)$, it satisfies the equality
$$
\Bbb P(X \in A, Y\in B) = \Bbb P(X\in A)\Bbb P(Y\in B)
$$
