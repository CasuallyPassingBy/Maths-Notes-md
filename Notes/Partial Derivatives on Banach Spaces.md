---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Differentiablity of Real valued functions of Rn]], [[Differentiability of Vector valued functions of Rn]], [[Fréchet-Derivative]], [[Mean Value Theorem for Fréchet Derivatives]]

Let $V_1, \dots, V_n, W$ Banach spaces. The Cartesian product $V =V_1 \times \dots \times V_n$ with the norm: $$ \|(v_1, \dots, v_n) \|_{V} := \max_{j =1, \dots, n}\|v_j\|_{V_j}$$is a Banach space. The inclusion of the $j$th factor $$\iota_j:V_j \to V \qquad \iota_j(v) := (0, \dots, 0, v, 0, \dots, 0)$$
is a linear function and a isometry. If $\Omega$ is an open $V$, and $u \in \Omega$, then $$ \Omega_{j, u} := \{v \in V_j \mid u + \iota_j v \in \Omega\}$$is open in $V_j$ and contains a $0$.

For the rest of the note $\Omega$ is open in $V$. 

**Def:** A function $\varphi: \Omega\to W$ is *partially differentiable with respect to the* $j$*th variable at the point $u$ of* $\Omega$ if the function: $$\varphi_{j, u}:\Omega_{j, u}\to W \qquad \varphi_{j, u}(v) := \varphi(u + \iota_j v) $$is differentiable at $0$. The *partial derivative of $\varphi$ with respect to the $j$th variable on* $u$ is defined as $$\partial_j\varphi(u) := \varphi_{j, u}' (0) \in \mathcal B(V_j, W)$$The function $\varphi$ is *partially differentiable with respect to the $j$th variable in* $\Omega$ if it is on every point $u \in \Omega$, and *the partial derivative of $\varphi$ respect to the $j$th variable* on $\Omega$ is the function $$\partial_j\varphi:\Omega\to \mathcal B(V_j, W) \qquad u \mapsto \partial_j\varphi(u)$$
If $\varphi:\Omega \to W$ is differentiable on $u$ then, by the chain rule, $\varphi$ is partially differentiable with respect to the $j$th variable on $u$ and $$\partial_j \varphi(u) = \varphi'(u) \circ \iota_j \qquad j \in \{1, \dots, n\}$$Meaning that $\partial_j\varphi(u)$ is a restriction of $\varphi$ to the factor $V_j$. We can see that $v = \sum_{j = 1}^n \iota_j v_j$ if $v = (v_1, \dots, v_n)$. In consequence $$\varphi'(u)v = \sum_{j = 1}^n \partial_j\varphi(u)v_j $$
**Th:** A function $\varphi:\Omega \to W$ is of class $\mathcal C^1$ on $\Omega$ iff $\varphi$ is partially differentiable with respect to the $j$th variable on $\Omega$ and $$\partial_j\varphi:\Omega\to \mathcal B(V_j, W) $$is continuous on $\Omega$ for each $j \in \{1, \dots, n\}$. 