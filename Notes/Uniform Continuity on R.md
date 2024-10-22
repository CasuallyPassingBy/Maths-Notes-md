---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Continuity on R]]

## Definitions

### $\varepsilon$-$\delta$ Definition

let $f:A\to\Bbb{R}$ is said to be _uniformly continuous on $A$_ iff:

$$ \forall\varepsilon>0\exists\delta>0\forall x,y\in A[|x-y|<\delta\implies|f(x)-f(y)|<\varepsilon] $$

### Sequential Criterion

$$ \forall(x_n), (y_n) \subseteq D [\lim_{n\to\infty}| x_n-y_n| = 0 \implies\lim_{n\to\infty} |f(x_n)-f(y_n)|= 0] $$

## Sequential Criterion for Absence of UC

Let $f:A\to\Bbb{R}$, _fails to be uniformly continuous on A_ iff there’s a $\varepsilon_0>0$, and sequences $(x_n)$ and $(y_n)$ contained in $A$, and:

$$ |x_n -y_n|\to 0 \text{ and, } |f(x_n)-f(y_n)| \ge\varepsilon_0 $$

## Lipschitz Functions

$f:D\to\Bbb{R}$, is a _Lipschitz function_ iff there’s an $M>0$ such that:

$$ \forall x,y\in D[|f(x)-f(y)|\le M|x-y|] $$

### Contraction Mapping Theorem

Let $f:\Bbb{R}\to\Bbb{R}$, $f$ is a Lipschitz function with a Lipschitz constant of $c$ with $0<c<1$. with an arbitrary $x\in\Bbb{R}$, and the sequence:

$$ y_n =\begin{cases} x&n=0\\ f(y_{n-1}) &\text{otherwise} \end{cases} $$

Then there’s a unique $y$, such that no matter the starting value $\lim_{n\to\infty}y_n = y$. This is a special case of [[Banach's Fixed Point Theorem]]

## Hölder Functions

$f:D\to\Bbb{R}$, is a _Hölder function_ iff there’s are $M, \alpha>0$ such that:

$$ \forall x,y\in D[|f(x)-f(y)|\le M|x-y|^\alpha] $$

When $\alpha \ge 1$, then it will be a Lipschitz function.

### Uniform Extension Theorem
Let $f:(a,b)\to\Bbb{R}$, $f$ is uniformly continuous on $(a,b)$ iff $f$ can be extended to the endpoints such that $f:[a,b]\to\Bbb{R}$ is uniformly continuous