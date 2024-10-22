---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Existence of Solutions of First Order Differential Equations]], [[Second Order Linear Differential Equations]], [[nth Order Linear Differential Equations]]
### Local Existence

Let $f:D = [x_0-a, x_0+a] \times B_b(y_0) \subseteq \Bbb R\times \Bbb C ^n \to \Bbb C^n$, and satisfies a Lipschitz condition on $D$. If $M>0$, such that $\| f \| \le M$ on $D$. Then Picard iteratives $(\phi_k)$ on converge on ${I = [x_0-\alpha, x_0+\alpha]}$ with $\alpha = \min\{a, b/M\}$ to a solution of the initial value problem 

$$
y' = f(x,y) \quad y(x_0)= y_0
$$

on $I$. Additionally 

$$
\|\phi -\phi_k \| \le \frac{M}{K}\frac{(K\alpha)^{k+1}}{(k+1)!}e^{K\alpha}
$$

### Non-local Existence of Solutions

Let $S=[x_0-a, x_0+a] \times \Bbb C^n$, and $f:S \to \Bbb C^n$ be Lipschtiz continuous with constant ${K>0}$. The succesive approximations $(\phi_k)$ for the problem 

$$
y' = f(x, y) \quad y(x_0) =y_0
$$

exists on the entire interval $[x_0-a, x_0+a]$, and converge there to solution $\phi$ of the initial value problem.

**Cor:** Suppose $f:\Bbb R\times \Bbb C^n \to \Bbb C^n$ be a continuous function on the plane which satisfies the Lipschitz condtion on the strip $S_a =[-a, a] \times \Bbb R$, where $a>0$. Then every initial value problem 

$$
y' = f(x, y) \quad y(x_0) =y_0
$$

has a solution which exists for all $x$

### Approximations and uniqueness

Let $f, g$ be continuous functions on ${R= [x_0-a,x_0+a]\times[y_0-b, y_0+b]}$, and suppose $f$ satisfies the Lipschitz condition with a Lipschitz constant $K$. Let $\phi$ and $\psi$ be solutions of 

$$
y' = f(x, y) \quad y(x_0) =y_1 $$$$
y' = g(x, y) \quad y(x_0) =y_2 
$$

respectively on an interval $I$ containing $x_0$, with graphs contained in $R$. Additionally let ${\varepsilon, \delta \ge 0}$, such that ${\|f-g\| \le \varepsilon}$ on $R$, and $|y_1-y_2| \le \delta$. Then 

$$
\|\phi(x)-\psi(x)\| \le \delta e^{K|x-x_0|} + \frac{\varepsilon}{K}(e^{K|x-x_0|}-1)
$$

for all $x$ in $I$. In particular, the problem

$$
y' = f(x, y) \quad y(x_0) =y_0
$$

has at most one solution any interval containg $x_0$

### Linear sytems of equations
Consider the linear system 

$$
y'= f(x,y)
$$

where the components of $f$ are given by 

$$
f_j(x, y)= \sum_{k = 1}^n a_{jk}(x)y_k + b_j(x)
$$

and the functions $a_{jk}$, $b_j$ are continuous on an interval $I$ containg $x_0$. If $y_0$ is any vector in $\Bbb C^n$ there exists one and only one solution $\phi$ to the problem

$$
y' = f(x, y) \quad y(x_0) =y_0
$$

on $I$

### Equations of order $n$

Let $f:D=[x_0-a, x_0+a]\times B_b(y_0) \subseteq \Bbb R \times \Bbb C^n \to \Bbb C^n$ , and let $N>0$ such that ${\|f\| \le N}$ on $D$. Suppose there exists $L >0$ such that 

$$
\|f(x,y) -f(x, z) \| \le L\|y-z\|
$$

for all $(x, y), (x, z) \in D$. Then there exists a unique solution to the problem 

$$
y^{(n)} = f(x, y, y', \dots, y^{(n-1)})
$$

on the interval $I = [x_0-\alpha, x_0+\alpha]$, with $\alpha = \min\{a, b/M\}$ and $M= N+b+\|y_0\|)$ which satisfies 

$$
\phi(x_0) = \alpha_1, \quad \phi'(x_0)= \alpha_2, \quad \cdots, \phi^{(n-1)}(x_0) = \alpha_n 
$$$$
y_0 =(\alpha_1,\alpha_2, \dots, \alpha_n)
$$

### Linear $n$th order equations

Let $a_1, \dots, a_n, b: I \to \Bbb C$ continuous functions, and $I$ an interval containing $x_0$. If ${\alpha_1, \dots, \alpha_n \in \Bbb C}$ are constants, there exists a unique solution $\phi$ of the equation 

$$
y^{(n)}+a_1(x)y^{(n-1)} + \cdots +a_n(x) y = b(x)
$$

on $I$ satisfying 

$$
\phi(x_0) = \alpha_1, \quad \phi'(x_0)= \alpha_2, \quad \cdots, \phi^{(n-1)}(x_0) = \alpha_n 
$$