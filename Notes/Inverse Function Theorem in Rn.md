---
tags:
  - VectorAnalysis
---

Subjects: [[Vector Analysis]]  
Links: [[Differentiablity of Real valued functions of Rn]], [[Norm of Linear Operators for finite dimensions]], [[Space of Linear Transformations]], [[The Rank of a Matrix and Matrix Inverses]]

# Injective functions and their Inverses

**Th:** Let $D$ be an open interval of $\Bbb R$ and consider a continuous function $f:D\subseteq\Bbb R\to\Bbb R$. The following are equivalent:

- $f$ is injective
- $f(N)$ is an open interval whenever $N$ is an open interval in $D$
- $f$ is strictly monotonic

********Def:******** The function $f:D\subseteq\Bbb R^n\to \Bbb R^m$ is said to be locally injective at $x\in D$ if there is an open set $N$ in $\Bbb R^m$ with $x\in N\subseteq D$ such that $f$ is injective on $N$. We also under these circumstances that $f$ is _**locally invertible**_ at $\mathbf p$ and, where there is no possible ambiguity, denote the local inverse $f^{-1}:f[N] \to D$.

********Th:******** A differentiable function $f:D\subseteq \Bbb R\to\Bbb R$ is not locally injective at any point where it has a local extremum

# Inverse Function Theorem
- *********Lemma 1:*********
    **************Lemma:************** Let $f:D\subseteq\Bbb R^n\to \Bbb R^m$ be differentiable on $D$; $f$ is continuously differentiable at $x_0 \in D$ iff for any $\varepsilon > 0$, there’s a $\delta >0$ such that for any $\mathbf x \in D$ if $\|{x -x}_0 \| <\delta$, then $\|df_{x} - df_{x_0}\|_{\mathcal L(n,m)} < \varepsilon$.
    
    **********Cor:********** Let $f:D\subseteq\Bbb R^n\to\Bbb R^m$ be a $\cal C^1$ function on $D$ iff $df : D \subseteq \Bbb R^n \to \mathcal L(n,m)$ is continuous on $D$ with respect to$\|\cdot\|_{\mathcal L(n,m)}$ norm.
    
    **************Lemma:************** Let $f:D\subseteq\Bbb R^n\to\Bbb R^m$ be a $\cal C^1$ function and let $x\in D$. Then for all $\varepsilon >0$ there exists a $\delta>0$ such that for all $y\in B_\delta(x) \subseteq D$
    - $\|df_y(h)-df_x(h)\| \le \varepsilon \| h\|$
    - $\|f(y)- f(z) - df_x(y-z)\| \le \varepsilon\|y-z\|$ , for all $y,z \in B_\delta(x)$

*********Prop:********* Let $f:D\subseteq\Bbb R^n\to\Bbb R^m$ be a $\cal C^1$ function on $D$, then for any compact set $K \subseteq D$, then exists $x_0 \in K$, such that for any $x \in K$

$$ \|df_{x}\|_{\mathcal L(n,m)} \le \|df_{x_0}\|_{\mathcal L(n,m)} $$

- ********Lemma 2:********
    **************Lemma:************** Let $f:D\subseteq\Bbb R^n\to\Bbb R^m$ be a differential on $D$ and continuously differentiable at $x_0 \in D$, such that $df_{x_0}:\Bbb R^n\to \Bbb R^n$ is invertible, then exists $\delta >0$ and $M >0$ such that for all $x \in D$ if $x \in B_\delta(x_0)$, then
    $$ M\|y\| \le \|df_{x}(y) \| \qquad \text{for all $y \in \Bbb R^n$} $$
    **************Cor:************** Let $f:D\subseteq\Bbb R^n\to\Bbb R^m$ be a differential on $D$ and continuously differentiable at $x_0 \in D$, such that $df_{x_0}:\Bbb R^n\to \Bbb R^n$ is invertible, then exists $\delta >0$ and $M >0$ such that for all ${x \in D}$ if $x \in B_\delta(x_0)$, $df_{x}$ is invertible
    
    ********Th:******** Let $f:D\subseteq\Bbb R^n\to \Bbb R^n$ be a $\cal C^1$ function on an open set $D$ in $\Bbb R^n$ and let $x_0\in D$ such that $\det J_f(x_0)\ne 0$ . Then there is $\delta >0$ where $B_\delta(x_0) \subseteq D$ such that
    - $\det J_f(y) \ne 0$ for all $y \in B_\delta(x_0)$
    - $f:B_\delta(x_0) \to \Bbb R^n$ is injective

**************Lemma 3:************** Let $f:D\subseteq\Bbb R^n\to\Bbb R^m$ be a $\cal C^1$ function and let $\mathbf p \in D$. If $df_{\mathbf p}$ is invertible then there’s a $\delta>0$ and $m>0$ such that $B_\delta(\mathbf p)\subseteq D$ and
$$ \|f(y) -f(x) \|\ge m\|{y-x}\|\qquad \text{for all } {x, y} \in B_\delta(x_0) $$

## Inverse Function Theorem
Let $f:D\subseteq\Bbb R^n\to\Bbb R^n$ be of class $\cal C^1$ on an open set $D$ in $\Bbb R^n$ and let ${\det J_f(x_0) \ne 0}$ at a point $x_0\in D$. Then

- There exists an open set $U$ in $\Bbb R^n$ containing $x_0$ and an open set $V$ in $\Bbb R^n$ containing $f(x_0)$ such that $U \subseteq D$, $f(U) = V$ and $f$ is injective on $U$
    
- The function $f^{-1}:V\subseteq\Bbb R^n\to \Bbb R^n$ locally inverse to $f$ on $U$ of class $\cal C^1$, with derivative such that if $y = f(x) \in V$:
    
    $$ df^{-1}_{y} = df^{-1}_{f(x)} = (df_x)^{-1} $$
    
    and
    
    $$ J_g(y ) =J_g(f(x))= (J_f(x))^{-1} $$
    
    If $f$ is $\mathcal C^k, k\ge 1$ then so is $f^{-1}$ is unique.
    

## Straightening-Out Theorem
Let $f:D\subseteq \Bbb R^n\to \Bbb R$, be a class $\cal C^k$ function with $k \ge 1$, and $D$ open in $\Bbb R^n$. Let $x_0 \in D$ suppose $f(x_0) =0$ and $\nabla f(x_0)\ne \mathbf 0$. Then there is an open set $U$, and open set $V$ containing $x_0$, and a function $h: V\to U$ of class $\cal C^k$ with inverse $h^{-1}:U\to V$ of class $\cal C^k$ such that

$$ (f\circ h)(x_1, \dots, x_n) = x_n $$

### Straightening-Out Theorem V.2.
Let $f:D\subseteq \Bbb R^n\to \Bbb R^m$ with $m\le n$, be a class $\cal C^k$ function with $k \ge 1$, and $D$ open in $\Bbb R^n$. Let $x_0 \in D$ suppose $f(x_0) =\mathbf 0$ and $\dim(\operatorname{Im}(df_{x_0})) = m$. Then there is an open set $U$, and open set $V$ containing $\mathbf x_0$, and a function $h: V\to U$ of class $\cal C^k$ with inverse $h^{-1}:U\to V$ of class $\cal C^k$ such that

$$ (f\circ h)(x_1, \dots, x_n) = (x_{n-m+1}, \dots, x_n) $$

### Straightening-Out Theorem V.3.

Let $f:D\subseteq \Bbb R^n\to \Bbb R^m$ with $m\ge n$, be a class $\cal C^k$ function with $k \ge 1$, and $D$ open in $\Bbb R^n$. Let $x_0 \in D$ suppose and $\dim(\operatorname{Im}(df_{x_0})) = n$. Then there is an open set $U$ in $\Bbb R^m$ containing $f(x_0)$, and open set $V$ in $\Bbb R^m$, and a function $g: U\to V$ of class $\cal C^k$ with inverse $g^{-1}:V\to U$ of class $\cal C^k$ such that

$$ (g\circ f)(x_1, \dots, x_n) = (x_{1}, \dots, x_n, 0,\dots, 0) $$

for all $x \in D$.

## Eliminating Dependencies Theorem

Let $D\subseteq\Bbb R^n$ be open, $f:D\to \Bbb R^N$ be a $\cal C^k$ function where $\dim(\operatorname{Im}df_x) =m$ for all $x$ in an open neighborhood of $x_0\in A$. Then there is are open sets $U, V\subseteq\Bbb R^n$ such that $x_0 \in V$ and a function $h: U\to V$ of class $\cal C^k$ with inverse $h:V\to U$ of class $\cal C^k$such that $f\circ h$ only depends on $x_1,\dots, x_m$. This is that $(f\circ h) (x_1, \dots, x_n) = \tilde f(x_1, \dots, x_m)$ for some $\cal C^k$ function

**Cor:** Let $D\subseteq\Bbb R^n$ be open, $f:D\to \Bbb R^N$ be a $\cal C^k$ function where $\dim(\operatorname{Im}df_x) =m$ for all $\mathbf x$ in an open neighborhood of $\mathbf x_0\in A$. Then there are open sets $U_1, U_2 \in \Bbb R^n$ with $x_0 \in U_2$ and $V_1 , V_2 \subseteq\Bbb R^N$ with $f(x_0) \in V_1$, and functions $h:U_1 \to U_2$ and $g: V_1\to V_2$ of class $\cal C^k$ with inverses of class $\cal C^k$ such that

$$ (g\circ f\circ h)(x_1, \dots, x_n) = (x_1,\dots, x_m, 0,\dots, 0) $$