---
tags:
  - FourierAnalysis
  - PartialDifferentialEquations
---
Subjects: [[Fourier Analysis]], [[Partial Differential Equations]]
Links: [[Harmonic Functions]], [[2D Harmonic Functions]], [[Fourier Transform in R]], [[Convolution#Rapidly Decreasing Functions|Convolution for Rapidly Decreasing Functions]]

The equation we are concerned with is $$\Delta u = \frac{\partial^2 u}{\partial x^2} +\frac{\partial^2 u}{\partial y^2} = 0$$
in the upper half-plane $\Bbb R^2_+\{(x, y) \mid y >0\}$. The boundary condition we require is $u(x, 0) = f(x)$. The kernel that solves this problem is called the *Poisson kernel* for the upper half-plane, and is given by $$\mathcal P_y(x) = \frac1{\pi} \frac{y}{x^2+y^2} \qquad x\in\Bbb R, y>0$$
This is the analogue of the Poisson kernel used in the [[Laplace's Equation on the disk]]. We see that $\mathcal P_y$ is a only of moderate decrease as a function of $x$. 

We proceed as in the case of the time-dependent heat equation, by taking the Fourier transform of the equation in the $x$ variable thereby obtaining $$-4\pi^2\omega^2 \hat u(\omega, y) + \frac{\partial^2 \hat u}{\partial y^2}(\omega, y) = 0$$
with the boundary condition that $\hat u(\omega, 0) = \hat f(\omega)$. The general solution of this ode un $y$ with $\omega$ fixed, takes the form $$\hat u(\omega, y) = A(\omega) e^{-2\pi |\omega| y} + B(\omega) e^{2\pi |\omega|y}$$We disregard the second term because of the rapid exponential growth, after setting $y =0$, that $$\hat u(\omega, y) = \hat f(\omega) e^{-2\pi |\omega|y}$$
Thus $u$ is given in terms of the convolution of $f$ with a kernel whose Fourier transform is $e^{-2\pi |\omega| y}$.

**Lemma:** The following identities hold:
$$\int_{-\infty}^\infty e^{-2\pi |\omega|y}e^{2\pi i x\omega }\, d\omega = \mathcal P_y(x)$$
$$\int_{-\infty}^\infty \mathcal P_y(x) e^{-2\pi i x\omega }\, dx = e^{-2\pi |\omega|y}$$

**Lemma:** The Poisson kernel is a good kernel on $\Bbb R$ as $y\to 0$

**Th:** Given $f\in \mathcal S(\Bbb R)$, let $u(x, y) = (f*P_y)(x)$. Then:
- $u(x, y)$ is $\mathcal C^2$ in $\Bbb R^2_+$ and $\nabla^2 u = 0$
- $u(x,y) \to f(x)$ uniformly as $y \to 0$
$$\lim_{y\to 0} \int_{-\infty}^\infty |u(x, y)- f(x)|^2 \,dx = 0$$
- If $u(x, 0) = f(x)$, then $u$ is continuous on the closure $\overline{\Bbb R^2_+}$ of the upper half-plane and vanishes at infinity in the sense that $$u(x, y) \to 0 \qquad \text{as }|x| + y \to \infty$$
We see that we solved the same problem in different ways in [[2D Harmonic Functions#Dirichlet Problem for the Upper Half plane|Complex analysis]], with the Poisson kernel given from above, while here we derived it. 

**Th:** Suppose $u$ is continuous on the closure of the upper half-plane $\overline{\Bbb R^2_+}$, satisfies that $\nabla^2 u =0$ for $(x, y) \in \Bbb R^2_+$, $u(x, 0) = 0$ and $u(x, y)$ vanishes at infinity. Then $u \equiv 0$. 
