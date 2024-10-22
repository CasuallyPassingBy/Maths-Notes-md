---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Complete Metric Spaces]], [[Bounded Linear Operators]], [[Differentiability of Vector valued functions of Rn]], [[Bounded Linear Operators]], [[Limits in Metric Spaces]], [[Differentiabilty of vector valued functions of R]]

Let $V$ and $W$ be a Banach space and $\Omega$ be an open subset of $V$, with this we can define the derivative:

Let $\varphi: \Omega \to  W$ is Fréchet-differentiable at the point $u_0 \in \Omega$ if there's $T \in {\cal B}(V, W)$ such that
$$
\lim_{v \to 0}\frac{\|\varphi(u_0+v)-(\varphi(u_0)+Tv)\|_W}{\|v\|_V} = 0
$$
$T$ is called the Fréchet-derivative of $\varphi$ at $u_0$ and is denoted as
$$
	\varphi'(u_0) \quad \text{ or } \quad D\varphi(u_0) 
$$
This is completely analogous to what happens with derivatives of functions from $\Bbb R^n$ to $\Bbb R^m$

I wanna emphasis, that $\varphi'(u_0) : V \to W$, and it is a bounded linear operator. 

We can rephrase the limit condition of the derivative as, for any $\varepsilon>0$, there's a $\delta>0$ such that for any $v \in V$, that $\|v\|_V< \delta$, then
$$
u_0 +v  \in \Omega \quad \text{ and } \quad \|\varphi(u_0+v) -(\varphi(u_0)+\varphi'(u_0)v)\|_W < \varepsilon \|v\|_V
$$
If $\varphi$ is Fréchet-differentiable at $u_0$, then the function $T \in {\cal B}(V, W)$ that satisfies the derivative equation is unique. 

Also we have the special case that if $T \in {\cal B}(V, W)$, then $T$ is differentiable on $V$, and $T'(u)=T$, for all $u \in V$.

$\varphi: \Omega \to W$ is *Fréchet-differentiable on $\Omega$* if it is at every point $u \in \Omega$. The function
$$
\varphi':\Omega\to {\cal B}(V, W),  \quad u\mapsto \varphi'(u)
$$
it is called the *Fréchet-derivative of $\varphi$*. We will denote it as
$$
D\varphi: \Omega \to {\cal B}(V, W)
$$
If $\varphi$ is differentiable at $u_0$, then $\varphi$ is continuous on $u_0$

Let $\varphi, \psi:\Omega \to W$ are Fréchet-differentiable on $u_0$, and $\lambda, \mu \in \Bbb R$, then $\lambda \varphi,+  \mu \psi$ is differentiable at $u_0$ and
$$
(\lambda \varphi+\mu \psi)' = \lambda \varphi'+\mu \psi'
$$
Let $\Omega \subseteq V$, $\tilde \Omega \subseteq W$ be open subsets. If $\varphi:V \to W$ is differentiable at $u_0$, $\varphi(v) \in\tilde  \Omega$ for all $v \in \Omega$ and $\psi: \tilde\Omega \to Z$ is differentiable at $v_0 := \varphi(u_0)$, then $\psi \circ \varphi: \Omega \to Z$  is differentiable at $u_0$ and
$$
(\psi \circ \varphi)'(u_0) = \psi'(\varphi(u_0))\circ \varphi'(u_0) = \psi'(v_0)\circ \varphi'(u_0)
$$

A function $\varphi:\Omega \to W$ is of class $\mathcal C^1$, or continuously differentiable, on $\Omega$, if it is Fréchet-differentiable on $\Omega$, and its derivative
$$
\varphi':\Omega \to {\cal B}(V, W)
$$
is continuous.