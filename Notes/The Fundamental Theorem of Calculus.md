---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Riemann Integral in R]], [[Riemann Integrals in R Properties]], [[The Derivative on R]]
## Part 1:

If $f:[a,b]\to\mathbb{R},$ and $f\in\mathcal{R}_{[a,b]}$. Let $F:[a,b]\to\mathbb{R}$ be differentiable and for any $x\in [a,b]$, then $F'(x) = f(x)$, then:

$$ \int_a^bf =F(a) - F(b) $$

## Part 2:

let $g:[a,b]\to\mathbb{R}$, then the function $G: [a,b]\to\mathbb{R}$ defined as:

$$ G(x)=\int_a^xg $$

Then $G$ is continuous on $[a, b]$. If $g$ is continuous at some $c\in[a,b]$, then $G$ will be differentiable at $c$, and it’s $G'(c) = g(c).$

## Consequences

### Substitution Theorem:

Let $J = [a,b]$ and $\varphi:J\to\mathbb{R}$, have a continuous derivative on $J$. If $f: I \to\mathbb{R}$ is continuous on $I$ and $\varphi(J)\subseteq I$, then:

$$ \int_a^b f(\varphi)\varphi' = \int_{\varphi(a)}^{\varphi(b)} f $$

### Integration by Parts:

Let $F,G \in \mathcal{C}^1[a,b]$ and $f:= F'$ , $g:= G'$ then:

$$ \int_a^b fG= FG\bigg|_a^b - \int_a^bFg $$