---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Continuity on R]], [[Functional Limits in R]]
Let $f:D\to\Bbb{R}$, $f$ is _differentiable at $c\in D$,_ and the derivative of $f$ at $c$ if:

$$ Df(c)=\left.\frac{df}{dx}\right\rvert_c = f'(c) = \lim_{x\to c}\frac{f(x)-f(c)}{x-c} = \lim_{h\to 0}\frac{f(c+h) -f(c)}{h} $$

provided the limit exists.

_**Theorem:**_ If $f:D\to\Bbb{R}$ is differentiable at $c$, then $f$ is continuous at $c$.

## Algebraic Properties

_**Theorem:**_ If $f,g:D\to\Bbb{R}$, if $f$ and $g$ are differentiable at $c$, then:

1. $(kf)'(c) = kf'(c)$, for any $k\in\Bbb{R}$.
2. $(f+g)'(c) = f'(c) + g'(c)$
3. $(fg)'(c) = f(c)'g(c) + f(c)g'(c)$
4. $\left(\frac{f}{g}\right)'(c) = \frac{g(c)f'(c)-g'(c)f(c)}{(g(c))^2}$, with $g(c) \ne 0$

### General Leibniz rule
If $f$ and $g$ is $n$ times differentiable functions, then $fg$ is also $n$ times differentiable and its $n$th derivative is given by 
$$
(fg)^{(n)}=\sum_{k=0}^n {n \choose k} f^{(n-k)} g^{(k)}
$$
## Chain Rule

_**Carathéodory’s Theorem:**_ Let $f:D\to\Bbb{R}$, $f$ is differentiable at $c$ iff there’s a continuous at $c$ ,$\varphi:D\to\Bbb{R}$, that satisfies:

$$ f(x)-f(c)=\varphi(x)(x-c), \text{ for, } x\in D $$

In this case, we have $\varphi(c) =f'(c)$

_**Chain Rule:**_ Let $f:J\to\Bbb{R}$, and $g:I\to\Bbb{R}$, functions $f(J)\subseteq I$, and $c\in J$. If $f$ is differentiable at $c$ and $g$ is differentiable at $f(c),$ the composite function $g\circ f$ is differentiable at $c$ and:

$$ (g\circ f)'(c)=g'(f(c))f'(c) $$

## Inverse Functions

_**Differentiable Inverse Theorem:**_ Let $I$ be an interval in $\Bbb{R}$ and let $f : I\to\Bbb{R}$ be strictly monotone and continuous on $I$. Let $J=f(I)$ and let $f^{-1}: J\to\Bbb{R}$ be the strictly monotone and continuous function inverse to $f$. If f is differentiable at $c\in I$ and $f'(c)\neq 0$, then $f^{-1}$ is differentiable at $f(c)$ and:

$$ (f^{-1})'(f(c))=\frac{1}{f(c)} $$

## Darboux’s Theorem

### Interior Extremum Theorem

Let $f$ be differentiable on an open interval $(a, b)$. If $f$ attains a maximum value at some point $c ∈ (a, b)$, then $f'(c)=0$. The same is true if $f(c)$ is a minimum value.

### Darboux’s Theorem

Let $f$ be differentiable on $[a,b]$, and if $L$, is between $f'(a)$ and $f'(b)$, then there’s a $c\in(a,b)$ such that $f'(c) = L$. In other words, any derivative of a function must have the [[Intermediate Value Theorem in R#Intermediate Value/Darboux Property|IVP]].