---
tags:
  - FourierAnalysis
  - PartialDifferentialEquations
---
Subjects: [[Fourier Analysis]], [[Partial Differential Equations]]
Links: [[The Heat Equation]], [[Laplace's Equation on the disk]], [[The Heat Equation on the Circle]], [[The Heat Equation on the Real line]]


Another application of the [[Poisson Summation Formula]] and the the [[Jacobi Theta function]] is the time-dependent heat equation on the circle. A solution to the initial value problem $$\begin{align*} \frac{\partial u}{\partial t} &= {\partial^2 u}{\partial x^2}\\
u(x, 0) &= f(x) \end{align*}$$where $f$ is a periodic function of period $1$. The solution we arrived at was $$ u(x, t) (f*H_t)(x)$$where $H_t(x)$ is the heat kernel in the circle, that is $$ H_t(x) = \sum_{n = -\infty}^\infty e^{-4\pi^2 n^2 t}{e^{2\pi i nx}} $$
We see that the definition of the Jacobi theta function, gives us that $\vartheta_{00}(z; 4\pi i t) = H_t(x)$. We also have that the heat equation on $\Bbb R$ gave rise to the heat kernel, $$\mathcal H_t(x) = \frac1{(4\pi t)^{1/2}}e^{-x^2/4t}\qquad \text{and} \quad \hat{\mathcal H_t}(\omega) = e^{-4\pi^2t\omega^2}$$where $\hat{\mathcal H_t}(\omega) = e^{-4\pi^2 \omega t}$. 

**Th:** The heat kernel on the circle is the periodization of the heat kernel on the real line: $$H_t(x) = \sum_{n =-\infty}^\infty \mathcal H_t(x+n)$$**Cor:** The kernel $H_t(x)$ is a good kernel as $t \to 0$. 

We have a similar relation between the two Poisson kernels:

[[Laplace's Equation on the disk]], [[Laplace's Equation in the upper half-plane]]

**Th:** let $r = e^{-2\pi y}$, then $$P_r(2\pi x) = \sum_{n = -\infty} ^\infty \mathcal P_y(x+n)$$
with $$P_r(\theta) =\sum_{n =-\infty}^\infty r^{|n|}e^{in\theta} \qquad 0\le r <1, 0 \le\theta \le 2\pi$$and $$ \mathcal P_y(x) = \frac1{\pi} \frac{y}{x^2+y^2} \qquad x\in\Bbb R, y>0$$