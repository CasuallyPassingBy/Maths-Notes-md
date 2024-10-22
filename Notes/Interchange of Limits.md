---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[The Derivative on R]], [[Continuity on R]], [[Riemann Integral in R]]
### Differentiable Limit Theorem
Let $f_n \to f$ on $[a,b]$, and that each $f_n$ is differentiable. If $(f'_n)$ converges uniformly on $[a,b]$ to a function $g$, then the function $f$ is differentiable and $f' =g$
**************Lemma:************** Let $(f_n)$ be a sequence of differentiable functions defined on the closed interval $[a, b]$, and assume $(f'_n)$ converges uniformly on $[a, b]$. If there exists a point ${x_0 ∈ [a, b]}$ where $f_n(x_0)$ is convergent, then $(f_n)$ converges uniformly on $[a, b]$.

**********************************Stronger Version:**********************************
Let $(f_n)$ be a sequence of differentiable functions defined on the closed interval $[a, b]$, and assume $(f'_n)$ converges uniformly to a function $g$ on $[a, b]$. If there exists a point $x_0 ∈ [a, b]$ for which $f_n(x_0)$ is convergent, then $(f_n)$ converges uniformly. Moreover, the limit function $f = \lim f_n$ is differentiable and satisfies $f' = g$.

Let $(f_n)$ be a sequence of functions be differentiable functions on the interval $I$, assume $\sum_{k=1}^\infty f'_n$ converges uniformly to a limit $g(x)$ on $A$. If there’s an $x_0\in[a,b]$ where $\sum_{n=1}^\infty f_n(x_0)$ converges, then the series $\sum_{n=1}^\infty f_n\rightrightarrows f$ where $f\in\mathcal{C}^1[a,b]$ satisfying $f'=g$. In other words:

$$ \sum_{n=1}^\infty f_n = f \text{, and } \sum_{n=1}^\infty f'_n=f' $$

### Integrable Limit Theorem
Assume that $f_n \rightrightarrows f$ on $I$, and that each $f_n \in\mathcal{R}_I$, then $f \in\mathcal{R}_I$ and that:

$$ \lim_{n\to\infty}\int_If_n = \int_If $$

Similarly suppose $g_k:I \to \Bbb R$, that for each $g_k \in \mathcal R_I$, and $\sum_{k = 1}^\infty g_k$ converges uniformly then, $\sum_{k = 1}^\infty g_k \in \mathcal R_I$, and

$$ \int_I \sum_{k = 1}^\infty g_k = \sum_{k = 1}^\infty\int_I g_k $$

### Bounded Convergence Theorem
Assume that $f_n \rightarrow f$, and $\exists K> 0\forall n \in \mathbb{N} (|f_n| \leq K)$, with both, $\forall n\in\mathbb{N}(f_n\in\mathcal{R}_I), f \in\mathcal{R}_I$, then:

$$ \lim_{n\to\infty}\int_If_n = \int_If $$

### **Moore-Osgood Theorem***
Let $a \in \Bbb R$ and the sequence of functions $f_n \rightrightarrows f$ on $X \setminus\{a\}$, and $\lim_{x\to a} f_n(x) = L_n$ exists for large $n\in \Bbb R$, then both $\lim_{n\to\infty} L_n$ and $\lim_{x\to a}f(x)$ exist and are equal, i.e.

$$ \lim_{n\to\infty}\lim_{x\to a}f_n(x) = \lim_{x\to a}\lim_{n\to\infty}f_n(x) $$
## Some Interchange properties

Let $\varphi_n:(0, \infty) \to (0, \infty)$, and $\varphi = \sum\limits_{n = 1}^\infty \varphi$. If $\sum\limits_{n = 1}^\infty \varphi$ converges uniformly on every $[a,b] \subseteq (0, \infty)$, and $\int \varphi < \infty$, then:
$$\int_0^\infty \varphi_n <\infty\qquad \forall n \in \Bbb N^+$$
$$\sum_{n = 1}^\infty \int_0^\infty \varphi_n <\infty$$
$$\sum_{n = 1}^\infty \int_0^\infty \varphi_n = \int_0^\infty \varphi  = \int_0^\infty \sum_{n = 1}^\infty \varphi_n $$
