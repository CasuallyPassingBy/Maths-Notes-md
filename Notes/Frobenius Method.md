---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Series Solutions of Linear Equations on Regular Singular Points]], [[Power Series in R]]
## Second order equations with regular points

### The Process

We have the equation 

$$
L[y] =x^2 y'' + a(x)xy'+b(x) y=0
$$

we will supose that the solution is of the form, with $x >0$

$$
\phi(x) = x^r \sum_{k = 0}^\infty c_k x^k \qquad c_0\ne 0
$$

and 

$$
a(x)=\sum_{k = 0}^\infty \alpha_k x^k , \qquad b(x)=\sum_{k = 0}^\infty \beta_k x^k ,
$$

Then 

$$
x\phi'(x) = x^{r} \sum_{k = 0}^\infty (k+r)c_kx^k
$$

$$
x^2 \phi''(x) = x^r \sum_{k = 0}^\infty (k+r)(k+r-1)c_k x^k
$$

Lastly, we have to consider the series of $a(x)x\phi'(x)$ and $b(x) \phi(x)$, we get that 

$$
\begin{align*}
b(x) \phi(x) &= x^r \left(\sum_{k = 0}^\infty \beta_k  x^k\right)\left(\sum_{k = 0}^\infty c_k  x^k\right) \\
&= x^r \sum_{k =0}^\infty \tilde \beta_k x^k
\end{align*}
$$

and 

$$
\begin{align*}
a(x)x\phi'(x) &= x^r \left(\sum_{k = 0}^\infty \alpha_k  x^k\right)\left(\sum_{k = 0}^\infty (k+r)c_k  x^k\right) \\
&= x^r \sum_{k =0}^\infty \tilde \alpha_k x^k
\end{align*}
$$

where 

$$
\tilde \alpha_k = \sum_{j = 0}^k(j+r)c_j \alpha_{k-j} \qquad \tilde \beta_k = \sum_{j=0}^kc_j \beta_{k-j}
$$

Finally, we get that 

$$
L[\phi](x) = x^r \sum_{k =0}^\infty [(k+r)(k+r-1) c_k +\tilde \alpha_k + \tilde \beta_k]x^k = 0
$$

Then we must have that 

$$
[\quad]_k =(k+r)(k+r-1) c_k +\tilde \alpha_k + \tilde \beta_k =0 \qquad k =0, 1, 2, \dots
$$

If we subsitute and “simplify” (i guess), we get 

$$
[\quad]_k = [(k+r)(k+r-1) + (k+r)\alpha_0 +\beta_0]c_k + \sum_{j = 0}^{k-1}[(j+r)\alpha_{k-j} + \beta_{k-j}] c_j =0
$$

for $k =0$, we get that 

$$
r(r-1) + \alpha_0 r+ \beta_0 =0
$$

since $c_0 \ne 0$. This second degree polynomial is the ***************indicial polynomial***************, denoted as $I(r)$ or $q(r)$, and the only admissible. We can see that $I(r) = r(r-1)+ a(0) r+ b(0)$

Then 

$$
[\quad]_k = q(r+k)c_k + d_k =0
$$

where 

$$
d_k = \sum_{j = 0}^{k-1}[(j+r)\alpha_{k-j} + \beta_{k-j}] c_j
$$

If we leave $c_0$ and $r$ indeterminate for the moment, we solve the equations above, in terms of $c_0$ and $r$. These solutions we denote by $C_k(r)$, and the corresponding $d_k$ by $D_k(r)$. Thus

$$
D_1(r) = (r\alpha_1 + \beta_1)c_0, \qquad C_1(r) = -\frac{D_1(r)}{q(r+1)}
$$

and in general 

$$
D_k(r) = \sum_{j = 0}^{k-1}[(j+r)\alpha_{k-j} + \beta_{k-j}] C_j(r)
$$

$$
C_k(r) = -\frac{D_k(r)}{q(r+k)}
$$

The $C_k$ thus are determined are rational functions of $r$, and the only points where they cease to exist are the points for which $q(r+k ) =0$, for some $k =1, 2, \dots$. Only two such possible points exist. Let us define $\Phi$ by 

$$
\Phi(x, r) = c_0 x^r + x^r\sum_{k =1}^\infty C_k(r) x^k
$$

If the series converges for $0 < x < r_0$, then clearly, 

$$
L[\Phi](x, r) = c_0I(r) x^r
$$

We have that if $\phi$ defined above is a solution of $L[y] =0$, then $r$ must be a root of $I(r)$, and $c_k$  ($k \ge1$) are is determined, meaning $I(r+k) \ne 0$, for $k \ge1$, then the function ${\phi(x) = \Phi(x,r)}$ is a solution of the equation for any choice of $c_0$, provided the series converges. Let $r_1$, $r_2$ be the two roots of $I$, we have them labled such that ${\Re (r_1) \ge \Re(r_2)}$, with $C_k(r_1)$ exists for all $k =1, 2, \dots$, and letting $c_0 = C_0(r_1) = 1$, we see that the function $\phi_1$ given by 

$$
\phi_1(x) = x^{r_1}\sum_{k = 0}^\infty C_k(r_1) x^k
$$

If $r_2$ is a distinct root of $I$, and $C_k(r_2)$ exists for all $k =1, 2, \dots$, and the function $\phi_2$ given by 

$$
\phi_2(x)=  x^{r_2}\sum_{k = 0}^\infty C_k(r_2) x^k
$$

********Th:******** If we consider the equation: 

$$
x^2 y'' + a(x) xy' + b(x) y =0
$$

where $a$, $b$ have convergent power series expansions for 

$$
|x| < r_0 \qquad r_0 >0
$$

Let $r_1$, $r_2$, such that $\Re(r_1) \ge \Re(r_2)$, be roots of the indicial polynomial 

$$
I(r)  = r(r-1) +a(0) r + b(0)
$$

For $0 < |x|< r_0$, there is a solution $\phi_1$ of the form 

$$
\phi_1(x) = |x|^{r_1}\sum_{k = 0}^\infty c_k x^k
$$

where the series converges for $0<|x| < r_0$. If $r_1 - r_2$ is not nonnegative integer, there is a second solution $\phi_2$ of the form 

$$
\phi_2(x) = |x|^{r_2} \sum_{k = 0}^\infty \tilde c_k x^k
$$

where the series converges for $|x| <r_0$.

The coefficients $c_k$, $\tilde c_k$ can be obtained by subsititution of the solutions into the differential equation.

## Exceptional Cases

### $r_1 = r_2$

The solution is quite similar, to one technique we used to solve Euler Equations. We know that 

$$
L[\Phi](x, r) = c_0 I(r) x^r
$$

since $r_1$ is a double root. Then $I(r_1)=I'(r_1) =0$, then we can derive with respect to $r$, and evaluate at $r_1$, then we get that 

$$
\frac{\partial }{\partial r} L[\Phi] (x, r) = c_0 (I'(r) + I(r) \ln x) x^r
$$

when  $r= r_1$, we get that the equation above equals $0$, then showing that 

$$
\left. \frac{\partial }{\partial r} \Phi(x, r)\right|_{r = r_1}
$$

must be a solution. Doing the algebra we get that the other solution is 

$$
\phi_2 (x) = \phi_1(x) \ln x +x^{r_1} \sum_{k = 1}^\infty C'_k(r_1) x^k
$$

We know that $C_k'(r_1)$ always exist, since each $C_k(r)$ is a rational function and the denomitor is never $0$, at $r= r_1$.

### $r_1 - r_2 \in \Bbb N^+$

Let $r_1 = r_2 +m$, and $m \in \Bbb N ^+$. If $c_0$ is given,  

$$
C_1(r_2), \dots, C_{m-1}(r_2)
$$

all exists as finite numbers, but since 

$$
I(r+m) C_m(r_2) = - D_m(r_2)
$$

If we have that $D_m(r)$ has a factor of $r-r_2$, then we get that we can “cancel” out the factor. By choosing 

$$
C_0(r) = r-r_2
$$

Then we see that $D_k(r)$ is linear homogeneous in 

$$
C_0(r), \dots, C_{k-1}(r)
$$

and hence $D_k(r)$ has a factor $C_0(r) = r-r_2$. Thus $C_m(r_2)$ will exists as a finite number. Letting 

$$
\Psi(x, r) = x^r \sum_{k = 0}^\infty C_k(r) x^k
$$

We can evaluate $L$ on $\Psi$, getting that 

$$
L[\Psi](x, r) =(r-r_2)I(r) x^r
$$

If we define 

$$
\psi(x) = \Psi(x, r_2)
$$

we get that since $C_k(r_2) = 0$, for $k =0, 1, \dots, m-1$, then we see that 

$$
\psi(x) = x^{r_2 + m} \sigma(x) = x^{r_1}\sigma(x)
$$

with $\sigma(x)$  is some power series. Then we can see that $\psi$ is a constant multiple of $\phi_1$. If we differentiate, $\Psi$ with respect to $r$, we get 

$$
\frac{\partial}{ \partial r } L[\Psi] (x, r) = I(r) x^r +(r-r_2) [I'(r) +I(r) \ln x] x^r
$$

Then 

$$
\phi_2(x) = \frac{\partial \Psi}{\partial r}(x, r_2)
$$

is a solution of $L[y] = 0$. Then it has the form 

$$
\phi_2(x) = x^{r_2} \sum_{k = 0}^\infty C_k'(r_2)x^k +(\ln x)x^{r_2} \sum_{k = 0}^\infty C_k(r_2) x^k
$$

but this can be simplified as 

$$
\phi_2(x) = x^{r_2} \sum_{k = 0}^\infty C_k'(r_2)x^k + c(\ln x)\phi_1(x)
$$

********Th:******** Consider the equation 

$$
x^2 y'' +a(x) xy'+b(x) y = 0
$$

where $a$ and $b$ have power series expansions which are convergent for $|x| < r_0$, $r>0$. Let $r_1$, $r_2$, with ($\Re(r_1) \ge \Re(r_2)$) be the roots of the indicial polynomial 

$$
I(r) = r(r-1) + a(0) r + b(0)
$$

If $r_1 = r_2$ there are two linearly independent solutions $\phi_1$, $\phi_2$ for $0 <|x| < r_0$ of the form 

$$
\phi_1(x) = |x|^{r_1} \sigma_1(x), \qquad \phi_2(x) = |x|^{r_1 +1} \sigma_2(x) + (\ln x) \phi_1(x) 
$$

where $\sigma_1$, $\sigma_2$ have power expansions which are convergent for $|x| <r_0$, and $\sigma_1(0) \ne 0$. 

If $r_1 - r_2 \in \Bbb N^+$ there are two linearly independent  solutions $\phi_1$, $\phi_2$ for $0<|x| <r_0$ of the form. 

$$
\phi_1(x) = |x|^{r_1} \sigma_1(x)
$$

$$
\phi_2(x) = |x|^{r_2} \sigma_2(x) + c (\ln x) \phi_1(x)
$$

where $\sigma_1$, $\sigma_2$ have power series expansions which are convergent for 

$$
|x| < r_0, \qquad \sigma_1(0) \ne 0, \qquad \sigma_2(0) \ne 0
$$

and $c$ is a constant. It may happen that $c = 0$.