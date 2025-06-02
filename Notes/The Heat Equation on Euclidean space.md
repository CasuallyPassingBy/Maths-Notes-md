---
tags:
  - FourierAnalysis
  - PartialDifferentialEquations
---
Links: [[Fourier Transform in Rn]], [[The Heat Equation on the Real line]]

We consider the time-dependent heat equation in $\Bbb R^n$ $$\frac{\partial u}{\partial t} = \Delta u$$
with the boundary values $u(x, 0) = f(x) \in \mathcal S(\Bbb R^n)$. We make a similar procedure as we did for the real line. But now we apply The Fourier transform with respect to the spacial coordinates to the heat equation getting that: $$-4\pi^2 \|\omega\|^2\hat u(\omega, t) = \frac{\partial \hat u}{\partial t}(\omega,t)$$If we fix $\omega$ this is an ODE in $t$, solving it we get that $$\hat u (\omega, t) = A(\omega) e^{-4\pi^2\|\omega\|^2 t}$$
We apply the boundary condition, and we see that $A(\omega) = \hat f(\omega)$, getting the solution $$\hat u(\omega, t) = \hat f(\omega) e^{-4\pi^2\|\omega\|^2t}$$
With this in mind we can, calculate the $n$-dimensional heat kernel as, the inverse Fourier transform of $e^{-4\pi^2\|\omega\|^2 t}$, getting that $$\mathcal H_t^{(n)}(x) = \frac1{({4\pi t})^{n/2}} e^{-\|x\|^2/4t}$$
We see that $$\hat{ \mathcal H}_t^{(n)} (\omega) = e^{-4\pi^2\|\omega\|^2 t}$$
**Th:** Given $f \in \mathcal S(\Bbb R)$, let $$u(x, t)= (f*{\mathcal H_t^{(n)}})(x)$$where $\mathcal H_t$ is the heat kernel. Then:
- The function $u$ is ${\cal C}^2$ when $x \in \Bbb R^n$ and $t>0$, and $u$ solves the heat equation
- $u(x, t) \to f(x)$ uniformly in $x$ as $t\to 0$. Hence if we set $u(x, 0) = f(x)$, then $u$ is continuous on  $\overline{\Bbb R^{n+1}_+}= \{(x, t) \in \Bbb R^n \times \Bbb R^{\ge 0}\mid x \in \Bbb R, t \ge 0\}$
and
$$\lim_{t \to 0^+}\int_{-\infty}^\infty |u(x, t)-f(x)|^2\, dx = 0$$

**Th:** Suppose that $u(x, t)$ satisfies the following conditions:
- $u$ is continuous on $\overline{\Bbb R^{n+1}_+}= \{(x, t) \in \Bbb R^n \times \Bbb R^{\ge 0}\mid x \in \Bbb R, t \ge 0\}$
- $u$ satisfies the heat equation for $t>0$
- $u$ satisfies the boundary condition $u(x, 0) = 0$
- $u(\cdot, t)\in \mathcal S(\Bbb R)$ uniformly in $t$
Then we conclude that $u \equiv 0$
