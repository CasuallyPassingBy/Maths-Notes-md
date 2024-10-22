---
tags:
  - VectorAnalysis
  - DifferentialGeometry
---
Subjects: [[Vector Analysis]], [[Differential Geometry]]
Links: [[Differentiabilty of vector valued functions of R]], [[Rectifiable Curves in Rn#Arc-lenght Parametrization|Arc-lenght Parametrization]]

**Def:** Let $\gamma:E\subseteq\Bbb R\to\Bbb R^n$ be a twice differentiable arc-length parametrization of a curve $\gamma(E)$ in $\Bbb R^n$:

- The unit tangent vector $\gamma'(s)$ at $s \in E$ will also be denoted as $T(s)$
    
- The non-negative number:
    
    $$ \kappa (s) = \|T'(s)\|=\|\gamma''(s)\| $$
    
    is called the _****curvature****_ of $\gamma$ at $s$.
    
- If $\kappa (s) \ne0$, then the unit vector $N(s)$ such that:
    
    $$ T'(s) = \kappa(s) N(s) $$
    
    is called the ************principal normal************ to $\gamma$ at $s$. If $\kappa(s)=0$, the principal normal is not defined at $s$.
    
- The plane in $\Bbb R^n$ through $\gamma(s)$ parallel to the subspace spanned by $T(s)$ and $N(s)$ is called the **********osculating plane********** of $h$ at $s$.
    
- If $\gamma''(s)\ne 0$, we define the the ************osculating circle************ with center of
    
    $$ Q(s)=\gamma(s) +\frac{1}{\kappa(s)}N(s) $$
    
    and a radius of, sometimes called the ******radius of curvature:******
    
    $$ R(s) = \frac{1}{\kappa(s)} $$
    

********Th:******** Let $\gamma:E\subseteq\Bbb R \to \Bbb R^n$ be a twice differentiable arc-length parametrization. Then $\kappa(s) = 0$ for all $s \in E$ iff $h(E)$ is a subset of a straight line in $\Bbb R^n$.

**********Th:********** Let $\gamma:E\subseteq \Bbb R \to \Bbb R^3$ be a three differentiable arc-length parametrization of a curve $C$ in $\Bbb R^3$ with $\kappa(s) \ne 0$ for all $s \in E$. The curve $C$ lies in a plane in $\Bbb R^3$ iff $N'(s)$ is a multiple of $T(s)$.

********Th:******** With the hypothesis above, the vector $N'(s) + \kappa(s)T(s)$ is orthogonal to the osculating plane at $\gamma$ at $s$.

**********Def:********** Suppose that the function $\gamma:E\subseteq \Bbb R\to\Bbb R^3$ is 3 times differentiable arc-length parametrization of a curve in $\Bbb R^3$ with $\kappa(s) \ne 0$ for all $s\in E$.

- For each $s \in E$, the unit vector:
    
    $$ B(s) = T(s) \times N(s) $$
    
    is called the _********binormal********_ at $h$ at $s$
    
- There’s a number $\tau(s)$ such that:
    
    $$ N'(s) + \kappa(s)T(s)= \tau(s)B(s) $$
    
    The number $\tau(s)$ is called the ********torsion******** of $\gamma$ at $s$.
    

********Cross-Product Relations:********

$$ \begin{align} T(s) \times N(s)&= B(s), \\ B(s) \times T(s) &= N(s),\\ N(s) \times B(s) &= T(s)\end{align} $$

********Frénet-Serret Equations:******** Suppose that the function $\gamma:E\subseteq \Bbb R\to\Bbb R^3$ is 3 times differentiable arc-length parametrization of a curve in $\Bbb R^3$ with $\kappa(s) \ne 0$ for all $s\in E$. The three vector value functions $T, N, B$ on $E$ and the two real-valued functions $\kappa$ and $\tau$ on $E$ satisfy the following formula:

$$ \begin{align} \frac{d{T}}{ds} &= \kappa{N}, \\ \frac{d{N}}{ds} &= -\kappa\mathbf{T}+\tau{B},\\ \frac{d{B}}{ds} &= -\tau{N}\end{align} $$

or:

$$ \begin{bmatrix} {T'} \\ {N'} \\ {B'} \end{bmatrix} = \begin{bmatrix} 0 & \kappa & 0 \\ -\kappa & 0 & \tau \\ 0 & -\tau & 0\end{bmatrix}\begin{bmatrix} {T} \\ {N} \\ {B} \end{bmatrix} $$

********Th:******** Let $\gamma, \eta:E\subseteq\Bbb R \to \Bbb R^3$ be two three times differentiable arc-length parametrizations of curves $C_\gamma$ and $C_\eta$ in $\Bbb R^3$. If ${\kappa_\gamma(s) = \kappa_\eta(s) \ne 0}$ and ${\tau_\gamma(s) = \tau_\eta(s)}$ for all $s \in E$, then the two curves are identical, except possibly in their positions in space.

********Th:******** Let $\gamma, \eta:E\subseteq\Bbb R \to \Bbb R^2$ be two two times differentiable arc-length parametrizations of curves $C_\gamma$ and $C_\eta$ in $\Bbb R^3$. If ${\kappa_\gamma(s) = \kappa_\eta(s) \ne 0}$ for all $s \in E$, then the two curves are identical, except possibly in their positions in space.

**********Th:********** With the above notation, and denoting $\lambda'(t) = \|f'(t)\|$ by $v(t)$, and $\gamma$ is the re-parametrization by arc-length of $f$, we have, for ${t\in D}$ ********************

- $f'(t) = v(t) T_\gamma(\lambda(t))$
- $f''(t) = v'(t)(T_\gamma\circ \lambda)(t) + (v(t))^2 (\kappa_\gamma \circ \lambda)(t)(N_\gamma \circ \lambda)(t)$, if ${(\kappa_\gamma \circ \lambda)(t) >0}$
- $f''(t) = v'(t)(T_\gamma\circ \lambda)(t)$ , if ${(\kappa_\gamma \circ \lambda)(t) =0}$

**********Def:********** In the notation of the above theorem we define:

- $T_f(t) = (T_\gamma \circ \lambda)(t)$
- $N_f(t) = (N_\gamma \circ \lambda)(t)$
- $\kappa_f(t) = (\kappa_\gamma \circ \lambda)(t)$

and provided $n = 3$

- $B_f(t) = (B_\gamma \circ \lambda)(t)$
- $\tau_f(t) = (\tau_\gamma \circ \lambda)(t)$

********Th:******** Let $f:D\subseteq\Bbb R \to \Bbb R^n$ be a twice differentiable smooth parametrization of a curve ${C= f(D)}$ in $\Bbb R^n$, and let $v(t) = \|f'(t)\|$, $t\in D$. Then the unit tangent $T_f(t)$, and the curvature $\kappa_f(t) \ge 0$, and if $\kappa_f(t) >0$, the principal normal $N_f(t)$ to $f$ at ${t\in D}$ are given by the relations

$$ \begin{align} f'(t) &= v(t)T_f(t), \\ f''(t) &= v'(t)T_f(t)+(v(t))^2\kappa_f(t)N_f(t)\\ \end{align} $$

Furthermore, for the case $n = 3$, if $\kappa_f(t) \ne 0$, the binomial $B_f(t)$ and torsion $\tau_f(t)$ to $f$ at $t$ are given by:

$$ \begin{align} B_f(t) &= T_f(t)\times N_f(t), \\ B_f'(t) &= -v(t)\tau_f(t)N_f(t)\\ \end{align} $$

## Formula Compendium

### Parametrization by Arc-Length

$$ \begin{align} T(s) &= \gamma'(s), \\ \kappa(s) &= \|\gamma''(s)\|,\\ N(s) &= \frac{\gamma''(s)}{\|\gamma''(s)\|} ,\\ B(s) &= \frac{\gamma'(s) \times \gamma''(s)}{\|\gamma''(s)\|}, \\ \tau(s) &= \frac{\gamma'''(s) \cdot(\gamma'(s)\times \gamma''(s))}{\|\gamma''(s)\|^2} \end{align} $$

### Smooth but not parametrized by arc-length

$$ \begin{align} T(t) &= \frac{f'(t)}{\|f'(t)\|}, \\ \kappa(t) &= \frac{\|f'(t) \times f''(t)\|}{\|f'(t)\|^3},\\ N(t) &= \frac{(f'(t)\times f''(t)) \times f'(t)}{\|(f'(t)\times f''(t)) \times f'(t)\|} ,\\ B(t) &= \frac{f'(t) \times f''(t)}{\|f'(t) \times f''(t)\|}, \\ \tau(t) &= \frac{f'''(t) \cdot(f'(t)\times f''(t))}{\|f'(t) \times f''(t)\|^2} \end{align} $$
