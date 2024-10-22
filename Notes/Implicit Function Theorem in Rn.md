---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Differentiability of Vector valued functions of Rn]], [[Inverse Function Theorem in Rn]]

**Def:** Let $f:D\subseteq \Bbb R^{n+m}\to \Bbb R^m$ be differentiable at a point ${({a, b}) =(a_1,\dots a_n, b_1, \dots, b_m) \in D}$ is defined, then _********left-hand panel of the Jacobian is defined as:********_

$$ \left(\frac{\partial f}{\partial \mathbf x}{(a,b)}\right)_{ij} = \frac{\partial f_i}{\partial x_{j}} {(a,b)} \quad \text{for } 1\le i \le m \text{ and } 1\le j \le n $$

Similarly the _********right-hand panel of the Jacobian********_ is defined as:

$$ \left(\frac{\partial f}{\partial \mathbf y} {(a,b)} \right)_{ij} = \frac{\partial f_i}{\partial y_{j}} {(a,b)} \quad \text{for } 1\le i, j \le m $$

and

$$ J_f{(a,b)} = \left( \frac{\partial f}{\partial \mathbf x}{(a,b)} \quad \frac{\partial f}{\partial \mathbf y}{(a,b)} \right) $$

## Implicit Function Theorem

Let $f:D\subseteq\Bbb R^{n+m}\to \Bbb R^n$ be a differentiable function with coordinates ${(x,y)}$. If we fix a point ${(a,b)}$, with $f{(a,b) = \mathbf 0}$, and if the right-hand panel of the Jacobian

$$ \frac{\partial f}{\partial\mathbf y}{(a,b)} = \left(\frac{\partial f_i}{\partial y_j}{(a,b)}\right) $$

is invertible, then there exists an open set $U\subseteq\Bbb R^n$ containing $\mathbf{a}$ such that there’s a unique differentiable function $g:U\subseteq \Bbb R^n\to \Bbb R^m$ such that $g({a) =b}$ , and $f(x, g(x)) = \mathbf 0$, for all $x \in U$. Moreover the Jacobian matrix of $g$ in $U$ is given by

$$ J_g(\mathbf x) = -\left(\frac{\partial f}{\partial \mathbf y}(x, g(x))\right)^{-1} \left( \frac{\partial f}{\partial \mathbf x}(x, g(x))\right) $$

If $f$ is $\mathcal C^k, k\ge 1$ then so is $g$.

## Implicit Function Theorem (Paez)

Let $g_1, \dots, g_m : U \subseteq \Bbb R^m \times \Bbb R^k \to \Bbb R$ be of class $\mathcal C¹$ on $U$. If $$S=\{(x, y) = (x_1, \dots, x_m, y_, \dots, y_k) \in U \mid g_i(x, y) = 0 \forall i \in \{1, \dots, m\}\}$$and $(x_0, y_0)  \in S$ is such that the matrix$$\begin{bmatrix}
\frac{\partial g_1}{\partial x_1}(x_0, y_0) &\cdots & \frac{\partial g_1}{\partial x_m}(x_0, y_0) \\
\vdots & \ddots & \vdots \\
\frac{\partial g_m}{\partial x_1}(x_0, y_0) &\cdots& \frac{\partial g_m}{\partial x_m}(x_0, y_0)
\end{bmatrix}$$is invertible, then there exists $\delta>0$, $V \subseteq \Bbb R^k$ an open subset, and a function $h:V\subseteq \Bbb R^k \to \Bbb R^m$ of class $\mathcal C¹$, such that $y_0 \in V$, $h(y_0) = x_0)$ and $(h(y), y) \in B_\delta((x_0, y_0))\cap S$ for all $y\in V$. This properties make $h$ unique.  

### Morse’s Lemma
Let $A \subseteq \Bbb R^n$ be open, $f: A\to \Bbb R$ be of class $\cal C^\infty$ for which $0$ is a non-degenerate critical point, namely $\nabla f = 0$ and the hessian at $0$ has the trivial kernel. Then in some neighborhood $U$ of $0$ there is a local $\mathcal C^\infty$ coordinate system, namely a $\mathcal C^\infty$ diffeomorphism

$$ \varphi= (x_1, \dots, x_n): U \to V\subseteq\Bbb R^n $$

with $\varphi (0) =0$ such that the map $\tilde f = f\circ \varphi$ (namely $\varphi$ in the $x$-coordinates) takes the form

$$ {\tilde f (x) = f(0) - x_1^2 -\cdots -x^2_\lambda +x_{\lambda +1}^2 + \cdots x_n^2} $$

Here the number $\lambda$ is the *********Morse Index********* of the critical point $0$ of $f$, that is the number of negative eigenvalues of the Hessian of $f$ at $0$, counted multiplicities. The assumption $\mathcal C^\infty$ may be relaxed to $\mathcal C^k$ for $k \ge 2$, but in this case the change of variables $\varphi$ is in general only of class $\mathcal C^{k-2}$. This said we can approximate it using a [[Quadratic Forms|quadratic form]] .