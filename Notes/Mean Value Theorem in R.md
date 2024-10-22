---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[The Derivative on R]]
## Rolle’s Theorem

Let $f:[a,b]\to\Bbb{R}$, $f$ be differentiable on $(a,b)$ and continuous on $[a,b]$. If $f(a)=f(b)$, there’s a $c\in(a,b)$ such that $f’(c) = 0$.

## MVT

Let $f:[a,b]\to\Bbb{R}$, $f$ be differentiable on $(a,b)$ and continuous on $[a,b]$. If $f(a)=f(b)$, there’s a $c\in(a,b)$ such that:

$$ f'(c) =\frac{f(b) -f(a)}{b-a} $$

## Corollaries

Let $g:I\to\Bbb{R}$, $g$ is differentiable on $I$, and $g'(x) = 0$ for all $x\in I$, then $g(x) = k$ for some $k\in\Bbb{R}$.

Let $f$, and $g$ be differentiable on $I$, and $f'(x) = g'(x)$ , for all $x\in I$, then there’s a $k\in\Bbb{R}$, such that $f(x) = g(x) + k$.

Let $f$ be differentiable on $I$, then:

1. $f$ is increasing on $I$ iff $f' \ge 0$ on $I$.
2. $f$ is decreasing on $I$ iff $f' \le 0$ on $I$.

## Generalized MVT

Let $f,g$ be continuous on $[a,b]$ and differentiable on $(a,b)$. Then, there’s a $c\in(a,b)$, such that:

$$ [f(b)-f(a)]g'(c)= [g(b)-g(a)]f'(c) $$

if $g'$ is never zero then it can be expressed as:

$$ \frac{f'(c)}{g'(c)} = \frac{f(b)-f(a)}{g(b)-g(a)} $$