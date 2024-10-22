---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Second Order Linear Differential Equations]]
An equation of the form

$$ t^2 \frac{d^2 y}{dt^2} + \alpha t\frac{dy}{dt} + \beta y =0 $$

It is solved by taking $x = \ln t$, then we get that

$$ \frac{dy}{dt} = \frac{1}{t}\frac{dy}{dx} \\ \quad \\

\frac{d^2y}{dt^2} = \frac{1}{t^2}\left(\frac{d^2y}{dx^2}-\frac{dy}{dx}\right) $$

Substiuing back into the equation we get that

$$ \frac{d^2y}{dx^2}+(\alpha-1)\frac{dy}{dx} + \beta y = 0 $$

Solving it we have that the characteristic poliomial has two cases. Let $\lambda_1$ and $\lambda_2$ be the roots then

- If $\lambda_1 \ne \lambda_2$ then, $y = c_1 e^{\lambda_1 x}+c_2 e^{\lambda_2 x}$, in terms of $t$ we have that $y = c_1 t^{\lambda_1}+c_2 t^{\lambda_2}$
- If $\lambda_1 = \lambda_2$ then $y = e^{\lambda_1x}(c_1+c_2x)$, in terms of $t$ we have that $y = t^{\lambda_1}(c_1+c_2\ln t)$