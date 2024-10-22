---
tags:
  - OrdinaryDifferentialEquations
  - PartialDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]], [[Partial Differential Equations]]
Links: [[Second Order Linear Differential Equations]]
# ODE

The **Legendre Equation**

$$ (1-x^2) y'' -2xy'+\alpha(\alpha+1) y= 0 $$

for $\alpha \in \Bbb R$, if $\alpha \in \Bbb N$, then polynomial that is a solution is a multiple of the [[Legendre Polynomials|Legendre Polynomial]]

The **Hermite Equation**

$$ y'' -2xy' +2\alpha y=0 $$

for $\alpha \in \Bbb R$, if $\alpha \in \Bbb N$, then polynomial that is a solution is a multiple of the [[Hermite Polynomials|Hermite Polynomial]]

The **Chebyshev equation**

$$ (1-x^2) y''-xy+\alpha^2 y =0 $$

for $\alpha \in \Bbb R$, if $\alpha \in \Bbb N$, then polynomial that is a solution is a multiple of the [[Chebyshev Polynomials|Chebyshev Polynomial]]

The **Laguerre equation**
$$
xy'' +(1-x)y'+\alpha y =0
$$
for $\alpha \in \Bbb R$, , if $\alpha \in \Bbb N$, then polynomial that is a solution is a multiple of the [[Laguerre Polynomials|Laguerre Polynomial]]

The **Bessel Equation**
$$ x^2 y''+xy'+(x^2-\alpha^2)y =0$$
for $\alpha \in \Bbb C$ with $\Re (\alpha) \ge 0$, which for solutions are called the [[Bessel Functions]]

The **Airy Equation**

$$y'' -x y = 0 $$
which is a generalisation of $\sin$ and $\cos$, the solutions are called the [[Airy Functions]]

The Euler's hypergeometric differential equation:

$$ z(1-z)y'' +[c-(a+b+1)z]y'-aby =0 $$

The [[Hypergeometric Function|Hypergeometric function]] is a solution to the equation which has $3$ singular points at $0$, $1$ and $\infty$.

The [[Lotka-Volterra Predator-Prey Model]]: 
$$
\frac{dx}{dt} = \alpha x-\beta xy
$$
$$
\frac{dy}{dt} = \delta xy- \gamma y
$$
We know that $x$ represents the density of the prey population, $y$ is the density of the predator population. $\alpha$ and $\beta$ represent, respectively, the maximum prey per capita growth rate, and the effect of the presence of predators on the prey's growth rate. The parameters $\gamma$ and $\delta$ represent, respectively, the predators death rate, and the effect of the presence of prey on the predators growth rate. All parameters are positive and real

# PDE

We have the Laplace equation, being 
$$
\nabla^2 f  = 0
$$
where the $\nabla ^2$ refers to the Laplacian operator, and the functions that satisfy this are called [[Harmonic Functions|harmonic]]

[[The Heat Equation]]

[[The Wave equation]]

[[Black-Scholes equation]]