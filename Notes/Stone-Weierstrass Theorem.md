---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Space of Continuous Functions From Rn to Rm]], [[Continuous Function Spaces]], [[Compactness in Metric Spaces]], [[Dense Subsets]]

### Using Polygonal functions
A continuous function $\phi: [a,b]\to \Bbb R$ is _polygonal_ iff, there’s a partition $\mathcal P$ of $[a,b]$, such that for in each subinterval $[x_i, x_{i+1}]$, $\phi$ is linear.

Let $f:[a,b] \to \Bbb R$ be continuous, and $\varepsilon >0$, there’s a polygonal function $\phi$ satisfying:

$$ \forall x \in [a,b](|\phi(x) - f(x)| < \varepsilon) \iff \|\phi - f\|_\infty < \varepsilon $$

In particular a special kind of polygonal function can be approximated by Taylor polynomials on a closed interval, ${h_a: \Bbb R \to \Bbb R}$, and $a\in\Bbb R$, $h_a(x) = 0$, whenever $x \le a$, and $h_a(x) = x-a$, $x>a$. or:

$$ h_a(x) = \frac{x-a+|x-a|}{2} $$

Every polygonal function $\phi$ can be written as a linear combination of $h_a$, where $a\in \Bbb R$.

Thus, let $\phi: [a,b]\to \Bbb R$ be a polygonal function, then:

$$ \forall \varepsilon >0\exists p \in \Bbb R[x](\|p-\phi\|_\infty < \varepsilon) $$
### Using [[Bernstein Polynomials]]
Most importantly: given a continuous function $f:[0,1]\to \Bbb R$, consider the sequence of polynomials:

$$ B_n(x;f) = \sum_{\nu = 0}^n f\left(\frac{\nu}{n}\right) b_{\nu, n}(x) $$

and this sequence of polynomials are called the *Bernstein polynomials of $f$*, and  $B_n(x;f) \rightrightarrows f$, proving the Weierstrass Approximation Theorem.

### Using Landau Kernels

We define the *Landau kernels* by $$L_n(x) = \begin{dcases}\frac{(1-x^2)^n}{c_n} & |x| \le 1 \\
0 &|x| \ge 1 \end{dcases}$$
Where $c_n$ is a normalisation constant so that $\int_\Bbb R L_n(x)\, dx = 1$. We see that $\{L_n\}_{n\ge 0}$ is a [[Good Kernels and Convergence in Fourier Analysis|family of good kernels]] as $n \to \infty$. Then if $f$ is a continuous function supported in $[-1/2, 1/2]$, then $(f*L_n)(x)$ is a sequence of polynomials on $[-1/2, 1/2]$ which converges uniformly to $f$. 

This is using the [[Fourier Transform in R]]

### Weierstrass Approximation Theorem

Let $f: [a,b]\to \Bbb R$ be continuous, and $\varepsilon > 0$, then there’s a polynomial $p:[a,b]\to \Bbb R$ such that: $\|f-p\|_\infty <\varepsilon$

$$ \forall f \in \mathcal C[a,b]\forall\varepsilon > 0 \exists p \in \Bbb R[x](\|f-p\|_\infty <\varepsilon) $$

As a corollary, given any continuous function $f$, then there’s a sequence of polynomials $(p_n)$ such that $p_n \rightrightarrows f$.

As another corollary, $\mathcal C^0[a,b]$ is separable since it has the dense countable subset of $\mathbb Q[x]$.

As a trivial consequence of the Weierstrass Approximation Theorem, if $f$ has a continuous derivative on $[a,b]$, and $\varepsilon >0$, then there’s a $p \in \Bbb R[x]$ such that: ${\|f-p\|_\infty, \|f'-p'\|_\infty < \varepsilon}$ .

Let $K$ be a compact metric space. If we take a took at ${\cal C}^0(K)$, this is not only a vector space, but it also has a product meaning if $f, g \in {\cal C}^0(K)$, then $fg \in {\cal C}^0(K)$, this means that ${\cal C}^0(K)$ is an $\Bbb R-$algebra

We can see that in general ${\cal C}^0(X)$ for any topolgical space $X$, is an $\Bbb R-$algebra

Let $\cal A$ be a subset of ${\cal C}^0(K)$ with the following properties:

- $\lambda \phi +\mu \psi \in$ for any $\lambda, \mu \in \Bbb R$ and $\phi, \psi \in {\cal A}$
- $\phi\psi \in \cal A$ for any $\phi, \psi \in \cal A$
- $1 \in \cal A$, meaning the constant function $1$
- Given $x_1\ne x_2$ in $K$, then there exists $\phi \in A$ such that $\phi(x_1) \ne \phi(x_2)$

The first three conditions can be shorted into saying that $\cal A$ is a [[K-Algebra|subalgebra]] of ${\cal C}^0(K)$, and the last one is that separates points

We need the following lemmas for the Stone-Weiestrass Theorem

Let $x_1 \ne x_2$ in $K$, and $c_1, c_2\in \Bbb R$, there’s $\psi \in \cal A$ such that $\psi (x_1) = c_1$ and $\psi(x_2) = c_2$

The closure $\overline {\cal A}$ of $\cal A$ in ${\cal C}^0(K)$ is also a subsalgebra of ${\cal C}^0(K)$

If $\phi \in \overline {\cal A}$, then $|\phi| \in \overline {\cal A}$ (This uses the Weiestrass Approximation Theorem)

If $\phi, \psi \in \overline {\cal A}$, then $\max \{\phi, \psi\}, \min \{\phi, \psi\} \in \overline {\cal A}$

### Stone-Weiestrass Theorem
Let $K$ be a compact metric space and let $\cal A$ be a subalgebra of ${\cal C}^0(K)$ with unity that separates points. Then $\cal A$ is dense in ${\cal C}^0(K)$, i.e., for every continuous function $f:K \to \Bbb R$, there exists a sequence $(\phi_k)$ of functions in $\cal A$ that converges uniformly to $f$ in $K$

Let’s denote $\Bbb R[x_1, \dots, x_n]$ be the set of all real polynomials with $n$ variables

Let $K$ be a compact subspace of $\Bbb R^n$. Then, given a continuous function $f:K\to \Bbb R$, there exist a sequence of polynomials $(p_k)$ in $\Bbb R[x_1, \dots, x_n]$ that converge uniformly to $f$ in $K$

Let $\Bbb S^1=\{(\cos\theta, \sin \theta) \in \Bbb R^2 \mid 0\le \theta\le 2\pi\}$ the unit circle in $\Bbb R^2$. Then any continuous function $f:\Bbb S^1 \to \Bbb R$ is the limit of functions of the form

$$ \phi(\cos\theta, \sin\theta) =a_0+ \sum_{k = 1}^n(a_k \cos k\theta +b_k \sin\theta) $$

with $a_i ,b_i \in \Bbb R$ and $n \in \Bbb N$

Let $X, Y$ be compact metric spaces. Any continuous function $f:X\times Y\to \Bbb R$ is the uniform limit of functions of the form

$$ \phi(x, y) = \sum_{k = 1}^n f_k (x)g_k(y) $$

with $f_1, \dots f_n \in {\cal C}^0(X)$ and $g_1, \dots, g_n \in {\cal C}^0(K)$ and $n \in \Bbb N$
### Stone-Weierstrass Theorem in $\Bbb R^n$
Let $A \subseteq \Bbb R^n$ be a compact set and let $\mathcal B \subseteq \mathcal C(A, \Bbb R)$ satisfy
- $\mathcal B$ is an algebra
- the constant function $x \mapsto 1$ lies in $\mathcal B$
- $\mathcal B$ separate points; that is; for $x, y \in A$ if $x \ne y$ then there is an $f \in \mathcal B$ such that $f(x) \ne f(y)$
Then $\mathcal B$ is dense in $\mathcal C(A, \Bbb R)$