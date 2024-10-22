---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Limits and Continuity of Vector valued functions of Rn]], [[Differentiabilty of vector valued functions of R]]

**********Def:********** Given a function $f:D\subseteq\Bbb R^n\to \Bbb R^m$, where $D$ is an open subset of $\Bbb R^n$, and $x\in D$, the *******************_difference function $\delta f_x: D_x\subseteq\Bbb R^n\to \Bbb R^m$_ is defined by

$$ \delta f_x (h) = f({x+h}) -f(x) $$

******************Def:****************** Let $g:N\subseteq \Bbb R^n\to \Bbb R^m$ and $g^*:M\subseteq\Bbb R^n\to \Bbb R^m$ be two functions whose open domains both contain $\mathbf 0$. We will say that $g$ and $g^*$ **********_closely approximates each other near $\mathbf 0$_ if there is a function $\eta: M\cap N\to\Bbb R^m$ such that:

- $g(h) -g^*(h) = \|h\|\eta(h)$
- $\lim_{{h\to \mathbf 0}}\eta(h) = \mathbf 0$

**********Def:********** A function $f:D\subseteq\Bbb R^n\to \Bbb R^m$, defined on an open subset $D$ of $\Bbb R^n$, is _differentiable at_ $x\in D$ if the difference function $\delta f_x$ can be closely approximated by a linear function ${L:\Bbb R^n\to \Bbb R^m}$ near $\mathbf 0$. The function is said to be _differentiable_ if it is differentiable everywhere in $D$.

We can also define it in another way:
Let $f:U\subseteq \Bbb R^n \to \Bbb R^n$ and $x_0 \in U$, we say that $f$ is differentiable on $x_0$ if there's a linear map $L: \Bbb R^n \to \Bbb R^m$ such that
$$
\lim_{x\to x_0}\frac{\|f(x)-(f(x_0)+L(x-x_0))\|}{\|x-x_0\|}
$$

and we call $L$ is called the derivative, and this is equivalent to the definition above. 

********Th:******** A function $f:D\subseteq\Bbb R^n\to \Bbb R^m$ is differentiable at $x \in D$ iff each of the component functions $f_i:D\subseteq\Bbb R^n \to \Bbb R$, $1 \le i \le m$, is differentiable at $x\in D$.

**********Cor:********** If $f:D\subseteq\Bbb R^n\to \Bbb R^m$ is differentiable at $x\in D$, then it is also continuous at $x$.

**********Cor:********** Let $f:D\subseteq\Bbb R^n \to \Bbb R^m$ be differentiable at $x\in D$. Then there is only one close linear approximation of $\delta f_x$ near $\mathbf 0$. It is the linear function

$$ L(h) = \begin{pmatrix} d(f_1)_x(h)\\ d(f_2)_x(h)\\ \vdots\\ d(f_n)_x(h) \end{pmatrix} $$

**********Def:********** Let $f:D\subseteq\Bbb R^n\to \Bbb R^m$ be differentiable $x \in D$. Then the _****unique****_ close linear approximation of $\delta f_x$ at $\mathbf 0$ is denoted as $df_x$ and it is called the differential of $f$ at $x$.

**********Th:********** If the function $f:D\subseteq\Bbb R^n\to \Bbb R^m$ is differentiable at $x_0 \in D$, then all partial derivatives $\partial_i f_j(x_0)$ exists and the matrix representing the differential $df_{x_0}$ with respect to the standard bases of $\Bbb R^n$ and $\Bbb R^m$ is the $m \times n$

$$ J_f(x_0)=\frac{\partial f}{\partial \mathbf x}(x_0) = \left[\partial_j f_i(x_0)\right]= \left[\frac{\partial f_i}{\partial x_j}(x_0)\right] $$

- Properties
    Let $f,g :D\subseteq\Bbb R^n\to \Bbb R^m$ , $x_0\in D$ and $\lambda \in \Bbb R$ are differentiable at $\mathbf p$ then
    
    $f+g$ is differentiable at $x_0$
    $$ d(f+g)_{x_0} = df_{x_0} +dg_{x_0} \quad \text{ or } \quad D(f+g)(x_0) = Df(x_0) +Dg(x_0)$$
    
    $\lambda f$ is differentiable at $x_0$
	    $$ d(\lambda f)_{x_0} = \lambda df_{x_0} \quad \text{ or }\quad D(\lambda f)(x_0)= \lambda Df(x_0)$$
    
    $f \cdot g$ is differentiable at ${x_0}$
    

******Def:****** Let $f:D\subseteq\Bbb R^n\to \Bbb R^m$ be differentiable at $x \in D$. The $m\times n$ matrix $J_f(x)$ is called _the Jacobian of $f$ at_ $x$. When $n = m$ the determinant of the square matrix $J_f(x)$ is denoted by

$$ \det J_f(x)= \frac{\partial(f_1, \dots, f_n)}{\partial(x_1, \dots, x_n)}(x) $$

********Th:******** In the special case of considering ${\hat u}\in \mathbb S^{n-1}$ and $df_x({\hat u})$ then it is obtained that ^5fd4a0

$$Df(x)(\hat u) =df_x({\hat u}) = \begin{pmatrix} \partial_{{\hat u}}f_1(x) \\ \partial_{{\hat u}}f_2(x) \\ \vdots\\ \partial_{{\hat u}}f_n(x) \end{pmatrix} = \frac{\partial f}{\partial {\hat u}}(x) = \partial_{{\hat u}}f(x) $$

Similarly:

$$ Df(x)(e_i)=df_x(e_i) = \begin{pmatrix} \partial_{i}f_1(x) \\ \partial_{i}f_2(x) \\ \vdots\\ \partial_{i}f_n(x) \end{pmatrix} = \frac{\partial f}{\partial x_i}(x) = \partial_{i}f(x) $$

**********Th:********** Consider a function $f:D\subseteq\Bbb R^n\to \Bbb R^m$ which is defined on an open subset $D$ of $\Bbb R^n$. If all the partial derivatives $\partial_i f_j$ exist throughout $D$, $1 \le i \le n$, $1\le j\le m$, and if they are all continuous at $x \in D$, then $f$ is differentiable at $x$.

********Th:******** Let $D\subseteq \Bbb R^n$ open $f:D\to \Bbb R^m$ is differentiable in $D$. Then for all $x_0 \in D$ there is a constant $M>0$ and $\delta_0>0$ such that $\|{x-x}_0\|<\delta_0$ implies ${\|f(x)-f(x_0)\|\le M\|x-x_0\|}$. This can be understood to be that $f$ is locally Lipschitz.

************Def:************ Let $D$ be an open subset of $\Bbb R^n$. A function $f:D\subseteq \Bbb R^n\to\Bbb R^m$ all of whose partial derivatives are continuous in $D$ is said to be _continuously differentiable_ on $D$. Any such function is also said to be a $\cal C^1$ function.

**********Def:********** A function $g:S\subseteq\Bbb R^n\to\Bbb R^m$ whose domain is not an open subset of $\Bbb R^n$ is said to be $\cal C^1$function if can be extended to a $\mathcal C^1$ function $f:D\subseteq\Bbb R^n\to\Bbb R^m$ defined on an open set $D$ containing $S$, such that $f$ and $g$ agree on all points in $S$.

**********Def:********** A function $f:D\subseteq\Bbb R^n\to\Bbb R^m$ is said to be $\cal C^k$ if each of the function $f_i$ is $\cal C^k$ functions. In the case that $D$ isn’t open, then if it can be extended into a an open domain.

************Def:************ A function $f:D\subseteq\Bbb R^n\to \Bbb R^m$ is _******smooth******_ if $f$ is a $\cal C^1$ function and if for all $x \in D$, the Jacobian $J_f(x)$ is of the maximum possible rank $\min(m,n)$. A function $g:S\subseteq\Bbb R^n\to \Bbb R^m$ whose domain is not an open subset of $\Bbb R^n$ is said to be _******smooth******_ if it can be extended to a smooth function on an open domain containing $S$.

****************Th:**************** Let $f:D\subseteq\Bbb R^n\to\Bbb R^m$ be a differentiable function defined on an open path-connected subset $D$ of $\Bbb R^n$. If the differential $df_x = Df(x)$ is the zero function for all $x\in D$ then $f$ is a constant function.

**********Cor:********** Let $f,g:D\subseteq\Bbb R^n\to \Bbb R^m$ be differentiable functions and an open path-connected subset $D$ of $\Bbb R^n$. If $df_x = dg_x$ for al $x\in D$, then there exists $k\in \Bbb R^m$ such that $f(x)= g(x)+k$ for all $x \in D$.

### Chain Rule
**************Lemma:************** Suppose that $G:\Bbb R^k\to \Bbb R^n$ is closely approximated near $\mathbf 0 \in \Bbb R^k$ by a linear function $M:\Bbb R^k\to \Bbb R^n$ and that $F:\Bbb R^n\to\Bbb R^m$ is closely approximated near $\mathbf 0 \in \Bbb R^n$ by a linear function $L:\Bbb R^n\to \Bbb R^m$. Then $F\circ G:\Bbb R^k \to \Bbb R^m$ is closely approximated by $\mathbf 0 \in \Bbb R^k$ by the linear function $L \circ M:\Bbb R^k\to\Bbb R^m$.

********Lemma:******** Let $g:E\subseteq\Bbb R^k\to\Bbb R^n$ and $f:D\subseteq\Bbb R^n\to \Bbb R^m$ be functions such that $\mathbf a \in E$, and $g[E] \subseteq D$, then

$$ \delta(f\circ g)_{a} = \delta f_{g(a)} \circ \delta g_a $$

Let $g:E\subseteq\Bbb R^k\to\Bbb R^n$ be defined on an open subset $E$ of $\Bbb R^k$ and let $f:D\subseteq\Bbb R^n\to \Bbb R^m$ be defined on an open subset $D$ of $\Bbb R^n$ such that $g[E]\subseteq D$. Define $F:E\subseteq\Bbb R^k \to \Bbb R^m$ to be ${F= f\circ g}$

Suppose that $g$ is differentiable at $a \in E$ and $f$ is differentiable at $g(a) \in D$. Then $F$ is differentiable at $\mathbf a\in E$, and its differentiable is given by

$$ dF_a = df_{g(a)}\circ dg_a \quad \text{ or } \quad DF(a) = Df(g(a))\circ Dg(a)$$

Furthermore, the Jacobian matrix of $F$ is given at $a$ is given by

$$ J_F(a) = J_f(g(a))J_g(a) $$

### Mean-Value Theorem
Let $f:D\subseteq\Bbb R^n\to \Bbb R^m$ be a differentiable function whose open set domain contains the points $x$ and ${x+h}$ and the segment joining them. Then the corresponding to unit vector ${{\hat u}\in \Bbb R^n}$ there is $\theta \in (0,1)$

$$ (f({x+h})-f(x))\cdot {\hat u} = df_{{x+\theta h}}(h) \cdot {\hat u}  = Df(x+\theta h)\cdot \hat u$$