---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Random Variables]], [[Random Vectors]]

We say that the random variables $X$ and $Y$ are independent if the events $(X \le x )$  and $(Y \le y)$ are independent for all real values of $x$ and $y$, meaning 

$$
P[(X\le x) \cap(Y\le y)] = P(X \le x) P( Y\le y)
$$

### Discrete case

We say that the random variables $X$ and $Y$ are independent if all real values of $x$ and $y$, we have that 

$$
P(X = x, Y= y) = P(X = x) P(Y = y)
$$

### Continuous case

We say that the random variables $X$ and $Y$ are independent if all real values of $x$ and $y$, we have that 

$$
f_{X, Y}(x,y) = f_X(x) f_Y(y)
$$

# Using Random Vectors

We say that the random variables $X_1, \dots, X_n$ are independent if for any for Borels sets $A_1, \dots, A_n$ of $\Bbb R$ it follows that:
$$
P(X_1\in A_1, X_2\in A_2, \dots,X_n\in A_n) = \prod_{i = 1}^nP(X_i\in A_i)
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
P(X \in A, Y\in B) = P(X\in A)P(Y\in B)
$$
