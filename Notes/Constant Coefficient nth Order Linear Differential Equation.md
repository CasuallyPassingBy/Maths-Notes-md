---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[nth Order Linear Differential Equations]]
# Homogeneous Equations with Constant Coefficients
Consider the $n$th order linear homogeneous differential equation

$$ L[y] = \sum_{k = 0}^n a_k y^{(k)} =0 $$

We look at $y = e^{\lambda t}$, then

$$ L[e^{\lambda t} ] = e^{\lambda t} \sum_{k = 0}^n a_k \lambda^k = 0 $$

$L$ is a special kind of operator. It is a polynomial differential operator.

**********Def:********** The characteristic polinomial of $L$ is the the polinomial $p_L(\lambda) = \sum a_k \lambda^k$ as seen above. Then the zeros of $p_L$ are the coefficients for the exponent, and $p_L (D) = L$.

We can write the characteristic polinimial as

$$ p_L(\lambda) = a_n \prod_{k = 1}^m(\lambda-\lambda_k)^{r_k} $$

where $\sum_{k = 1}^m r_k = n$, and for any $\lambda_k \in \Bbb C$. This tells us that we can decompose $L$ into simple linear differential operators. Meaning

$$ L = \sum_{k = 0}^n a_k D^k = a_n \prod_{k = 1}^m (D-\lambda_k )^{r_k} $$

by the decomposition we made. This decomposition is valid since it will comute.

### Exponential Shift Theorem

Let $p \in \Bbb C[x]$, and, then $p(D)$ is a polynomial differential operator. Then

$$ p(D)(e^{\lambda t} f(t)) = e^{\lambda t} p(D+\lambda) f(t) $$

Then using linear algebra and the fact that $\dim (N(L)) = n$. Then we only need to find the basis for $N((D-\lambda_k)^{r_k})$, since each has dimension $r_k$.

### Method of Annihilators

Then we can get that the solutions to

$$ (D-\lambda)^r y =0 $$

in general. We get that the basis is of the form $\{e^{\lambda t}, te^{\lambda t}, t^2e^{\lambda t}, \dots, t^{r-1} e^{\lambda t}\}$. Then the basis for $N(L)$ is the union of all of this basis. Then $y$, that satisfies the differential equation ${L[y] =0}$ is of the form

$$ y = \sum_{k = 1}^m \left(e^{\lambda_k}\sum_{j = 1}^{r_k} c_{j, k} t^{j-1}\right) $$
# Nonhomogeneous Equation

### Method of Undetermined Coeffcients

refer to the [[Method of Undetermined Coefficients for Linear Differential Equations|table]]. It is a lot of algebra.

### Method of Annihilators for Nonhomogeneous equations

Let $L(D)$ be a differential operator with constant coefficients, and the nonhomogeneous equation is

$$ L(D)[y] = g $$

The restriction we need to add is that $g$ is only a is a sum or product of exponential, polynomial or synusiodal terms. Then we can find a differential operator $H(D)$ with constant coefficients such that $H(D)[g] = 0$. Then we can solve the equation

$$ H(D) L(D) [y] =0 $$

We can ignore the terms of the solution that solve $L(D)[y] =0$, the remaining terms form a particular solution of $L(D)[y] = g$.