---
tags:
  - VectorAnalysis
  - DifferentialGeometry
---
Subjects: [[Vector Analysis]]
Links: [[Functions of Bounded Variation on R]], [[Vector-valued functions of R]], [[Differentiabilty of vector valued functions of R]]

**Def:** A continuous function $f:[a,b] \to \Bbb R^n$ is called a **path** in $\Bbb R^n$ from $f(a)$ to $f(b)$. The path is differentiable, $\cal C^1$ or smooth if the function $f$ is respectively differentiable, $\cal C^1$ or smooth. If $f(a) = f(b)$ then it is a closed path.

**Def:** A path $f:[a,b] \to \Bbb R^n$ is called ***simple*** if $f$ is not closed $f$ is injective, if it is closed $f$ is injective on $[a,b)$ or $(a,b]$.

**Prop:** Let $f:[a,b] \to \Bbb R^n$ is a nonsimple path with a finite number of self-intersections, then we can partition it into simple paths.

**Def:** Let $f:[a,b] \to\Bbb R^n$, and $\cal P$ be a partition of $[a,b]$, we can define the length of the polygonal path with vertices as $f(x_0), \dots, f(x_n)$ , in this order.

$$ \Lambda(f, \cal P) := \sum_{k =1}^n \|f(x_k)-f(x_{k-1})\| $$

The length of $f$ is:

$$ \Lambda_f(a,b)=\Lambda(f) := \cal\sup_{P \in \wp} \Lambda(f, P) $$

if $\Lambda(f) < \infty$, then $f$ is called _**rectifiable**_, otherwise is **************nonrectifiable**************.

There are two notations: $\Lambda(f)$ is primarily used when the domain is clear or unchanging, and $\Lambda_f(a,b)$ to make the domain clear or changing

**Th:** Let $f:[a,b]=I\to\Bbb R^n$, $f$ is rectifiable iff every component $f_k$ is of bounded variation on $[a,b]$. If $f$ is _********rectifiable********_ then for any $1\le k\le n$:

$$ V(f_k) \le \Lambda (f) \le \sum_{k = 1}^n V(f_k) $$

********Th:******** Let $f:[a,b] \to\Bbb R^n$ be rectifiable and $c \in(a,b)$, then:

$$ \Lambda_f(a,b) = \Lambda_f(a,c) + \Lambda_f(c,b) $$

**Th:** If $f:[a,b] \to\Bbb R^n$ and $f \in \cal C^1$, then $f$ is rectifiable, and:

$$ \Lambda(f) = \int_a^b \|f'\| $$

********Th:******** Let $f:[a,b]\to\Bbb R^n$ and $g:[c,d]\to\Bbb R^n$ be two $1-1$ continuous parametrizations of the curve $C$, them ${\Lambda(f) = \Lambda(h)}$.

********Th:******** Let $f:[a,b]\to\Bbb R^n$ and $g:[c,d]\to\Bbb R^n$ equivalent $\cal C^1$ parametrizations of the curve $C$, them ${\Lambda(f) = \Lambda(h)}$.

**Cor:** All smooth parametrizations of a smooth simple arc in $\Bbb R^n$ have the same length.

**Def:** The ******_length $\Lambda(C)$_ of a smooth simple arc in $C$ in $\Bbb R^n$ is the length of any smooth parametrization of $C$.

**Def:** A $\cal C^1$ parametrization $\gamma:E\subseteq\Bbb R\to\Bbb R^n$ of a curve $C$ in $\Bbb R^n$ is a *path-length parametrization* of $C$ if $\|\gamma'(s)\| =1$ for all $s \in E$.

### Arc-lenght Parametrization
**Def:** Let $f:D\subseteq \Bbb R\to\Bbb R^n$ be smooth parametrization of a curve $C$ in $\Bbb R^n$. Choose a base point $p\in D$. Then *arc-length* function based at $p$ is the function $\lambda:D\subseteq\Bbb R\to \Bbb R$ defined by:
$$ s(t) =\lambda(t) := \int_p^t \|f'(u)\|\,du = \Lambda_f(p,t) \quad t\in D $$

where $s= \lambda(t)$ represents the distance travelled by the particle in the interval between $p$ and $t$. The speed of $f$ at time given by:

$$ \lambda'(t) = \|f'(t)\| > 0 $$

Thus $\lambda$ is invertible.

********Th:******** For any smooth parametrization $f:D\subseteq\Bbb R\to\Bbb R^n$ of a curve $C$ in $\Bbb R^n$ there’s is a arc-length parametrization $\gamma:E\subseteq\Bbb R\to\Bbb R^n$ of $C$ which is properly equivalent to $f$.

Chose a base point $p \in D$, and let $\lambda:D\to \Bbb R$ be arc-length function based at $p$. $E = \lambda(D)$, then $\gamma = f\circ\lambda^{-1}:E\subseteq\Bbb R\to\Bbb R^n$ is an equivalent parametrization by arc-length. This process is called re-parametrization by arc-length.

**Def:** Let $f:[a,b]\to\Bbb R^n$ be a path. The *inverse path* is defined to be the function $f^-:[a,b]\to\Bbb R^n$ where:

$$ f^-(t) = f(a+b-t) $$

### Concatenation of Paths
Def Let $f:[a,b] \to \Bbb R^n$ and $g:[c,d]\to\Bbb R^n$ be paths in $\Bbb R^n$ where ${f(b) = g(c)}$. The product or concatenation path $h=fg=f\oplus g= f*g =f+g:[a, b+d-c]\to\Bbb R^n$ is defined by:

$$ h(t) = \begin{cases} f(t) &\quad t\in[a,b] \\ g(c-t+b) &\quad t\in [b, b+d-c] \end{cases} $$