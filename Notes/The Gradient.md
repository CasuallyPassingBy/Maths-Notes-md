---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Differentiablity of Real valued functions of Rn]]

**********Def:********** Let $f:D\subseteq\Bbb R^n\to\Bbb R$ be a function that is differentiable at ${x\in D}$. The ***********_gradient of $f$ at $\mathbf x$_ is defined to be the vector

$$ \begin{align*} (\operatorname{grad}f)(x) = \nabla f(x) &= \begin{pmatrix} \partial_1f(x)\\ \partial_2f(x)\\ \vdots \\ \partial_nf(x) \end{pmatrix} \end{align*} $$

********Th:******** Let $f:D\subseteq\Bbb R^n\to\Bbb R$ be a function that is differentiable at ${\mathbf x\in D}$. Then:

- The differential $df_{x}$ is related to the gradient by:

$$ df_{x}(h) = h \cdot \nabla f(x) $$

- Similarly, let ${\hat u} \in \mathbb S^{n-1}$, the directional derivative ${\partial_{{\hat u}}f(x)}$ is expressible by:

$$ \frac{\partial f}{\partial{\hat u}}(x) = {\hat u} \cdot \nabla f(x) $$

### Chain Rule

Let $g:E\subseteq \Bbb R\to\Bbb R^n$ be defined on an open interval $E$ and let ${f:D\subseteq\Bbb R^n\to\Bbb R}$ be defined on an open set $D$ such that $g(E)\subseteq D$. Define $F:E\subseteq\Bbb R\to\Bbb R$ to be the composite function given by ${F(t) = (f\circ g)(t)}$

Suppose that $g$ is differentiable at $a \in E$ and that $f$ is differentiable at ${g(a)\in D}$. Then $F$ is differentiable at a $a$ and

$$ F'(a) = (f\circ g)'(a) = \nabla f(g(a)) \cdot g'(a) $$

**********Def:********** Let $f:D\subseteq\Bbb R^n\to \Bbb R$ be a differentiable function at $\mathbf x \in D$ and $\nabla f(x) \ne \mathbf 0$. Then:

- The directional derivative $\partial _{{\hat u}}f(x)$ takes the maximum value iff $\mathbf{\hat u}$ is the unit vector in the direction $\nabla f(x)$. The maximum value is ${\|\nabla f(x)\|}$.
- $\partial_{{\hat u}}f(x) = 0$ iff ${\hat u}$ is a unit vector orthogonal to $\nabla f(x)$

************Def:************ A set $S\subseteq \Bbb R^n$ is called a _******smooth surface******_ if $S$ is a level set of a $\cal C^1$ function $f:D\subseteq\Bbb R^n\to\Bbb R$, such that $\nabla f(x) \ne 0$ for $x \in S$.

**********Def:********** A function $f:D\subseteq \Bbb R^n\to \Bbb R$ is said to be _******smooth******_ if it is continuously differentiable and if ${\nabla f(x) \ne \mathbf 0}$ for all $x \in D$.

********Th:******** The graph of a $\cal C^1$ function ${f:D\subseteq\Bbb R^{n-1}\to\Bbb R}$ is a smooth surface in $\Bbb R^n$.

**********Th:********** Let $S$ be a surface which is a level set of a smooth function ${f:D\subseteq\Bbb R^{n}\to\Bbb R}$ and $x$ be a point in $S$. Then any differentiable path ${\gamma:E\subseteq\Bbb R\to \Bbb R^n}$ such that $\gamma(E) \subseteq S$ and any ${a\in E}$ such that $\gamma(a) = x$, the tangent vector $\gamma'(a)$ is orthogonal to the vector $\nabla f(x)$.

********Def:******** Let the surface $S$ in $\Bbb R^n$ be a level set of a smooth function ${f:D\subseteq\Bbb R^n\to \Bbb R}$. Then, for any ${x_0\in S}$,

- the straight line through $x_0$ in the direction $\nabla f(x_0)$ is called the ************normal line************ to the surface $S$ at $x_0$.
- the set of all vectors $x$ such that ${({x-x_0})\cdot\nabla f(x_0) =0}$ is called the *****************_tangent space to $S$ at $\mathbf x_0$._

********Def:******** Let the surface $S$ in $\Bbb R^n$ be a level set of a smooth function ${f:D\subseteq\Bbb R^n\to \Bbb R}$, ${\phi:U \subseteq \Bbb R^n \to \Bbb R}$, and $x_0 \in S$, then we define the ********************_normal derivative of $\phi$ at $x_0$ over the set $S$ as_

$$ \frac{\partial \phi}{\partial \hat n} = \nabla \phi \cdot \hat n $$

where

$$ \hat n= \frac{\nabla f(x_0)}{\|\nabla f(x_0)\|} $$

********Th:******** Let the surface $G\subseteq \Bbb R^n$ be a level set of a smooth function ${F:D\times \Bbb R\subseteq\Bbb R^n\to \Bbb R}$ and also the graph of a $\cal C^1$ function ${f:D\subseteq\Bbb R^{n-1}\to \Bbb R}$. Then in the sense of stated just above, the equation of the tangent space to $G$ at ${(x_0, f(x_0)) \in G}$ is

$$ x_m = f(x_0) + \sum_{k =1}^{n-1}(x_k- x_{0,k})\frac{\partial f}{\partial x_k}(x_0) $$

********Th:******** Let $D$ be an open path connected subset of $\Bbb R^n$ and let ${f:D\to\Bbb R}$ be a differentiable function such that $\nabla f(x) \ne \mathbf 0$ for all $x\in D$. Then $f$ is constant function.