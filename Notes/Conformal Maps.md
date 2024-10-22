---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]]

A map $f:A \to \Bbb C$ is called ************_conformal at $z_0$_ if there exists $\theta \in [0, 2\pi)$ and an $r>0$ such that for any curve $\gamma(t)$ that is differentiable at $t=0$, for which $\gamma(t) \in A$ and $\gamma(0) = z_0$, and satisfies $\gamma'(0) \ne 0$, the curve $\sigma(t) = f(\gamma(t))$ is differentiable at $t=0$ and, setting ${u = \sigma'(0)}$ and $v = \gamma'(0)$, we have that $|u| =r|v|$ and $\arg u = \arg v + \theta \pmod{2\pi}$. A map is called **********conformal********** when it is conformal at every point.

### Conformal Mapping Theorem

If $f:A\to \Bbb C$ is analyitic and $f'(z_0) \ne0$, then $f$ is conformal at $z_0$ with $\theta = \arg(f'(z_0))$ and $r= |f'(z_0)|$.