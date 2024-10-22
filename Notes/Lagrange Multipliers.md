---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Implicit Function Theorem in Rn]], [[Inverse Function Theorem in Rn]], [[Differentiability of Vector valued functions of Rn]], [[The Gradient]]

Let:
- $g_1, \dots ,g_m:D\subseteq \Bbb R^n\to \Bbb R$ be $\cal C^1$ functions on $D$
- The set $S\subseteq \Bbb R^n$ defined as    $$ S=\{x\in \Bbb R^n \mid \forall 1\le i\le m [g_i(x) =0]\} $$
- $x_0 \in S$ such that $\nabla g_1(x_0), \dots, \nabla g_m(x_0)$ be linearly independent
    

Then $f:D\subseteq\Bbb R^n\to \Bbb R$ be $\cal C^1$ on $D$ such that $f$ local extrema on $\mathbf x_0$ on the set $S$ then there exists $\lambda_1, \dots, \lambda_m \in \Bbb R$ such that

$$ f(x_0) = \sum_{k =1}^m \lambda_kg_k(x_0) $$

Additionally we can use an auxiliary function, sometimes called the _Lagrangian_ or the **Lagrange function**, $\mathcal L:D\times\Bbb R^{m} \to \Bbb R$ to be of the form

$$ \mathcal L(x_1, \dots, x_n, \lambda_1, \dots, \lambda_m) = f(x_1, \dots, x_n) -\sum_{k =1}^m\lambda_k g(x_1, \dots, x_n) $$

and we are looking for

$$ \nabla \mathcal L = \mathbf 0 \iff \begin{cases} \nabla f(x) = \sum_{k=1}^m \lambda_k \nabla g(x) \\ g_1(x) =\cdots = g_m(x) =0 \end{cases} $$

**Cor:** If $f$ is constrained to the set $S$, then has a local extremum at $x_0$ then $\nabla f(x_0)$ is orthogonal to $S$ at $x_0$.

**Def:** The special case of the Hessian matrix of the Lagrange function, we get the **Bordered Hessian,** to make the notation a bit lighter we will use ${(x, \lambda)}$ coordinates where $\lambda\in \Bbb R^m$, and $\mathbf x\in D$

$$ \mathbf H_{\mathcal L} = \begin{pmatrix} \dfrac{\partial^2 \mathcal L}{\partial \lambda^2} & \dfrac{\partial^2 \mathcal L}{\partial \lambda \partial \mathbf x} \\ \left(\dfrac{\partial^2 \mathcal L}{\partial \lambda \partial \mathbf x}\right)^{\mathsf{T}} & \dfrac{\partial^2 \mathcal L}{\partial \mathbf x^2} \end{pmatrix} $$

which can be used to find if it’s the critical point $\mathbf x_0\in S$ is a local maxima, minima or a saddle point.

### Lagrange Multiplier Strategy for finding Absolute Maxima and Minima on Regions with a boundary

Let $f:D\subseteq\Bbb R^n\to\Bbb R$ be differentiable, and $D$ be close and bounded region $D=U\cup \partial U$, $U$ open in $\Bbb R^n$, with $\partial U$ being smooth

- Locate all critical points of $f$ in $U$
- Use the method of Lagrange Multipliers to locate all the critical points of $f|_{\partial U}$
- Compute all the values of $f$ at the critical points
- Select the largest and smallest