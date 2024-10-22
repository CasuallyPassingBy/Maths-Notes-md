---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[First Order Linear Differential Equations]], [[Existence and Uniqueness of Solutions to Systems of Differential Equations]]

Let $P(t)$ be a $n\times n$ matrix function, and $g$ be a vector function then $$x' = P(t) x+g(t)$$
where $x$ is an element of $\Bbb R^n$. Then this represents linear system of differential equations. If $g \equiv 0$, then it is a homogeneous system of linear differential equations if not then the system is called nonhomogeneous. 

We can expand the system of equations getting that $$
\begin{align*}
x_1' &= p_{11}(t)x_1 + \dots +p_{1n}(t) x_n + g_1(t) \\
&\vdots \\
x_n' &= p_{n1}(t)x_1 + \dots +p_{nn}(t) x_n + g_n(t)
\end{align*}$$
We say that $x = \phi(t)$ is a solution to the system if its components satisfy the system of equations above.

It is convenient to first consider the homogeneous equation $$x' = P(t) x$$I am going to use the notation $x^{(k)}$ to refer to the $k$th solution since it can interpreted as the $k$th derivative. 

**Prop:** If the vector functions $x$ and $y$ are solution to the system $x' = P(t) x$, then the linear combination $c_1 x + c_2y$ is also a solution for any constants $c_1$ and $c_2$. 

It is reasonable to expect that the system $x' = P(t) x$ of $n$ first order equations, it is sufficient to form a linear combination of $n$ properly chosen solutions. Therefore let $x^{(1)}, \dots, x^{(n)}$ be $n$ solutions of the system, and consider the matrix $$X(t) = \begin{pmatrix}
x_{11}(t) & \cdots & x_{1n}(t) \\
\vdots &&\vdots \\
x_{n1}(t) &\cdots &x_{nn}(t) 
\end{pmatrix}$$ We know that the columns of $X$ are linearly independent for a given value of $t$ iff $\det X(t) \ne 0$ for that value of $t$. The determinant is called the Wronskian of the $n$ solutions $x^{(1)}, \dots, x^{(n)}$ and is its also denoted as $W[x^{(1)}, \dots, x^{(n)}]$ that is $$W[x^{(1)}, \dots, x^{(n)}](t) = \det X(t)$$
**Th:** If the vector function $x^{(1)}, \dots, x^{(n)}$ are linearly independent solution of the system $x' = P(t) x$ for each point in the interval $t\in (\alpha, \beta)$ then each solution $x = \phi(t)$ of the system can be expressed as the linear combination of $x^{(1)}, \dots, x^{(n)}$, $$\phi(t) = \sum_{k = 1}^n c_k x_k$$in exactly one way. 

**Def:** Any set of solutions $x^{(1)}, \dots, x^{(n)}$ of $x' = P(t)x$ that is linearly independent at each point in the interval $\alpha < t <\beta$ is said to be the *fundamental set of solutions* on that interval

**Th:** If $x^{(1)}, \dots, x^{(n)}$ are solutions to $x' = P(t)x$ on the interval $\alpha < t < \beta$, then in this interval $W[x^{(1)}, \dots, x^{(n)}]$ is either identically zero or never vanishes. 

We actually we can prove that $$\frac{dW}{dt} = \text{Tr} (P(t)) W $$Meaning that as a generalisation to [[Solutions to Homogeneous nth Order Linear Differential Equations#Abel’s Identity|Abel's Identity]] we get that $$W = c \exp\left(\int \text{Tr}(P(t))\, dt \right)$$
**Th:** Let $e_1, \dots, e_n$ be the canonical basis for $\Bbb R^n$, further let $x^{(1)}, \dots, x^{(n)}$ be the solutions to $$x' = P(t)x$$ that satisfy the initial conditions $$x^{(k)}(t_0) = e_k ,\qquad k \in\{1, \dots, n\}$$where $t_0$ is a point in the interval $(\alpha, \beta)$. Then $x^{(1)}, \dots, x^{(n)}$ form a a fundamental set of solutions of the system. 

We usually study the case with [[Homogeneous Linear System of Differential Equations with Constant Coefficients|constant coefficients]] since it can be very enlightening