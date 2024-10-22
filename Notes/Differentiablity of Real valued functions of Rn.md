---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Real-valued Functions of Rn]], [[Limits and Continuity of real valued functions of Rm]], [[Differentiability of Vector valued functions of Rn]]
# Linear Approximation and Differentiability
### Directional Derivatives

**********Def:********** Let $\mathbb{S}^{n} \subseteq \Bbb R^{n+1}$ is called the $n-$sphere, and it is defined as ${\mathbb{S}^n=\{x\in \mathbb{R}^{n+1} \mid \| x\|=1\}}$ , and an $n-$sphere of radius $r$ is defined as: ${\mathbb S^n(r) =\{x \in \Bbb R^{n+1} \mid \|x\|=r\}}$. If $x \in \mathbb S^n$ are gonna be denoted as ${\hat x}$.

**********Def:********** Let $f:S\subseteq \Bbb R^n \to \Bbb R$, $x \in S$ and and ${\hat u} \in \mathbb{S}^{n-1}$. We say $f$ _is differentiable at $\mathbf x$ and in the direction_ ${\hat u}$ if, the following limit exists:

$$ \lim_{h \to 0}\frac{f({x}+h {\hat u})-f(\mathbf x)}{h} $$

in that case we say that the ************directional derivative************ of $f$ at $x$ in the direction $\mathbf{\hat u}$ is denoted as $\def\pain{{\hat u}} \nabla_\pain f(x),f'_\pain (x), D_\pain f(x), \partial_\pain f(x), \frac{\partial f}{\partial \pain}$ with their value corresponding to the limit above.

********Th:******** Let $f:S\subseteq \Bbb R^n\to \Bbb R$, $x\in S$ and ${{\hat u} \in \mathbb{S}^{n-1}}$ if $\partial_{{\hat u}} f(x)$ exists then:

$$ \lim_{h\to 0} f(x+h{\hat u}) = f(x) $$

**********Th:********** Let $f,g :S\subseteq\Bbb R^n\to \Bbb R, x\in S$ and ${{\hat u} \in \mathbb{S}^{n-1}}$ if both $\partial_{{\hat u}} f(x)$ and $\partial_{{\hat u}} g(x)$ exists then:

- $\partial_{{\hat u}} (f+g) (x)$ exists and $\partial_{{\hat u}} (f+g) (x)= \partial_{{\hat u}} f(x) +\partial_{{\hat u}} g(x)$
- Given $\alpha \in \Bbb R$, then $\partial_{{\hat u}} (\alpha f) (x)$ exists and $\partial_{{\hat u}} (\alpha f) (x) = \alpha \partial_{{\hat u}} f(x)$
- $\partial_{{\hat u}} (fg) (x)$ exists and $\partial_{{\hat u}} (fg) (x) = f(x) \partial_{{\hat u}} g (x) + \partial_{{\hat u}} f (x) g(x)$
- If $g$ is continuous at $x$ and $g(x) \ne 0$, then $\partial_{{\hat u}} (f/g) (x)$ exists and:

$$ \frac{\partial}{\partial{{\hat u}}}\left(\frac{f}{g}\right) (x) = \frac{g(x)\partial_{{\hat u}} f (x) - f(x) \partial_{{\hat u}} g (x)}{g^2(x)} $$

************Chain Rule:************ Let $f:S\subseteq\Bbb R^n\to \Bbb R, x\in S$, ${{\hat u} \in \mathbb{S}^{n-1}}$ and ${f(S) \subseteq (a,b)}$. If $g:(a,b) \subseteq \Bbb R \to \Bbb R$ is differentiable at $f (x)$ and $\partial_{{\hat u}} f (x)$ exists, then $\partial_{{\hat u}} (g \circ f)( (x)$ exists and:

$$ \partial_{{\hat u}} (g \circ f) (x) = g'(f(x)) \partial_{{\hat u}} f (x) $$

**********Def:********** Let ${a,b \in \Bbb R^n}$, then the set ${[a,b]} \subseteq \Bbb R^n$ is defined as:

$$ {[a,b]}:= \{ta+(1-t)b \in \Bbb R^n \mid 0 \le t \le 1\} $$

****MVT for Directional Derivatives:****

Let $f:S\subseteq \Bbb R^n\to \Bbb R$, and ${a, b} \in S$ where ${a \ne b}$, ${{\hat u} = {(b-a)/\|b-a\|} \in \mathbb{S}^{n-1}}$. If $\partial_{{\hat u}}f (x)$ exists for all $x \in {[a,b]}$, then there’s an $t' \in (0, {\|b-a\|})$ such that ${c = a +t' {\hat u}}$,

$$ f(b) - f(a)= {\|b-a\|}\partial_{{\hat u}}f(c) $$

******Def:****** Let $f:S\subseteq \Bbb R^n\to \Bbb R$, considering the special case of the directional derivative, such that ${\hat u} \in \{e_i\}_{i=1}^n$ then $\partial_{{e_i}}f$ is called the ********************************_partial derivative with respect to $x_i$ at $x_0$_ usually denoted as: $\partial_{x_i} f, \partial_i f, \frac{\partial f}{\partial x_i}, f_x, f'_x, \frac{\partial}{\partial x_i} f$ .

****MVT for Partial Derivatives:****

Let $f:S\subseteq \Bbb R^n\to \Bbb R$, and $\mathbf {a, b} \in S$ where $\mathbf {a \ne b}$, and ${\mathbf{b-a}=(b-a)e_i}$. For some ${1 \le i \le n}$, $\partial _i f(x)$ exists for all $x\in\mathbf{ [a,b]}$, then there’s a $t' \in (0, |b-a|)$ such that ${\mathbf{c =a} +t'e_i \in \mathbf{[a,b]}}$ that

$$ f(\mathbf b) - f(\mathbf a) = (b-a) \partial_i f(\mathbf c) $$

### Total Derivative

**********Def:********** For a set $D \subseteq \Bbb R^n$ with $x_0\in D$, let $D_{x_0} = \{h \in \Bbb R^n \mid {x_0+h} \in D\}$.

We will consider the set $D$ as open subset of $\Bbb R^n$, to simplify things.

********Def:******** Consider a function $f:D\subseteq \Bbb R^n \to \Bbb R$, where $D$ is an open subset of $\Bbb R^n$, and let $x\in D$. The *************_difference function ${\delta f_{x}:D_x\subseteq\Bbb R^n \to \Bbb R^n}$_ is defined by:

$$ \delta f _{x}(h) = f({x+h}) -f(x) $$

**********Def:********** Let $g:N\subseteq \Bbb R^n\to \Bbb R$ and $g^*:M\subseteq \Bbb R^n\to \Bbb R$ be two functions defined on open domains $N$ and $M$ such that $\mathbf 0 \in N\cap M$. We say that $g$ and $g^*$ *********************************_closely approximate each other near $\mathbf 0\in \Bbb R$_ if

$$ g(\mathbf 0) = g^*(\mathbf 0) \text{ and } \lim_{\mathbf{h\to 0}}\frac{g(h) -g^*(h)}{\|h\|}=0 $$

Equivalently, $g$ and $g^*$ closely approximate each other near $\mathbf 0$ if there exists a function ${\eta:N\cap M \subseteq \Bbb R^n \to \Bbb R}$ such that:

- $g(h) = g^*(h) + \|h\|\eta(h)$
- $\lim_{{h\to \mathbf 0}}\eta(h) = 0$

**********Def:********** A function $f:D\subseteq\Bbb R^n\to \Bbb R$ which is defined on an open subset $D\in \Bbb R^n$ is ******differentiable****** at $x\in D$ if the difference function ${\delta f _x:D_x \subseteq \Bbb R^n \to \Bbb R}$ can be closely approximated by a linear function near $\mathbf 0$.

Equivalently, $f$ is differentiable at $\mathbf p$ if there exists a linear function ${L :\Bbb R^n \to \Bbb R}$ and a function ${\eta:D_p \subseteq \Bbb R^n \to \Bbb R}$ such that, given $\mathbf h \in D_p$:

$$ f({x+h}) -f(x) = L(h)+\|h\|\eta(h) $$

and

$$ \lim_{h\to \mathbf{0}}\eta(h) = 0 $$

************Th:************ A function $f:D\subseteq\Bbb R^n \to\Bbb R$ which is differentiable at $x\in D$ is also continuous there.

********Th:******** Let $f:D\subseteq\Bbb R^n \to \Bbb R$ be differentiable at $x\in D$. Then there sis only one close linear approximation to $\delta{f_ x}$ near $\mathbf 0$.

**********Def:********** If $f:D\subseteq\Bbb R^n \to\Bbb R$ is differentiable at $x\in D$, then the _******unique******_ close linear approximation to $\delta{f_ x}$ is denoted by $df_{x}$ and it is called the _************differential************_ of $f$ at $x$.

****Th:**** If $f:D\subseteq\Bbb R^n \to \Bbb R$ and $x \in D$, if $f$ is differentiable at $x$, then for any ${\hat u} \in \mathbb{S}^{n-1}$ $\partial_{{\hat u}}f(x)$ exists, and it is equal to $df_{x} ({\hat u})$.

- Properties
    
    Let $f,g:D\subseteq\Bbb R^n\to \Bbb R^m$ , $x \in D$ if $f$ and $g$ are differentiable at $x$. Then
    
    $f+g$ is differentiable at $x$
    
    $$ d(f+g)_x = df_x+dg_x $$
    
    Let $\lambda \in \Bbb R$, then $\lambda f$ is differentiable at $x$
    
    $$ d(\lambda f)_x = \lambda df_x $$
    
    $fg$ is differetiable at $x$
    
    $$ d(fg)_x = f(x)dg_x + g(x)df_x $$
    
    if $g(x) \ne 0$, then $f/g$ is differentiable at $x$
    
    $$ d\left(\frac{f}{g}\right)_x = \frac{1}{g^2(x)}(g(x)df_x -f(x)dg_x) $$
    

********Cor:******** Let $f:D\subseteq\Bbb R^n \to\Bbb R$ be differentiable at $x\in D$. Then:

- the partial derivative $\partial_i f(x)$ exists and it is equal to $df_{x}(e_i)$, for each $1 \le i \le n$.
- for all $h \in \Bbb R^n$,
    
    $$ df_{\mathbf p}(h) = \sum_{i=1}^n (h \cdot e_i) {\partial_i f}(x) $$
    
- the $1 \times n$ matrix representing $df_{x}$, with respect to the canonical basis is:
    
    $$ J_f(x) = \left[\partial_1 f(x) \cdots \partial_nf(x)\right] $$
    
    The matrix $J_f(x)$ representing the differential $df_{x}$ is called the ****************Jacobian matrix**************** or $f$at $x$. Other notation regarding the Jacobian is
    
    $$ J_f(p)=\frac{\partial f}{\partial \mathbf x}(x) $$
    

********Th:******** The function $f:D\subseteq\Bbb R^n\to \Bbb R$ is differentiable at $x\in D$ iff:

- all partial derivatives of $f$ exist at $x$
    
- there exists a function $\eta:D_{x} \subseteq \Bbb R^n\to \Bbb R$ such that for all ${h\in D_{x}}$
    
    $$ f({x+h}) - f( x) = \sum_{k = 1}^n(h \cdot e_k) \partial_kf(x) +\|h\|\eta(h) $$
    
    where
    
    $$ \lim_{h\to\mathbf{0}}\eta(h) = 0 $$
    

********Th:******** Let $f:D\subseteq\Bbb R^n \to\Bbb R$, $\mathbf x \in D$, $r > 0$ such that $B_r(\mathbf x) \subseteq U$. If for any $1 \le i \le n$, and all $\mathbf y \in B_r(\mathbf x)$, $\partial_i f(\mathbf y)$ exists and is continuous at $\mathbf x$. Then, $f$ is differentiable at $\mathbf x$.

********Th of Pain:******** Let $f:D\subseteq\Bbb R^n \to\Bbb R$, $\mathbf x \in D$, $r > 0$ such that $B_r(\mathbf x) \subseteq U$. If for any $1 \le i \le n$, and all $\mathbf y \in B_r(\mathbf x)$, $\partial_i f(\mathbf y)$ exists and for $2 \le i \le n$ , $\partial_if$ is continuous at $\mathbf x$. Then, $f$ is differentiable at $\mathbf x$.

**********Def:********** A function $f:D\subseteq\Bbb R^n \to\Bbb R$, whose partial derivatives exists throughout a neighbourhood of $\mathbf x\in D$ and are continuous at $\mathbf x$, is said to be _**********************continuously differentiable**********************_ at $\mathbf x$.

**********Def:********** A function $f:D\subseteq\Bbb R^n \to\Bbb R$ is said to be _continuously differentiable or a $\cal C^1$ function,_ if it is continuously differentiable at each point $\mathbf x\in D$

****Euler's Homogeneous Function Theorem****

Let $f$ be a homogeneous function of order $n$, meaning

$$ f(t x) = t^n f(x) $$

Then we get that

$$ \nabla f(x) \cdot x = n f(x) $$

### Tangent Space

Let $G \subseteq \Bbb R^n$ be the graph a differentiable function ${f:D\subseteq\Bbb R^{n-1} \to \Bbb R}$. For any ${\mathbf x_0\in D}$, the set $T \in \Bbb R^n$ with the equation

$$ x_n = f(\mathbf x_0)+df_{\mathbf x_0}(\mathbf{x-x_0}) $$

where $\mathbf x_0 =(x_1, \dots, x_{n-1})\in \Bbb R^{n-1}$. $T$ is called the **************_tangent space to $G$ at ${(\mathbf x_0, f(\mathbf x_0))}$_

### Chain Rule

Let $g:E\subseteq \Bbb R\to\Bbb R^n$ be defined on an open interval $E$ and let ${f:D\subseteq\Bbb R^n\to\Bbb R}$ be defined on an open set $D$ such that $g(E)\subseteq D$. Define $F:E\subseteq\Bbb R\to\Bbb R$ to be the composite function given by ${F(t) = (f\circ g)(t)}$

Suppose that $g$ is differentiable at $a \in E$ and that $f$ is differentiable at ${g(a)\in D}$. Then $F$ is differentiable at a $a$ and its differential is given by:

$$ dF_{a} =d(f\circ g)_{a}= df_{g(a)} \circ dg_a $$

Thus:

$$ J_F(a) = J_{f\circ g}(a) = J_f(g(a))J_g(a) $$

Equivalently:

$$ \frac{dF}{dt} = \sum_{k = 1}^n \frac{\partial f}{\partial x_k} \frac{dx_k}{dt} $$

where the partials are evaluated at $g(a)$ and $x'_k$ is evaluated at $a$.