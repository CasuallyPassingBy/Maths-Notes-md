---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Higher Order Derivatives and Taylor's Theorem for Real valued functions of Rn]], [[Real-valued Functions of Rn]]

******************Def:****************** The function $f$ is said to have a _local maximum_ at $x_0 \in D$ if there is a neighborhood $N$ of $x_0$ such that for all $x \in N$:

$$ f(x) \le f(x_0) $$

The function $f$ is said to have a _local minimum_ at $x_0 \in D$ if there is a neighborhood $N$ of $x_0$ such that for all $x\in N$:

$$ f(x) \ge f(x_0) $$

**********Def:********** We say that the function $f$ has a _local extremum_ at $x_0 \in D$ if $f$ has a local maximum or minimum at $x_0$. In this case $x_0$ is called an _**extremal point**_ of $f$.

********Th:******** Let $f:D\subseteq\Bbb R^n\to \Bbb R$ have a local extremum at $x_0 \in D$ and let ${\hat u }\in \mathbb S^{n-1}$ such that ${\partial_{{\hat u}}f(x_0)}$ exists. Then $\partial_{{\hat u}}f(x_0)=0$.

**********Cor:********** Let $f:D\subseteq\Bbb R^n\to\Bbb R$ be a differentiable function with a local extremum at $x_0\in D$. Then

- $\partial_i f(x_0) =0$, for all $1 \le i \le n$
- $df_{x_0}:\Bbb R^n\to \Bbb R$ is the zero transformation.

********Def:******** Let $f:D\subseteq\Bbb R^n\to \Bbb R$ be a differentiable function. Any point $x \in D$ for which $df_x$ is the zero transformation is called a _critical point_ of $f$. Equivalently the critical points are the points ${x\in D}$ for which $\partial _i f(x)= 0$ for all $1 \le i \le n$.

**********Def:********** A point $\mathbf p \in D$ is called a _************saddle point************_ of a differentiable function $f:D\subseteq\Bbb R^n\to \Bbb R$ if $\mathbf p$ is a critical point but $f$ doesn’t have a local extremum at $\mathbf p$.

**********Def:********** Let $f:D\subseteq\Bbb R^n\to \Bbb R$ be a function where all second-partial derivatives of $f$ exists at ${x_0\in D}$. Then *******_Hessian Matrix $\mathbf H$ of $f$ at $x_0$ is_ an $n\times n$ matrix defined as:

$$ (\mathbf H_f(x_0))_{ij} = \frac{\partial^2 f}{\partial x_i \partial x_j}(x_0) $$

If the second partial derivatives are all continuous, then the Hessian matrix is a symmetric matrix.

If we examine the second degree polynomial of $f$ at a critical point $x_0$.

$$ T_2(h) = f(x_0) + \nabla f(x_0)\cdot h + \frac{1}{2} h^\top \mathbf H_f(x_0) h $$

If we examine the second degree polynomial of $f$ at a critical point $x_0$. We obtain that:

$$ f(x_0+h) - f(x_0) = \frac{1}{2}\sum_{i, j =1}^n h_ih_j \frac{\partial^2 f}{\partial x_i \partial x_j}(x_0) + \|h\|^2 \eta (h) $$

We can simplify the sum as a [[Quadratic Forms|quadratic form]] of $\mathbf h^\top \mathbf H_f(\mathbf p) \mathbf h$, thus

$$ f(x_0+h) - f(x_0) = \frac{1}{2} h^\top \mathbf H_f(\mathbf p) h +\|h\|^2\eta(h) $$

We know that $\mathbf H_f(x_0)$ that is diagonalizable with real eigenvalues. In particular, let’s consider $\lambda_{max}$ and $\lambda_{min}$, the maximum and minimum eigenvalues. Then

$$ \lambda_{min}\|x_0\|^2 \le h^\top \mathbf H_f(x_0) h \le \lambda_{max} \| h\|^2 $$

******************Cor:****************** Suppose $f:D\subseteq \Bbb R^n\to \Bbb R$ be a $\mathcal C^2$ has a critical point at $x_0 \in D$. Then:

- If $\mathbf H_f(x_0)$ is a positive definite matrix, then $f$ has a local minimum of $x_0$
- If $\mathbf H_f(x_0)$ is a negative definite matrix, then $f$ has a local maximum of $x_0$
- If $\mathbf H_f(x_0)$ is indefinite matrix, then $x_0$ is a saddle point of $f$.

**********Def:********** Let $f:D \subseteq \Bbb R^n\to \Bbb R$ be a $\cal C^2$ function with a critical point $x_0$. The determinant of $\mathbf H_f(x_0)$ is called *******_the Hessian determinant or discriminant of $f$ at $x_0$_ denoted as $\Delta_f(x_0)$

********Th:******** Let $f:D \subseteq \Bbb R^n\to \Bbb R$ be a $\cal C^2$ function with a critical point $\mathbf p$. Then

- $f$ has a local minimum if $\partial_1^2 f(x_0)>0$ and $\Delta_f(x_0) >0$
- $f$ has a local maximum if $\partial_1^2 f(x_0)<0$ and $\Delta_f(x_0) >0$
- $f$ has a saddle point if $\Delta_f(x_0) < 0$