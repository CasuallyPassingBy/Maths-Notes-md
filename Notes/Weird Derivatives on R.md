---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[The Derivative on R]]
## Weird Derivatives

Let $f:D\to \Bbb{R}$, and $c \in D$, $f$ is _right semidifferentiable_ at $c$, if $c$ is a limit point of ${D\cap [c, \infty)}$, then the left derivative of $f$ at $c$:

$$ \partial_+f(c)=D_+ f(c) = \left.\frac{d^+f}{dx}\right\rvert_c = f'_+(c) = \lim_{x\to c^+}\frac{f(x)-f(c)}{x-c} $$

Let $f:D\to \Bbb{R}$, and $c \in D$, $f$ is _left semidifferentiable_ at $c$, if $c$ is a limit point of ${D\cap (-\infty, c]}$, then the left derivative of $f$ at $c$:

$$ \partial_-f(c)=D_-f(c)=\left.\frac{d^-f}{dx}\right\rvert_c = f'_-(c) = \lim_{x\to c^-}\frac{f(x)-f(c)}{x-c} $$

If both the right derivative exists and are equal, then $f$ is differentiable at $c$

### Symmetric Derivative

Let $f:D\to \Bbb{R}$, and $c\in D$, $f$ is _symmetrically differentiable_ at $c$, and the symmetric derivative of $f$ at $c$ is:

$$ f_s(c) = \lim_{h\to 0}\frac{f(c+h)-f(c-h)}{2h} $$

provided the limit exists

Also if the right, left and symmetric derivative exists then:

$$ f_s(x) = \frac{\partial_- f(x)+\partial_+ f(x)}{2} $$

**************************Quasi Role’s Theorem**************************

Let $f:[a,b] \to \Bbb{R}$ be continuous on $[a,b]$ and symmetrically differentiable on $(a,b)$, and $f(a) = f(b) =0$, then:

$$ \exists x,y\in(a,b)[f_s(x) \le 0 \le f_s(y)] $$

**************************************************Quasi Mean Value Theorem**************************************************

Let $f:[a,b] \to \Bbb{R}$ be continuous on $[a,b]$ and symmetrically differentiable on $(a,b)$, then:

$$ \exists x,y\in(a,b)\left[f_s(x) \le \frac{f(b)-f(a)}{b-a} \le f_s(y)\right] $$

If $f_s$ has the Intermediate Value property then:

$$ \exists z \in (a,b) \left[f_s(z) = \frac{f(b)-f(a)}{b-a}\right] $$
