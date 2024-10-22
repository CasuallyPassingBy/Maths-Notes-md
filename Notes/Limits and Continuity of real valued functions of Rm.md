---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Real-valued Functions of Rn]], [[Topological Characterization of Continuity in Rn]]

**********Def:********** The function $f:S\subseteq\Bbb R^n\to \Bbb R$ is said to be continuous at ${x \in S}$ if ${f({a}_k}) \to f(x)$ whenever $\mathbf{a}_k$, where the sequence $({a}_k) \subseteq S$. The function is continuous (on its domain $S$) if it is continuous at every point of $S$.

********Th:******** If $f, g:S\subseteq \Bbb R^n\to \Bbb R$ and if they are continuous at $x\in S$, then so is ${f+g}$, $fg$ and (provided that $g(x) \ne 0$) so is $f/g$.

**********Def:********** Given a cluster point $\mathbf{p} \in S \subseteq\Bbb R^n$, a point $L \in \Bbb R$, and a function $f:S\to \Bbb R$, we write $\lim_{{x} \to x_0}f(x) = L$ if ${f({a}_k) \to L}$ whenever $({a}_k ) \subseteq S$, ${a_k} \to x_0$ and ${a}_k \ne x_0$ for all ${k \in \Bbb N}$.

******Th:****** The function $f:S\subseteq \Bbb R^n \to \Bbb R$ is continuous at a cluster point $x_0\in S$ iff ${\lim_{x \to x_0}f(x) = f(x_0)}$.

********Th:******** Given a function $f:S\subseteq \Bbb R^n\to \Bbb R$ and a cluster point $x_0\in S$, then $\lim_{x \to x_0} f(x) = L$ iff:

$$ \forall \varepsilon>0\exists \delta>0\forall x\in S[0 < \|x-x_0\| < \delta \implies |f( x) - L| < \varepsilon] $$

or equivalently using balls:

$$ \forall \varepsilon>0\exists \delta>0\forall x\in S[x \in B_\delta(x_0) \implies f(x) \in B_\varepsilon(q)] $$

## Double Limits

In $\Bbb R^{m+k}$ we can create a different kind of double limit from $\lim_{(x,y)\to (a,b)}f(x,y)$,

$$ \lim_{\begin{smallmatrix} x \to a \\ y \to b \end{smallmatrix}} f(x,y) = L $$

We define this kind of double limit as

$$ \forall \varepsilon>0\exists \delta >0\forall (x, y)\in S[0<\|x-a\|, \|y-b\| < \delta \implies |f(x,y)-L|< \varepsilon] $$

This notion of double limit is weaker than the original definition:

********Th:******** If $\lim_{(x,y)\to (a,b)}f(x,y) = L$, then $\lim_{\begin{smallmatrix} x \to a \\ y \to b \end{smallmatrix}} f(x,y) =L$.

********Th:******** If $\lim_{\begin{smallmatrix} x \to a \\ y \to b \end{smallmatrix}} f(x,y) =L$, $\lim_{x\to a}f(x,y)$ exists for each $y$ near $b$, and $\lim_{y\to b}f(x,y)$ exist for $x$ near $a$, then $\lim_{y\to b}\lim_{x\to a}f(x,y) = \lim_{x\to a}\lim_{y\to b}f(x,y) = L$.

**********Cor:********** If $\lim_{(x, y)\to (a,b)} f(x,y) =L$, $\lim_{x\to a}f(x,y)$ exists for each $y$ near $b$, and $\lim_{y\to b}f(x,y)$ exist for $x$ near $a$, then $\lim_{y\to b}\lim_{x\to a}f(x,y) = \lim_{x\to a}\lim_{y\to b}f(x,y) = L$.

Similarly, for limits to infinity (in $\Bbb R^2$)we can think of

$$ \lim_{\begin{smallmatrix} x \to \infty \\ \\ y \to \infty \end{smallmatrix}} f(x,y) = L $$

as

$$ \forall \varepsilon >0\exists M>0[x,y > M \implies |f(x,y)-L|<\varepsilon] $$

********Th:******** If $\lim_{\begin{smallmatrix} x \to \infty \\ y \to \infty \end{smallmatrix}} f(x,y) =L$, $\lim_{x\to \infty}f(x,y)$ exists for each large $y$, and $\lim_{y\to b}f(x,y)$ exist for large $x$, then ${\lim_{y\to \infty}\lim_{x\to \infty}f(x,y) = \lim_{x\to \infty}\lim_{y\to \infty}f(x,y) = L}$.

## Uniform Convergence

Let $X\subseteq \Bbb R^n$ , $Y \subseteq \Bbb R^k$ and $f:X\times Y\subseteq\Bbb R^{n+k}\to\Bbb R$. Let $x_0 \in X'$ and $y_0\in Y'$. The limit $\lim_{x\to x_0} f(x,y) = \phi(y)$ exists for each $y \in B$ if the following hold:

$$ \forall y \in B\forall \varepsilon>0\exists \delta>0\forall x\in A[0 < |x-x_0|< \delta \implies |f(x,y)-\phi(y)| < \varepsilon] $$

We can formulate the a similar existence condition for $\lim_{y\to y_0}f(x,y) = \mu(x)$.

We can define a stronger type of convergence $\lim_{x\to x_0}f(x,y) = \phi(y)$ exists ************_uniformly in $x \in A$_ if **************************

$$ \forall \varepsilon>0\exists \delta>0\forall x\in A\forall y \in B[0 < |x-x_0|< \delta \implies |f(x,y)-\phi(y)| < \varepsilon] $$

We also say that $\lim_{x\to x_0}f(x,y) = \phi(y)$ uniformly on $Y$. We can formulate the a similar existence condition for $\lim_{y\to y_0}f(x,y) = \mu(x)$ uniformly on $X$.

**********Th:********** The Cauchy condition for the existence of the $\lim_{x\to x_0}f(x,y) = \phi(y)$ uniformly on $Y$ is

$$

\forall \varepsilon>0\exists \delta>0\forall x, x'\in A\forall y \in B[0<|x-x_0|, |x'-x_0|<\delta \implies |f(x,y)-f(x',y)| < \varepsilon]

$$

and it is equivalent to uniform convergence of $\lim_{x\to x_0}f(x,y) = \phi(y)$

### Moore-Osgood Theorem

If $\lim_{x \to a}f(x,y) = g(y)$ uniformly on $Y\setminus\{b\}$ and $\lim_{y\to b} f(x,y) = h(x)$ for each $x$ near $a$, then both $\lim_{y\to b}g(y)$ and $\lim_{x\to a}h(x)$ exist and are equal to the double limit

$$ \lim_{x\to a}\lim_{y\to b} f(x,y) = \lim_{y\to b}\lim_{x\to a} f(x,y) = \lim_{\begin{smallmatrix} x \to a \\ y \to b \end{smallmatrix}} f(x,y) $$

both $a$ and $b$ can be infinite

### Intermediate Value Theorem on $\Bbb R^n$

Let $f: A\subseteq \Bbb R^n\to \Bbb R$ continuous and $B \subseteq A$ connected and $x_1, x_2 \in B$ such that $f(x_1) < f(x_2)$. If $c \in \Bbb R$ such that $f(x_1)<c < f(x_2)$, then there exists $x \in B$ such that $f(x) = B$.