---
tags:
  - RealAnalysis
  - VectorAnalysis
---
Subjects: [[Real Analysis]], [[Vector Analysis]]
Links: [[Limits of a Sequence in R]]
## Pointwise Convergence

### Definition

The sequence of functions $(f_n)_{n\in\Bbb{N}}$ with a domain of $D$ into $\Bbb{R}^n$ converges pointwise to $f$, denoted as $f_n\to f$, iff:

$$ \forall x\in D\forall\varepsilon>0\exists N\in\Bbb{N}[\forall n\ge N(\|f_n(x)-f(x)\|_{}<\varepsilon)] $$

or

$$ \forall x\in D \left(\lim_{n\to\infty}f_n(x)=f(x) \right) $$

## Uniform Convergence

### Definition

A sequence of functions $(f_n)_{n\in\Bbb{N}}$, wit domain $D$ converges uniformly to $f$, denoted as $f_n\rightrightarrows f$, iff:

$$ \forall\varepsilon>0\exists N\in\Bbb{N}[\forall n\ge N\forall x\in D(\|f_n(x)-f(x)\|<\varepsilon)] $$

$$ \forall\varepsilon>0\exists N\in\Bbb{N}(\forall n \ge N[\|f_n-f\|_\infty <\varepsilon]) $$

_**Sequence Criterion for lack of Uniform Convergence**_

A sequence $( f_n)$ of functions on $A\subseteq\Bbb{R}$ to $\Bbb{R}$ does not converge uniformly on $A_0\subseteq A$ to a function $f : A_0\to\Bbb{R}$ if and only if for some $\varepsilon_0 > 0$ there is a subsequence $f_{n_k}$ of $f_n$ and a sequence $x_k$ in $A_0$ such that:

$$ \forall k\in\Bbb{N}[|f_{n_k}(x_k) -f(x_k)| \ge \varepsilon_0] $$

## Continuous Limit Theorem

If $f_k : D\to \Bbb{R}^n$ is a sequence of functions, and each $f_k$ is continuous at $c$, and $f_n\rightrightarrows f$, then $f$ is continuous at $c$.

- Algebraic Properties
    If $f_n\rightrightarrows f$ and $g_n\rightrightarrows g$, then
    - $f_n+g_n\rightrightarrows f+g$
    - if $\alpha \in \mathbb R$, then $\alpha f_n \rightrightarrows \alpha f$
    - If$f_n$ and $g_n$ are uniformly bounded then $f_n g_n \rightrightarrows fg$

### Cauchy Criterion

Let $f_k:D\to \Bbb{R}^n$ be a sequence of functions. Then $f_k$ converges uniformly iff

$$ \forall\varepsilon>0\exists N\in\Bbb{N}[\forall n,m\ge N\forall x\in D(\|f_n(x)-f_m(x)\|<\varepsilon)] $$

$$ \forall\varepsilon>0\exists N\in\Bbb{N}(\forall n, m \ge N[\|f_n-f_m\|_\infty <\varepsilon]) $$

This means that the space of continuous functions from $D$ into $\Bbb{R}^n$, also denoted as $\mathcal C(D, \Bbb{R}^n)$ is complete

- Preservation of things
    
    Uniform convergence preserves:
    
    1. Continuity
    2. Uniform Continuity
    3. Boundedness

### Dini’s Theorem
Suppose that $(f_n)$ is a monotone sequence of continuous functions on $I = [a, b]$ that converges pointwise on $I$ to a continuous function $f$. Then the convergence of the sequence is uniform.