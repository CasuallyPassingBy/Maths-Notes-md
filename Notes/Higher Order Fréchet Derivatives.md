---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Higher Order Derivatives and Taylor's Theorem for Real valued functions of Rn]], [[Fréchet-Derivative]], [[Bounded Multilinear Transformations]], [[Partial Derivatives]], [[Multi-index notation]]

Let $V$ and $W$ be Banach Spaces and $\Omega$ be an open set of $V$. If $\varphi:\Omega\to W$ is differentiable, and its derivative takes values in the space $\mathcal B(V, W)$. The natural question is if $\varphi':\Omega\to \mathcal B(V, W)$ is differentiable on $\Omega$. If it is, we say that $\varphi$ is twice differentiable on $\Omega$. The derivative of $\varphi'$ is called the second derivative of $\varphi$, and is denoted as $$D^2 \varphi:\Omega \to \mathcal B(V, \mathcal B(V, W))$$or simply $\varphi''$. 

**Def**: Let $k\in \Bbb N$, and $k\ge 2$. A function $\varphi:\Omega\to W$ is a $k$-*times differentiable on* $\Omega$ if $\varphi$ is $(k-1)$-times differentiable on $\Omega$ and its derivative of order $k-1$ is differentiable on $\Omega$. The derivative $D^{k-1}\varphi:\Omega \to \mathcal B_{k-1}(V, W)$ is called the *derivative of order* $k$ *of* $\varphi$ and it is denoted as $$D^k \varphi: \Omega \to \mathcal B_k(V, W)$$
If $D^k\varphi$ is continuous on $\Omega$ we say that $\varphi$ *is of class* $\mathcal C^k$ *in* $\Omega$. 
If $\mathcal D^i \varphi$ admits a continuous extension to the closure $\overline \Omega$ for each $i\in \{0, \dots, n\}$, where $D^0 \varphi := \varphi$, we sya that $\varphi$ is *of class $\mathcal C^k$ on* $\overline \Omega$. 
Finally, if $\varphi$ is of class $\mathcal C^k$ on $\Omega$ (respectively on $\overline \Omega$) for all $k\in \Bbb N$, we say that $\varphi$ *is of class $\mathcal C^\infty$ on* $\Omega$ (respectively on $\overline \Omega$)

**Prop:** if $\varphi:\Omega \to W$ is $k$ times differentiable on $\Omega$, por each $u \in \Omega$, the $k$th derivative of $\varphi$ on $u$ is a symmetric $k$-linear map. 

**Def:** If $V$ and $W$ are Banach spaces, $\Omega$ is an open subset of $V$ and $k \in \Bbb N \cup \{\infty\}$ we define $$\begin{align*} 
\mathcal C^k (\Omega, W) &:= \{ \varphi: \Omega \to W \mid \varphi \text{ is of class }\mathcal C^k \text{ on }\Omega \} \\
\mathcal C^k (\overline \Omega, W) &:= \{ \varphi: \Omega \to W \mid \varphi \text{ is of class }\mathcal C^k \text{ on }\overline \Omega \} 
\end{align*} $$
If $W = \Bbb R$, we simply write $$\begin{align*}
\mathcal C^k (\Omega) &:= \mathcal C^k(\Omega, \Bbb R) \\
\mathcal C^k (\overline \Omega) &:= \mathcal C^k(\overline \Omega, \Bbb R)
\end{align*}$$
# Higher Order Partial Derivatives

**Def:** Let $V_1, \dots, V_n, W$ be Banach spaces, $\Omega$ an open subset of $V:= V_1 \times \dots \times V_n$ and $\varphi: \Omega \to W$.

The partial derivative of order $2$, are $$\partial_j\partial _i \varphi(u):= \partial _j(\partial_i \varphi(u)) \in \mathcal B(V_j, \mathcal B (V_i, W))\cong \mathcal B(V_j, V_i, ;W)$$
 Let $V_1, \dots, V_n, W$ be Banach spaces, $\Omega$ an open subset of $V:= V_1 \times \dots \times V_n$ and $\varphi: \Omega \to W$. If $\varphi$ of class $\mathcal C²$, then for any $u \in \Omega$, $i,j\in \{1, \dots, n\}$ the partial derivatives of order $2$ exists and are continuous, and satisfy that $$D^2\varphi(u)(v, w) = \sum_{i, j = 1}^n \partial _j\partial _i \varphi(u) (v_j, w_i)$$
for any $v=(v_1, \dots, v_n), w = (w_1, \dots, w_n) \in V$

**Th:** If $\varphi\in \mathcal C^2(V, W)$, then $\partial_j\partial_i \varphi(u) = \partial_i\partial_j\varphi(u)$ for any $u \in \Omega$, $i,j \in \{i, \dots n\}$. 

**Th:** $\varphi: \Omega \to W$ is of class $\mathcal C^2$ iff the partial derivative of order $2$, $\partial_j\partial_i\varphi:\Omega \to \mathcal B(V_j, V_i;W)$ exist and is continuous for any $i, j  \in \{1, \dots, n\}$ 
With this we can generalize to higher order parial derivatives.

We define the $k$ order partial derivative as:
$$ \partial_{i_k}\partial_{i_{k-1}}\cdots \partial_{i_1} \varphi (u) = \partial_{i_k}(\partial_{i_{k-1}}\cdots \partial_{i_i}\varphi(u)) \in \mathcal B(V_{i_k}, \dots, V_{i_1}; W)$$

If $\varphi \in \mathcal C ^k(\Omega, W)$, the all the $k$ order partial derivatives exists and are continuous, and satisfy that $$D^k \varphi(u) (v_1, \dots, v_k) = \sum_{i_1, \dots i_k = 1}^n \partial_{i_1}\partial_{i_{2}}\cdots \partial_{i_k} \varphi (u) (v_{1, i_1}, \dots, v_{k, i_k})$$
for any $v_i = (v_{i, 1}, \dots, v_{i, n}) \in V$ for $i \in \{1, \dots, k\}$ 

**Th:** If $\varphi \in \mathcal C^k (\Omega, W)$, then as long as the partial derivatives of order $k$ have the same indeces where we derived with repetition, then the partial derivatives will be equal.

From this theorem, if we have $\varphi \in \mathcal C^k(\Omega, W)$ then we can implement a simpler notation, let $\alpha = (\alpha_1, \dots, \alpha_n)$ be a multi-index, with $|\alpha| = k$, then we can arrange any partial derivative of order $k$ into the partials with respect to the first coordinate, and so on.  So we can use the notation $$\partial^\alpha \varphi$$
to represent that there's $\alpha_i$ partial derivatives with respect to $V_i$, for $i \in \{1, \dots, n\}$.  We can use this result to clean up the notation, let $\alpha$, and $\beta$ be multi-indeces with $|\alpha| + |\beta| = k$, then $$\partial ^\alpha \partial ^\beta \varphi(u) = \partial^\beta \partial ^\alpha \varphi(u)$$
**Th:** A function $\varphi:\Omega \to W$ is class $\mathcal C^k$ iff the partial derivatives of order $k$, $\partial^\alpha \varphi$ exist and are continuous for any multi-index $\alpha$ with $|\alpha| = k$.  
# Taylor's Theorem

If $V$ is a Banach space, and $\Omega$ is an open subset of $V$, $u_0 \in \Omega$ and $v \in V$ satisfy such that $u_0 + tv \in \Omega$ for each $t \in  [0, 1]$ and $\varphi \in \mathcal C^{k+1}(\Omega)$, then there's $\theta \in (0, 1)$ such that $$\varphi(u_0 + v) = \varphi(u_0) + D\varphi(u_0)v + \frac{1}{2!} D²\varphi(u_0) (v, v) +\dots + \frac{1}{k!} D^k\varphi(u_0)(v, \dots, v)+\frac{1}{(k+1)!}D^{k+1}\varphi(u_0 + \theta v) (v, \dots, v)$$
or
$$\varphi(u_0+v) = \sum_{j = 0}^k \frac{1}{j!}D^j \varphi(u_0)(v, \dots, v) + \frac{1}{(k+1)!}D^{k+1}\varphi(u_0 + \theta v)(v, \dots, v)$$

**Taylor's Formula**
if $V$ is a Banach space, $\Omega$ is an open subset of $V$, $u_0\in \Omega$, and $\varphi \in \mathcal C^k(\Omega)$ then the function $$r_k(v) = \varphi(u_0+v) -\varphi(u_0) - D\varphi(u_0)v - \frac{1}{2!} D²\varphi(u_0) (v, v) -\dots - \frac{1}{k!} D^k\varphi(u_0)(v, \dots, v)$$
defined in the neighbourhood of $0$ on $V$, satisfies $$\lim_{v \to 0}\frac{r_k(v)}{\|v\|^k} = 0$$
The function $$P_k (v) :=  \sum_{j = 0}^k \frac{1}{j!}D^j \varphi(u_0)(v, \dots, v)$$is called the *Taylor expansion of degree* $k$ *of $\varphi$ around* $u_0$
