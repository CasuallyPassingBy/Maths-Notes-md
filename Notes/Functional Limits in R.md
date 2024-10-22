---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Limits of a Sequence in R]], [[Open and Closed Sets in R]]
Let $f:D\to\Bbb{R}$, and $c$ be a limit point of $D$.

$$ \lim_{x\to c}f(x) = L $$

### $\varepsilon$-$\delta$ Definition

$$ \forall\varepsilon>0\exists\delta>0\forall x\in D[0<|x-c|<\delta\implies|f(x)-L|<\varepsilon] $$

### Sequential Definition

$$ \forall (x_n)_{n\in\Bbb{N}}\subseteq D[\forall n\in\Bbb{N}(x_n\Bbb{N}e c)\land[\lim_{n\to\infty}x_n=c\implies\lim_{n\to\infty}f(x_n)=L]] $$

### Topological Definition

$$ \forall\varepsilon>0\exists\delta>0\forall x\in D[x\in V_\delta(c)\setminus\{c\}\implies f(x)\in V_\varepsilon(f(c))] $$

### Divergence Criterion

Let $(x_n)$ and $(y_n)\subseteq D$ such that $\forall n\in\Bbb{N}(x_n, y_n \Bbb{N}eq c)$, and that $\lim_{n\to\infty}x_n =\lim_{n\to\infty}y_n =c$, such that $\lim_{n\to\infty}f(x_n)\Bbb{N}eq\lim_{n\to\infty}f(y_n)$. Then, $\lim_{x\to c}f(x)$ doesn’t exist.

## Algebraic Properties

Let $f, g:D\to\Bbb{R}$, and $c$ be a limit point of $D$, and $\lim_{x\to c}f(x) = L$ , $\lim_{x\to c}g(x) = M$ then:

1. for any $\alpha\in\Bbb{R}, \lim_{x\to c} cf(x) = cL$
2. $\lim_{x\to c}f(x) + g(x) = L + M$
3. $\lim_{x\to c}f(x)g(x) = LM$

## Different types of Limits

### Left and Right Limits

Let $f:D\to\Bbb{R}$, let $c$ be limit point of $D$, $\lim_{x\to c^+}f(x) = L$ iff

$$ \forall\varepsilon>0\exists\delta>0\forall x\in D[0<x-c<\delta\implies|f(x)-L|<\varepsilon] $$

$$ \forall (x_n)_{n\in\Bbb{N}}\subseteq D[\forall n\in\Bbb{N}(x_n> c)\land[\lim_{n\to\infty}x_n=c\implies\lim_{n\to\infty}f(x_n)=L]] $$

Let $f:D\to\Bbb{R}$, let $c$ be limit point of $D$, $\lim_{x\to c^-}f(x) = L$ iff

$$ \forall\varepsilon>0\exists\delta>0\forall x\in D[0<c-x<\delta\implies|f(x)-L|<\varepsilon] $$

$$ \forall (x_n)_{n\in\Bbb{N}}\subseteq D[\forall n\in\Bbb{N}(x_n < c) \land[\lim_{n\to\infty}x_n=c\implies\lim_{n\to\infty}f(x_n)=M]] $$

_**Theorem:**_ Let $f:D\to\Bbb{R}$, $c$ be a limit point of $D$, then:

$$ \lim_{x\to c^+}f(x) =\lim_{x\to c^-}f(x) = L\iff\lim_{x\to c}f(x) =L $$

### Infinite Limits

$$ \lim_{x\to c}f(x) =\infty\iff $$

$$ \forall M>0\exists\delta>0\forall x\in D[0<|x-c|<\delta\implies f(x)>M] $$

$$ \lim_{x\to\infty}f(x) =L\iff $$

$$ \forall\varepsilon>0\exists N>0\forall x\in D[x>N\implies |f(x)-L|<\varepsilon] $$

$$ \lim_{x\to\infty}f(x) =\infty\iff $$

$$ \forall M>0\exists N>0\forall x\in D[x>N\implies f(x)>M] $$

## Squeeze Theorem

Let $f, g, h:D\to\Bbb{R}$ , and $\delta > 0$ such that $\forall x \in V_\delta(c)[g(x)\le f(x)\le h(x)]$, and

$$ \lim_{x\to c}g(x) =\lim_{x\to c}h(x) = L \implies \lim_{x\to c} f(x) = L $$