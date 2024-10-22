---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Differentiablity of Real valued functions of Rn]], [[Taylor Series in R]]

**********Def:********** The $n$th-order directional derivative of the function ${f:D\subseteq\Bbb R^n\to\Bbb R}$ in the direction of an unit vector $\mathbf{\hat u} \in \mathbb{S}^{n-1}$ is the function ${\partial_{{\hat u}}^n f:D\to \Bbb R}$ defined inductively by the rule:

$$ \frac{\partial^{r+1} f}{\partial{\hat u}^{r+1}} = \frac{\partial}{\partial{\hat u}}\left(\frac{\partial^{r} f}{\partial{\hat u}^{r}}\right) $$

for $r < n$, whenever these derivatives exist.

### **Schwarz's theorem or Clairaut's theorem on equality of mixed partials**

Let $f:D\subseteq\Bbb R^n\to\Bbb R$ a function such that, $x_0\in D$ and $r>0$ such that ${B_r(x_0) \subseteq D}$

- $\partial_i\partial_jf$ and $\partial_j\partial_if$ are continuous are continuous on ${B_{r}(x_0)}$.

$$ \frac{\partial^2f}{\partial x_i \partial x_j}(x_0) = \frac{\partial^2f}{\partial x_j \partial x_i}(x_0) $$

### Stronger **Schwarz's theorem or Stronger Clairaut's theorem on equality of mixed partials**

Let $f:D\subseteq\Bbb R^n\to\Bbb R$ a function such that:

- $\partial_if, \partial_jf$ and $\partial_j\partial_if$ exists throughout $D$
- $\partial_j\partial_if$ is continuous at $x_0\in D$

Then $\partial_i\partial_jf$ exists at $x_0$ and

$$ \frac{\partial^2f}{\partial x_i \partial x_j}(x_0) = \frac{\partial^2f}{\partial x_j \partial x_i}(x_0) $$

**********Def:********** A function $f:D\subseteq\Bbb R^n\to \Bbb R$ all of whose partial derivatives up to the order $n$ are continuous throughout $D$ is said to be $n$ times _continuously differentiable_ or a $\cal C^n$ _function._

******Th:****** Let $f:D\subseteq\Bbb R^n\to\Bbb R$ a be a $\cal C^n$ function and let ${\hat u} \in \mathbb S^{n-1}$. Then the functions $f, \partial_{{\hat u}}f, \partial^2_{{\hat u}}f, \dots, \partial^{n-1}_{{\hat u}}f$ are differentiable and $\partial^n_{{\hat u}}f$ and for ${1\le r \le n}$,

$$ \begin{align*} \frac{\partial^r f}{\partial {\hat u}^r} &= \left(\frac{\partial }{\partial {\hat u}}\right)^rf \\

&=\sum_{i_1, \dots i_r =1}^n u_{i_1} \cdots u_{i_r}\frac{\partial^r f}{\partial x_{i_r}\cdots \partial x_{i_1}} \end{align*} $$

using the [[Multi-index notation]]:

$$ \frac{\partial^r f}{\partial {\hat u}^r} = \sum_{|\alpha| =r} {r\choose \alpha}{\hat u}^{\alpha} \partial^{\alpha }f $$

**********Def:********** Let $f: D \subseteq \Bbb R^n \to \Bbb R$ be a $\mathcal C ^N$ function and let $x \in D$. We can define $T_N:\Bbb R^n \to \Bbb R$ by:

$$ T_N(h) = \sum_{|\alpha| = 0}^N \frac{h^\alpha}{\alpha!}\partial ^\alpha f(x) $$

$T_N$ is called the $N$-t_h Taylor polynomial of degree $N$ of $f$ at $x_0$._ Similarly the $R_N$ is called the _residue of the_ $N$-t_h Taylor polynomial of degree $N$ of $f$ at $x_0$,_ and it is defined as:

$$ R_N(h)=f(x_0+h) - T_N(h) $$

## Taylor’s Theorem

Let $x_0$ and $x_0+h$ be distinct points in an open set $D$, and $[x_0, x_0+h]\subseteq D$ . Let $\hat u \in \mathbb S^{n-1}$ be unit vector in direction $h$. Consider the function $f:D \subseteq \Bbb R^n \to \Bbb R$ such that, for some $N \in \Bbb N$ the functions

$$ f, \partial_{{\hat u}} f, \cdots \partial_{{\hat u}}^{N-1} f $$

are all differentiable all in $D$.

Then there exists $\theta \in (0,1)$ such that:

$$ f(x_0+h) = \left[\sum_{k = 0}^{N-1} \frac{\|h\|^k}{k!}\frac{\partial^k f}{\partial {\hat u}^k}(x_0)\right] + \frac{\|h\|^N}{N!}\frac{\partial^N f}{\partial {\hat u}^N}(x_0 + \theta h) $$

Additionally we can calculate the

********Th:******** Let $x_0$ and $x_0+h$ be distinct points in an open set $D$, and $[x_0, x_0+h]\subseteq D$. Let ${f:D \subseteq \Bbb R^n \to \Bbb R}$ be, for some $N \in \Bbb N$, $N$ times continuously differentiable. Then there exists a $\theta \in (0,1)$ such that:

$$ f(x_0+h ) = \left[\sum_{|\alpha| = 0}^{N-1} \frac{h^\alpha}{\alpha!} \partial^\alpha f(x_0)\right] +R_{f,N-1}(h) $$

where

$$ R_{f, N-1}(h) = \sum_{|\alpha| =N} \frac{h^\alpha}{\alpha!} \partial^\alpha f({x_0+\theta h)} $$

**********Def:********** Let $g :N\subseteq\Bbb R^n\to \Bbb R$ and $g^*:M\subseteq\Bbb R^n \to\Bbb R$ be two functions, whose open domains contain $\bf 0$. We say that $g$ and $g^*$ ****************_closely approximate each other to the $k$th degree near $\mathbf 0$_ if there is a function $\eta:M\cap N \to \Bbb R$ such that:

$$ g(h) - g^*(h) = \|h\|^k \eta( h) \quad h \in M\cap N $$

and $\lim_{{h\to \mathbf0}}\eta(h) =0$

The above conditions can be written as:

$$ g(\mathbf 0) = g^*(\mathbf 0) \qquad \lim_{{h \to 0}} \frac{|g(h) - g^*(h)|}{\|h\|^k}=0 $$

**************Lemma:************** Let $f, f^*:\Bbb R^n \to\Bbb R$ be two polynomials of degree $k$. If $f^*$ closely approximates $f$ to the $k$th degree, then $f = f^*$.

********Th:******** Let $f:D \subseteq\Bbb R^n\to \Bbb R$ be $n$ times continuously differentiable and let $x \in D$. Then $T_N$, the Taylor polynomial of $N$th degree of $f$ at $x$, is the only $N$th degree polynomial that closely approximates $\delta f_x$ to the $N$th degree near $\mathbf 0$.