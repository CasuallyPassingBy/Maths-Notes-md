---
tags:
  - FourierAnalysis
  - PartialDifferentialEquations
---
Subjects: [[Fourier Analysis]], [[Partial Differential Equations]]
Links: [[Fourier Transform in R]], [[The Heat Equation]], [[Convolution#Rapidly Decreasing Functions|Convolution for Rapidly Decreasing Functions]]

Consider an infinite rod, which we model by the real line, and suppose that we are ficen an initial temperature distribution $f(x)$ on the rod at time $t = 0$, We wish now to determine the temperature $u(x, t)$ at the point $x$ and time $t>0$. When $u$ is properly normalised, it solves the following pde:  $$ \frac{\partial u}{\partial t} = \frac{\partial^2 u}{\partial x^2}$$called the *heat equation*. The initial condition we impose is $u(x, 0) = f(x)$.

Just as in the case of [[The Heat Equation on the Circle|circle]] the solution is given in terms of a convolution. Indeed, define the *heat kernel* of the line by $$\mathcal H_t(x) = K_\delta(x), \qquad \text{with } \delta = 4\pi t$$so that $$\mathcal H_t(x) = \frac1{(4\pi t)^{1/2}}e^{-x^2/4t}\qquad \text{and} \quad \hat{\mathcal H_t}(\omega) = e^{-4\pi^2t\omega^2}$$
We see that as $t \to 0$, then $\delta \to 0$, then we see that $\mathcal H_t(x)$ is a good kernel as $t\to 0$. 

If we take the Fourier transform of the heat equation in the $x$ variable, leads to $$\frac{\partial \hat u}{\partial t}(\omega, t) = -4\pi^2\omega^2\hat u(\omega, t)$$If we fix $\omega$, this is an ode in the variable $t$, so there exists $A(\omega)$ so that $$\hat u(\omega, t) = A(\omega) e^{-4\pi^2 \omega^2 t}$$we mat also take the Fourier transform of the initial condition and obtain $\hat u(\omega, 0) = \hat f(\omega)$, hence $A(\omega) = \hat f(\omega)$, then the solution is $$\hat u(\omega, t) = \hat f(\omega) e^{-4\pi^2\omega^2 t} = \hat f(\omega) \hat{\mathcal H_t}(\omega)$$
**Th:** Given $f \in \mathcal S(\Bbb R)$, let $$u(x, t)= (f*{\mathcal H_t})(x)$$where $\mathcal H_t$ is the heat kernel. Then:
- The function $u$ is ${\cal C}^2$ when $x \in \Bbb R$ and $t>0$, and $u$ solves the heat equation
- $u(x, t) \to f(x)$ uniformly in $x$ as $t\to 0$. Hence if we set $u(x, 0) = f(x)$, then $u$ is continuous on the closure of the upper half-plane $\overline{\Bbb R^2_+}= \{(x, t) \mid x \in \Bbb R, t \ge 0\}$
and
$$\lim_{t \to 0^+}\int_{-\infty}^\infty |u(x, t)-f(x)|^2\, dx = 0$$

**Cor:** $u(\cdot, t)$ belongs to $\mathcal S(\Bbb R)$ uniformly in $t$, in the sense that for any $T>0$, $$\sup_{
\substack{x\in \Bbb R\\ 0< t< T}}|x|^k \left| \frac{\partial^n}{\partial x^n} u(x, t)\right| < \infty \qquad \forall k, n \ge 0$$
**Th:** Suppose that $u(x, t)$ satisfies the following conditions:
- $u$ is continuous on the closure of the upper half-plane
- $u$ satisfies the heat equation for $t>0$
- $u$ satisfies the boundary condition $u(x, 0) = 0$
- $u(\cdot, t)\in \mathcal S(\Bbb R)$ uniformly in $t$
Then we conclude that $u \equiv 0$

The idea of the proof is to define the energy at time $t$ of the solution $u(x, t)$ by $$E(t) = \int_\Bbb R |u(x,t)|^2\, dx$$$E(t) \ge 0$, we proved that $E'(t) \le 0$, and since $E(0) = 0$, thus it must be that $E \equiv 0$, thus also $u$

The idea that seems interesting is that the initial condition must also have "finite" energy to have a Fourier transform, and seems like a prerequisite to be solvable. 

**Th (Tychonoff):** Supose $u(x, t)$ satisfies the conditions:
- $u(x,t)$ solves the heat equation for all $x\in \Bbb R$ and $t>0$
- $u(x, t)$ is continuous for all $x\in \Bbb R$ and $0\le t\le c$
- $u(x, 0) = 0$
- $|u(x, t)| \le M e^{ax^2}$ for some $M, a$ and all $x \in \Bbb R$, $0\le t \le c$
Then $u$ is identically equal to $0$
