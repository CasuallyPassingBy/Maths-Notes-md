---
tags:
  - VectorAnalysis
  - DifferentialGeometry
---
Subjects: [[Vector Analysis]]
Links: [[Limits and Continuity of Vector Valued Functions of R]], [[Differentiability of Vector valued functions of Rn]]

## Differentiability

**********Def:********** Let $f: D\subseteq \Bbb R\to\Bbb R^n$ is differentiable on $x_0 \in D$ if the limit exists:

$$ \lim_{x\to a}\frac{f(x)-f(x_0)}{x-x_0} $$

then its value is the derivative of $f$ on $x_0$, usually denoted as $f'(x_0)$.

********Th:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$ is differentiable on $x_0 \in D$, iff for each $1 \le i \le n$ component functions $f_i$ is differentiable at $x_0$. If $f$ is differentiable at $x_0$, then:

$$ \begin{align*} f'(t) &= \begin{pmatrix} f'_{1}(t) \\ f'_{2}(t) \\ \vdots \\ f'_{n}(t) \end{pmatrix} \end{align*} $$

********Def:******** Let $f: D\subseteq \Bbb R\to\Bbb R^n$ is differentiable on $x_0 \in D$

- The derivative $f'(x_0)$ will also be called the tangent vector of $f$ at $x_0$
- If $f'(x_0) \ne 0$, then the straight line in $\Bbb R^n$ through $f(x_0)$ with direction $f'(x_0)$ will be called the ****_tangent line of $f$ at $x_0.$_ It is the set $\{f(x_0) + tf'(x_0)\mid t \in \Bbb R\}$

**********Def:********** Let $f: D\subseteq \Bbb R\to\Bbb R^n$ is differentiable if $f$ is differentiable at each $x \in D$. Then the function $f': D\subseteq \Bbb R\to\Bbb R^n$ whose image is $f'(x)$ for every $x \in D$.

********Th:******** Let $f, g: D\subseteq \Bbb R\to\Bbb R^n$ and $\phi:D\subseteq \Bbb R\to\Bbb R$ be differentiable at $x_0 \in D.$ Then:

- $f+g$ is differentiable at $x_0$, and $(f+g)'(x_0) = f'(x_0)+g'(x_0)$
- $f\cdot g$ is differentiable at $x_0$, and $(f\cdot g)'(x_0) = f'(x_0)\cdot g(x_0)+f(x_0)\cdot g'(x_0)$ Alternatively it can be expressed using the inner product notation: ${\langle f, g\rangle}'(x_0) = \langle f'(x_0), g(x_0)\rangle +\langle f(x_0), g'(x_0)\rangle$
- $\phi f$ is differentiable at $x_0$, and $(\phi f)'(x_0) = \phi(x_0)f'(x_0)+\phi'(x_0)f(x_0)$
- If $n = 3$, then $f\times g$ is differentiable at $x_0$, and ${(f\cdot g)'(x_0) = f'(x_0)\cdot g(x_0)+f(x_0)\cdot g'(x_0)}$

**Th:** Let $f: D\subseteq \Bbb R\to\Bbb R^n$ is differentiable, and $\|f (x)\|$ is constant for every $x \in D$, then $f(x)$ and ${f'(x)}$ are orthogonal for every $x \in D$.

**Def:** Let $f: D\subseteq \Bbb R\to\Bbb R^n$ is differentiable, and $f'$ is also continuous, then $f$ is a $\cal{C}^1$ function on $D$, or $f \in \mathcal{C}^1(D)$. If the $k$th derivative is continuous then $f$ is a $\cal{C}^k$ function on $D$, or ${f\in \mathcal{C}^k(D)}$.

**Def:** A subset $C \subseteq\Bbb R^n$ is a curve if there is a $\cal C^1$ function $f:D\subseteq \Bbb R\to \Bbb R^n$, where $D$ is an interval where $f(D) = C$. The function $f$ is called a $\cal{C}^1$ parametrization of $C$.

**Def:** Let $f: D\subseteq \Bbb R\to \Bbb R^n$ and $h:E\subseteq\Bbb R\to\Bbb R^n$ be $\cal{C}^1$ parametrization of the curve $C$. Then $h$ is equivalent to $f$ if there is a differentiable function $\phi$ from $E$ onto $D$ such that:

- $h = f\circ \phi$
- $\phi'(x) > 0$ for all $x \in E$ or $\phi'(x) <0$ for all $x \in E$

In the case that $\phi$ is **strictly increasing**, then we say that $f$ and $h$ are _properly equivalent_. In the other hand, if $\phi$ is **strictly decreasing**, the we say that $f$ and $h$ are **equivalent with opposite orientations**.

********Th:******** In this sense this type of equivalence does form an equivalence relation on the class of all $\cal{C}^1$ parametrization of $C$.

********Chain Rule:******** Let $\phi:E\subseteq\Bbb R\to\Bbb R$ and $f:D\subseteq\Bbb R\to\Bbb R^n$ be differentiable functions and let $\phi(E) \subseteq D$. Then ${f\circ \phi}$ is differentiable and for each $x \in E$:

$$ (f\circ \phi)(x) = f'(\phi(x))\phi'(x) $$

********Th:******** Let $f: D\subseteq \Bbb R\to \Bbb R^n$ and $h: E\subseteq \Bbb R\to \Bbb R^n$ be equivalent $\cal C^1$ parametrizations of a curve $C$ in $\Bbb R^n$ related by a differentiable function $\phi :E \to D$. Let $h = f\circ \phi$ and $\phi$ be strictly monotonic, then whenever $\phi(u) = t$ then:

- The tangent vector of $f$ at $t$, if non-zero, is parallel to the tangent vector of $h$ at $u$. The sign depends if $f$ and $h$ have the same orientation or opposite.

**Def:** A function $f: D\subseteq\Bbb R\to\Bbb R^n$ is said to be **smooth/regular** if it is $\cal C^1$ and if $f'(t) \ne 0$ for all ${t\in D}$

**Def:** A curve $C$ in $\Bbb R^n$ is a (smooth) simple arc if $C$ has a $1-1$ function (smooth) $\cal C^1$ parametrization of the form ${f:[a,b] \subseteq\Bbb R\to\Bbb R^n}$.

The points $f(a)$ and $f(b)$ are called the endpoints of the arc. The function $f$ is called a simple parametrization of $C$.

**Th:** Let $C$ be simple arc in $\Bbb R^n$ simply parametrized by a smooth injective function ${f:[a,b] \to \Bbb R^n}$. Then, any smooth parametrization $h:[c,d] \to \Bbb R^n$ of $C$ is injective and equivalent to $f$.

**Cor:** Let $q$ be a point in a smooth simple arc $C \subseteq \Bbb R^n$. Then all smooth parametrizations of $C$ associate the same tangent line with $q$.

**********Def:********** Let $C$ be smooth simple arc in $\Bbb R^n$ parametrized by smooth function $f:[a,b] \to \Bbb R^n$. The pair $(C, [f])$, where $[f]$ is the set of all smooth parametrizations of $C$ which are properly equivalent to $f$, is called an **************************oriented smooth simple arc**************************.

********Th:******** Let $f:[a,b] \to \Bbb R^n$ and $h :[c,d] \to\Bbb R^n$ be $1-1$ parametrizations of a simple arc $C$ in $\Bbb R^n$. Then there is unique $\phi$ from $[a,b]$ onto $[c,d]$ such that $h = f\circ \phi$. Moreover $\phi$ is continuous and strictly monotonic. In particular:

- If $\phi$ is strictly increasing then $f(a) = h(c)$ and $f(b) = h(d)$
- If $\phi$ is strictly decreasing then $f(a) = h(d)$ and $f(b) = h(c)$

**Def:** A function $f:[a,b] \to \Bbb R^n$ is said to be piecewise $\cal C^1$ (piecewise smooth) if there is a partition $\cal P =\{x_i\}_{i=0}^m$ of $[a,b]$ such that for each $1 \le k \le m$ the function $f$ is restricted to the subinterval $[x_{k-1}, x_k]$ is $\cal C^1$ (smooth).

Note that in the cases of $x_k$ the derivatives might not exists, but their left and right derivative must exist.
## Differentiability and linear approximation

**Def:** Let the set $f:D\subseteq\Bbb R \to \Bbb R^n$, and $p \in D$. Let’s consider the function ${\delta f_p:D_p\subseteq\Bbb R \to \Bbb R^n}$ where $D_p = \{h\in \Bbb R \mid p+h \in D\}$,
$$ \delta f_p(h) :=f(p+h)-f(p) $$

********Th:******** A function $f:D\subseteq \Bbb R\to \Bbb R^n$ is differentiable at $p\in D$ iff there exists a linear function $L:\Bbb R\to \Bbb R^n$ and a function $\eta:D_p\subseteq \Bbb R\to \Bbb R^n$ such that:

- $\delta f_p(h) = L(h) + h\eta(h)$, for all $h \in D_p$
- $\lim_{h\to 0} \eta(h) = \bf{0}$

**********Def:********** Let $g:N\subseteq \Bbb R\to \Bbb R^n$ and $g^*:M\subseteq\Bbb R \to \Bbb R^n$ be two functions on intervals $N$ and $M$ where $0 \in N \subseteq M$. We say that $g^*$ **********_closely approximates $g$ near $0$ if:

$$ \lim_{h\to 0} \frac{g(h)-g^*(h)}{h} = 0 $$

for $h \in N$.

**Cor:** A function $f:D\subseteq \Bbb R\to \Bbb R^n$ is _differentiable_ at $p\in D$ iff the difference function ${\delta_{f,p}:D_p\subseteq \Bbb R\to \Bbb R^n}$ can be closely approximated by a linear function near $0$. If such a close linear approximation exists then it is unique and is $L_{f,p}$

**Def:** the function $f:D\subseteq \Bbb R\to \Bbb R^n$ is **differentiable** at $p \in D$ if there is a linear function $df_p:\Bbb R\to\Bbb R^n$ (called the **differential** of $f$ at $p$) and a functions ${\eta:D_p\subseteq\Bbb R \to \Bbb R}$ such that:

- $f(p+h) -f(p) = df_p(h) + |h|\eta(h)$, for all $h \in D_p$
- $\lim_{h\to 0}\eta(h) = \bf 0$

Other notations for the differential of $f$ at $p$ are: $D_pf, Df(p), df_p, d_pf$ or $L_{f,p}$

**Def:** If the function $f:D\subseteq \Bbb R\to \Bbb R^n$ is differentiable at $p\in D$, then the ${n \times 1}$ matrix $J_{f}(p)$ which represents the linear transformation $df_p:\Bbb R\to\Bbb R^n$ with respect to the standard bases is called the *Jacobian* of $f$ at $p$.

The Jacobian of $f$ at $p$ can also be denoted as $J_f(p)$.

********Chain Rule:******** Let $\phi:E\subseteq \Bbb R\to\Bbb R$ and $f:D\subseteq \Bbb R\to \Bbb R^n$ be differentiable functions and let $\phi(E) \subseteq D$. Then $f\circ \phi: E\subseteq \Bbb R\to \Bbb R^n$ is differentiable and
$$ d(f\circ \phi)_p= df_{\phi(p)}\circ d\phi_p $$

with the corresponding Jacobian relation
$$ J_{f\circ \phi}(p) = J_f(\phi(p))J_\phi(p) $$