---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Functional Limits in R]], [[The Derivative on R]]
$0/0$ case: 
Let $f,g$ be continuous on an interval containing $a$, assume $f$ and $g$ differentiable on this interval with the possible exception of $a$. If $f(a) = g(a) = 0$, and $g'(a)\neq 0$, then

$$ \lim_{x\to a}\frac{f'(x)}{g'(x)}= L\implies\lim_{x\to a}\frac{f(x)}{g(x)} =L $$

$\infty/\infty$ case: 
Assume $f$ and $g$ are differentiable on $(a, b)$ and that $g'(x) \ne 0$ for all $x ∈ (a, b)$. If $\lim_{x\to a} |g(x)|=\infty$ , then:

$$ \lim_{x\to a}\frac{f'(x)}{g'(x)}= L\implies\lim_{x\to a}\frac{f(x)}{g(x)} =L $$