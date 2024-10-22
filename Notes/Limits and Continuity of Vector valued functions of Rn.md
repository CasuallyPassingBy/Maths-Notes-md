---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Vector Valued Functions of Rn]], [[Topological Characterization of Continuity in Rn]]

**********Def:********** A function $f:S \subseteq\Bbb R^n\to\Bbb R^m$ is said to be _continuous at $x \in S$_ if, for any sequence $(a_k) \subseteq S$, $f(a_k) \to f(x)$ whenever $a_k \to x$. The function is continuous if it is continuous at every point of $S$.

********Th:******** A function $f:S \subseteq\Bbb R^n\to\Bbb R^m$ is continuous at $x\in S$ iff for each ${1 \le i \le m}$ the coordinate function $f_i :S \subseteq \Bbb R^n \to \Bbb R$ is continuous at $x$.

********Cor:******** Let $D$ be an open subset of $\Bbb R^n$. A function $f:D\subseteq \Bbb R^n \to \Bbb R$ is continuously differentiable iff ********$\nabla f:D\to \Bbb R^n$** is continuous.

**************Cor:************** Any linear function $f:\Bbb R^n\to \Bbb R^m$ is continuous.

**********Def:********** Given a cluster point $x_0$ of $S \subseteq \Bbb R^n$, and a point $L \in \Bbb R^m$, and a function $f:S \to \Bbb R^m$, we write $\lim_{{x \to x_0}}f(x) = L$ if $f(a_k) \to L$ whenever $a_k \to x_0$, where the sequence ${( a_k) \subseteq S}$ and for all $k \in \Bbb N$ $a_k \ne x_0$.

**************Th:************** Given the function $f:S\subseteq\Bbb R^n \to \Bbb R^m$ and a cluster point $x_0$ of $S$, then ${\lim_{{x\to x_0}}f(x) = L}$ iff

$$ \forall \varepsilon >0\exists \delta >0\forall x \in S[0<\|x-x_0\|<\delta\implies \|f( x) -L\| < \varepsilon] $$

********Th:******** The function $f:S\subseteq\Bbb R^n\to\Bbb R^m$ is continuous at $x_0 \in S$ iff $\lim_{{x\to x_0}}f(x) =f(x_0)$
- Properties
    Let $f, g:S\subseteq\Bbb R^n\to\Bbb R^m$ and $\phi:S\subseteq\Bbb R^n\to\Bbb R$ be continuous at $\mathbf p$. Then the following functions are continuous:
    - $f+g$
    - $f\cdot g$
    - $\phi f$
    - if $n = 3$, $f\times g$
    If $g:E\subseteq\Bbb R^k\to \Bbb R^n$ and $f:D\subseteq\Bbb R^n\to\Bbb R^m$ such that $g(E) \subseteq D$, if $g$ is continuous at $\mathbf p\in E$ and $f$ is continuous at $g(\mathbf p) \in D$, then $f \circ g:E \to \Bbb R^m$ is continuous at $\mathbf p$.

**Def:** Let $S$ be a subset of $\Bbb R^n$ a *vector field* is represented by a vector valued function $f:S \to \Bbb R^n$. If $f$ is continuous then we say that the vector field is continuous, similarly if $f$ is differentiable, then the vector field is differentiable, and so on. Lastly we can have that $f:(a,b)\times S\to \Bbb R^n$ can be called a *time-dependent vector field*