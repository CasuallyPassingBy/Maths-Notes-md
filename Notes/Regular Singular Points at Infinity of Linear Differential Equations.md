---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Series Solutions of Linear Equations on Regular Singular Points]]
We sometimes want to investigate the solutions to an equation 

$$
L[y] = y''+ a(x) y' +b(x) y=0
$$

for large values of $|x|$. We make a substitution $x = 1/t$ and study the resulting equation near ${t=0}$. If $\phi$ is a solution for $|x| >r_0$ for some $r_0 >0$, let 

$$
\tilde \phi(t) = \phi\left(\frac{1}{t}\right), \qquad \tilde a(t) = a\left(\frac{1}{t}\right), \qquad \tilde b(t) = b\left(\frac{1}{t}\right)
$$

we have that after doing the algebre and calculus, (

$$
\frac{d^2 \phi}{dx^2}\left(\frac{1}{t}\right) + a\left(\frac{1}{t}\right)\frac{d \phi}{dx}\left(\frac{1}{t}\right)+b\left(\frac{1}{t}\right)\phi\left(\frac{1}{t}\right) =0
$$

we have that 

$$
t^4\tilde \phi''(t) +[2t^3-t^2\tilde a(t) ]\tilde\phi'(t)+\tilde b(t) \phi(t)  =0
$$

Then we define the new differential equation 

$$
\tilde L[y] = t^4y'' + [2t^3-t^2\tilde a(t)] y'+ \tilde b(t) y =0
$$

We say that ******infinity is a regular singular point****** of the originial equation if, $0$ is a regular singular point of the equation above, we can rewrite it to get: 

$$
t^2y''+\left(2-\frac{\tilde a(t)}{t}\right) ty'+ \frac{b(t)}{t^2}y =0
$$

$\tilde L[y] =0$ has a regular singular point at $0$, iff $\tilde a(t) /t$ and $\tilde b(t) /t^2$ are analytic at $t =0$. Then 

$$
\tilde a(t) = t \sum_{k = 0}^\infty \alpha_k t^k, \qquad\tilde b(t) = t \sum_{k = 0}^\infty \beta_k t^k
$$

where the series converges for $|t| < 1/r_0$, for $r_0>0$. We know the form of $a(x)$  and $b(x)$

$$
a(x) = \frac{1}{x}\sum_{k = 0}^\infty \frac{\alpha_k}{x^k}, \qquad 
b(x) = \frac{1}{x^2}\sum_{k = 0}^\infty \frac{\beta_k}{x^k}
$$

where these series converges for $|x| >r_0$. Thus infinity is a regular singular point for the original equation can be rewritten in the form 

$$
x^2 y'' +a(x)x y'+b(x)y =0
$$

where $a$, $b$ have convergent power series expansions in powers of $1/x$ for $|x| >r_0$ for some ${r_0 >0}$

This process is similar to what's is done studying [[Isolated Singularities#^1f45b1|isolated singularities at infinity]] in complex analysis