---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Tags: [[Lipschitz Uniformity with Jordan Measure]], [[Inverse Function Theorem in Rn]], [[Riemann Integral in Rn]]
[[Cubes in Rn]]
# Linear Case
**Def:** There are special linear maps, in particular we are gonna look at the elemental ones, meaning:

- $E_1 \in \mathcal L(n,n)$, where $E_1 = (x_1, \dots, \lambda x_k, \dots, x_n)$ for some $\lambda \in \Bbb R^*$, and some index $k\in\{1,\dots, n\}$, which multiplies a coordinate by non-zero scalar.
- $E_1 \in \mathcal L(n,n)$, where $E_1 = (x_1, \dots, x_k +\lambda x_j, \dots, x_n)$ for some $\lambda \in \Bbb R^*$, and some index $j,k\in\{1,\dots, n\}$, which multiplies a coordinate by non-zero scalar and adds it to another.

**************Lemma:************** Let $R = \prod_{i = 1}^n [a_i, b_i] \subseteq\Bbb R^n$ be a rectangle and let $T:\Bbb R^n\to \Bbb R^n$ is an [[Elementary Matrix Operations and Elementary Matrices|elemental linear map]], then $T[R]$ is Jordan-measurable, and

$$ J(T[R]) = |\det T| m(R) $$

From linear algebra we defined the determinant of a transformation.
********Lemma:******** Let $D\subseteq \Bbb R^n$ be Jordan-measurable and $T:\Bbb R^n\to \Bbb R^n$ be an elemental linear map, then $T[D]$ is Jordan-measurable and

$$ J(T[D]) = |\det T|J(D) $$

********Th:******** Let $D\subseteq \Bbb R^n$ be Jordan-measurable and $T:\Bbb R^n\to \Bbb R^n$ be [[The Rank of a Matrix and Matrix Inverses|non-singular linear map]], then $T[D]$ is Jordan-measurable and

$$ J(T[D]) = |\det T|J(D) $$

************Prop:************ If for any $m< n$, we will define the set

$$ P_m =\{(x_1, \dots, x_n)\in \Bbb R^n \forall i \in \{m+1, \dots, n[x_i = 0]\}\} $$

Then $P_m$ has $0$ Lebesgue measure, or $\lambda(P_m) = 0$.

****************Lemma:**************** Let $T:\Bbb R^n\to \Bbb R^n$ be a singular linear map, such that $T[\Bbb R^n]$ has dimension $m < n$, then there exists an isomorphism $\varphi:\Bbb R^n\to\Bbb R^n$ such that

$$ \phi[T[\Bbb R^n]] = P_m $$

This has a similar idea to the [[Inverse Function Theorem in Rn#Straightening-Out Theorem V.3.|Straightening-Out Theorem V.3.]].

********Prop:******** Let $D\subseteq \Bbb R^n$ be Jordan-measurable and $T:\Bbb R^n\to \Bbb R^n$ be a singular linear map, then $T[D]$ is Jordan-measurable and

$$ J(T[D]) = |\det T|J(D) =0 $$

### Important Theorem

Thus it is always true that if $D\subseteq \Bbb R^n$ be Jordan-measurable and $T:\Bbb R^n\to \Bbb R^n$ be a linear map, then $T[D]$ is Jordan-measurable and

$$ J(T[D]) = |\det T|J(D) $$

---

# General Case

**********Lemma:********** Let $\Omega \subseteq \Bbb R^n$ be an open set and $K \subseteq \Omega$ a compact set. If $g:\Omega \to \Bbb R^n$ is a $\cal C^1$ function on $\Omega$, for all $x \in K$ we have that $\det dg_x \ne 0$, and $g$ is injective on $\operatorname{int}(K)$ then for any $\varepsilon \in (0,2)$, exists a $\delta >0$, such that for any cube $C \subseteq \operatorname{int}(K)$ with dimension $s< \delta$ and center in $a$, has to

$$ \left(1-\frac{\varepsilon}{2}\right)|\det (dg_a)| m(C) \le J(g[C]) \le \left(1 +\frac{\varepsilon}{2}\right)|\det (dg_a)| m(C) $$

**************Lemma:************** Let $\Omega \subseteq \Bbb R^n$ be an open set and $K \subseteq \Omega$ a compact set. If $g:\Omega \to \Bbb R^n$ is a $\cal C^1$ function on $\Omega$, for all $x \in K$ we have that $\det dg_x \ne 0$, and $g$ is injective on $\operatorname{int}(K)$ then for any $\varepsilon \in (0,1)$ exists a $\delta >0$, such that for any rectangle $R \subseteq \operatorname{int}(K)$ with dimensions less than $\delta$, and for all $x \in R$

$$ (1-\varepsilon) |\det (dg_x)|m(R) \le J(g[R]) \le (1 + \varepsilon) |\det (dg_x)|m(R) $$

## Change of Variable Theorem

Let $\Omega \subseteq\Bbb R^n$ be an open set $D\subseteq \Omega$ Jordan-measurable, such that $\operatorname{cl}(D) \subseteq \Omega$. Let ${g:\Omega \to \Bbb R^n}$ be $\cal C^1$ function on $\Omega$, injective on $\operatorname{int}(D)$ such that $\det(dg_x) \ne 0$ for all ${x \in \operatorname{int}(D)}$. If $f: g[D] \to \Bbb R$ is bounded and continuous then

$$ \int_{g[D]} f = \int_D(f\circ g)|\det dg| $$

### Stronger Version

Let $\Omega \subseteq\Bbb R^n$ be an open set $D\subseteq \Omega$ Jordan-measurable, such that $\operatorname{cl}(D) \subseteq \Omega$. Let ${g:\Omega \to \Bbb R^n}$ be $\cal C^1$ function on $\Omega$, injective on $\operatorname{int}(D)\setminus B$, where $J(B) =0$ such that $\det(dg_x) \ne 0$ for all ${x \in \operatorname{int}(D)}\setminus A$, where $J(A) =0$. If $f: g[D] \to \Bbb R$ is bounded and continuous then

$$ \int_{g[D]} f = \int_D(f\circ g)|\det dg| $$

---

# Important Examples

## In $\Bbb R^2$

### Polar

The most important one is we can get that let $g$ be change of variable such that ${g: \Bbb R^{\ge 0} \times [0,2\pi] \to \Bbb R^2}$

$$ g(r,\theta) = (r\cos(\theta), r\sin(\theta)) $$

this is called the canonical polar transformation and, it is important to notice that $g$ isn’t injective in particular when $r = 0$, and when $\theta = 0, 2\pi$. Since it is set of $0$ Jordan measure we can still apply it.

$$ |\det dg_{(r, \theta)}| = r $$

which is only $0$ at $r = 0$, which is a set of $0$ Jordan measure.

## In $\Bbb R^3$

### Cylindrical

Similar to Polar Coordinates we can get that let $g$ be change of variable such that ${g: \Bbb R^{\ge 0} \times [0,2\pi]\times \Bbb R \to \Bbb R^3}$

$$ g(r,\theta, z) = (r\cos(\theta), r\sin(\theta), z) $$

this is called the canonical polar transformation and, it is important to notice that $g$ isn’t injective in particular when $r = 0$, and when $\theta = 0, 2\pi$. Since it is set of $0$ Jordan measure we can still apply it.

$$ |\det dg_{(r, \theta)}| = r $$

which is only $0$ at $r = 0$, which is a set of $0$ Jordan measure.

### Spherical

Let $g$ be change of variable such that ${g: \Bbb R^{\ge 0} \times [0,2\pi]\times [0, \pi] \to \Bbb R^3}$

$$ g(\rho,\theta, \phi) = (\rho\cos(\theta)\sin(\phi), \rho\sin(\theta)\sin(\phi), \rho\cos(\phi)) $$

this is called the canonical polar transformation and, it is important to notice that $g$ isn’t injective in particular when $\rho = 0$, when $\theta = 0, 2\pi$, and $\phi = 0, \pi$. Since it is set of $0$ Jordan measure we can still apply it.

$$ |\det g_{(\rho, \theta, \phi)}| = \rho^2 \sin(\phi) $$

which is only $0$ at $\rho = 0$ and $\phi = 0, \pi$, which is a set of $0$ Jordan measure.

## In $\Bbb R^n$

### Sphere in $n$ dimensions

It is a generalization of spherical coordinates with one radial coordinate $r$, and $n-1$ angular coordinates $\phi_1, \dots, \phi_{n-1}$, where $\phi_1, \dots, \phi_{n-2}$ over $[0, \pi]$ and $\phi_{n-1}$ over $[0, 2\pi]$ with the following transformation ${g: \Bbb R^{\ge 0} \times [0, \pi]^{n-2}\times [0, 2\pi] \to\Bbb R^n}$ with ${g(r, \phi_1, \dots, \phi_{n-1}) = (x_1,\dots, x_n)}$ and it is called the canonical $n-1$ spherical transformation,

$$ \begin{align*} x_1 &= r \cos(\phi_1) \\ x_2 &= r \sin(\phi_1) \cos(\phi_2) \\ x_3 &= r \sin(\phi_1) \sin(\phi_2) \cos(\phi_3) \\ &\,\,\,\vdots\\  
x_{n-1} &= r \sin(\phi_1) \cdots \sin(\phi_{n-2}) \cos(\phi_{n-1}) \\  
x_n &= r \sin(\phi_1) \cdots \sin(\phi_{n-2}) \sin(\phi_{n-1}) .\end{align*} $$

which is injective except when $\rho =0$, $\phi_k = 0, \pi$ for $k <n-1$, and $\phi_{n-1} = 0, 2\pi$. Since it a set of Jordan-measure $0$, we can still apply the theorem.

While talking about the Jacobian we can get several results, first of we can define $J_n$ to be the sequence of Jacobian of the canonical $n-1$ spherical transformation, then by using Laplace expansion in the final column. We get the recurrence relation

$$ |J_n| =| J_{n-1}|r\prod_{k = 1}^{n-2} \sin(\phi_k) $$

using induction, we can get the close form of

$$ |J_n| = r^{n-1}\prod_{k = 1}^{n-2}\sin^{n-1-k}(\phi_k) $$

Since $J_n =0$ only happens when $r = 0$, or when $\phi_k = 0, \pi$ for $k < n-1$. It is a set of $0$ Jordan measure thus we can use the Change of Variable Theorem.