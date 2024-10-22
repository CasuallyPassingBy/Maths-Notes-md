---
tags:
  - SpecialFunctions
---
Subjects: [[Special Functions]]

The integral with $\Re(z_1) , \Re(z_2) >0$

$$ \text{B}(z_1, z_2) = \int_0^1 t^{z_1-1}(1-t)^{z_2-1}\, dt $$

We have that $\text{B}(z_1, z_2)= \text{B}(z_2, z_1)$, we also have the equivalente integral definition

$$ \text{B}(z_1, z_2)=2\int_0^{\pi/2}(\sin\theta)^{2z_1-1}(\cos\theta)^{2z_2-1} \, d\theta $$

it has a relationship with the [[Gamma Function|Gamma function]] as

$$ \text{B}(z_1, z_2) = \frac{\Gamma(z_1)\Gamma(z_2)}{\Gamma(z_1+z_2)} $$

We have a simplification

$$ \int_0^1 x^p(1-x^m)^q \, dx = \frac{1}{m}\text{B}\left(\frac{p+1}{m}, q+1\right) $$

Also, the integrals

$$ \int_0^{\frac{\pi}{2}}(\sin \theta)^n \, d\theta = \int_0^{\frac{\pi}{2}}(\cos \theta)^n \, d\theta = \frac{1}{2} \text{B}\left(\frac{n+1}{2}, \frac{1}{2}\right) $$

We can look at special values of $\text{B}(a,b)$:

- $\text{B}(a,1) = 1/a$
- $\text{B}(a+1, b) = \dfrac{a}{b}\text{B}(a,b+1)$
- $\text{B}(a+1, b) = \dfrac{a}{a+b}\text{B}(a,b)$

### Incomplete Beta Function

We can define the incomplete beta function, as the integral

$$ \text{B}(x;a,b) = \int_0^x t^{a-1}(1-t)^{b-1}\, dt $$

we have that $\text{B}(1;a,b) = \text{B}(a,b)$.

We can define, the ****************regularized incomplete beta function****************, or _******************regularized beta function******************_ as

$$ I_x(a,b) = \frac{\text{B}(x;a,b)}{\text{B}(a,b)} $$

This has several important properties. It is used as the cdf of a random variable with a [[Beta Distribution|beta distribution]], and is related the cdf $F(x;n,p)$ of a random variable $X$ following a binomial distribution with a probability of a single success $p$ and number of Bernulliy trials

$$ F(k; n,p) = P(X \le k) = I_{1-p}(n-k,k+1) = 1-I_p(k+1,n-k) $$

Properties

- $I_0(a,b) =0$
- $I_1(a,b) =1$
- $I_x(a,1) = x^a$
- $I_x(1,b) = 1-(1-x)^b$
- $I_x(a,b) = 1-I_{1-x}(b,a)$
