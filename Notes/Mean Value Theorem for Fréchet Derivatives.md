---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Fréchet-Derivative]], [[Differentiabilty of vector valued functions of R]], [[Mean Value Theorem in R]], [[Rectifiable Curves]]

A linear function $T:\Bbb R \to V$ is totally determined with its value at $1$, since $T(t) = tT(1)$, for $t\in \Bbb R$.

From this we get that the function $\iota: {\cal B}(\Bbb R, V) \to V$, with $\iota(T) := T(1)$. This is a vector isomorphism, and additionally it is an isometry since 
$$
\|T\|_{{\cal B}(V, W)} = \sup_{v \in S_{\Bbb R}} \|T(v)\|_V = \|T(1)\|_V
$$
Then we can identify that ${\cal B}(\Bbb R, V)$ with $V$. 

If $\sigma:(a, b) \to V$ is Fréchet-differentiable at the point $t_0 \in (a,b)$, then we can identify the derivative $\sigma'(t_0) \in {\cal B}(\Bbb R, V)$, with its value at $1$, and then for simplicity we can write $\sigma'(t_0)$ to refers to $\sigma'(t_0)(1)$. Then we see that $\sigma'(t_0)\in V$, and 
$$
\sigma'(t_0) = \lim_{t \to 0}\frac{\sigma(t+t_0)-\sigma(t_0)}{t} \in V
$$
Which actually tells with the connection to the derivatives of functions from $\Bbb R$ to $\Bbb R^n$, and why it behaves like that. This we can actually interpret as a velocity at $t_0$ of $\sigma$.

Similarly we can look at the chain rule:
Let $\sigma:(a,b) \to \Omega \subseteq V$ is differentiable at $t_0\in (a,b)$ and $\varphi:\Omega \to W$ is differentiable at $u_0 := \sigma(t_0)$, then we get
$$
(\varphi\circ \sigma)'(t_0) = \varphi'(u_0) (\sigma'(t_0)) 
$$

The thing with the with the mean value in $\Bbb R$ is that given $f:[a,b]\to \Bbb R$ continuous and differentiable on $(a,b)$, then $f(a)-f(b) = (b-a)f'(c)$ for some $c\in(a,b)$. The issue here is that we don't know which $c$, so the most important is to have a bound for $|f'(c)|$, so we are going to do that in general:
##### Mean value theorem
Let $\sigma: [a,b]\to V$ is a continuous function. If $\sigma$ is differentiable for every $t\in(a,b)$, and there's $M>0$, such that
$$
\|\sigma'(t)\|\le M \qquad \forall t\in (a,b)
$$
Then 
$$
\|\sigma(b) -\sigma(a)\| \le M(b-a)
$$
We get the corollaries:

Let $\Omega$ be an open subset of $V$, $\varphi:\Omega \to W$ is of class $\cal C^1$ on $\Omega$, and $u_0, u_1 \in \Omega$ such that $u_t = (1-t)u_0 + tu_1 \in \Omega$ for all $t \in [0,1]$, meaning $[u_0, u_1]\subseteq \Omega$, then
$$
\sup_{t\in[0,1]} \|\varphi'(u_t)\|_{{\cal B}(V,W)} = \sup_{u \in[u_0, u_1]} \|\varphi'(u)\|_{{\cal B}(V, W)} <\infty
$$
and
$$
\|\varphi(u_1) - \varphi(u_0)\|_W \le \left(\sup_{u \in [u_0, u_1]}\|\varphi'(u)\|_{{\cal B}(V, W)}\right) \|u_1-u_0\|
$$
Let $\Omega$ be an open subset of $V$, $\varphi:\Omega \to W$ is of class $\cal C^1$ on $\Omega$, and $u_0, u_1 \in \Omega$ such that $u_t = (1-t)u_0 + tu_1 \in \Omega$ for all $t \in [0,1]$, meaning $[u_0, u_1]\subseteq \Omega$, for all $u \in \Omega$, then
$$
\sup_{t\in[0,1]}\|\varphi'(u_t)-\varphi'(u)\|_{{\cal B}(V, W)} <\infty
$$
 and it satisfies
$$
 \|\varphi(u_1)-\varphi(u_0)-\varphi'(u)(u_1-u_0)\|\le \left(\sup_{t\in [0,1]}\|\varphi'(u_t)-\varphi'(u)\|\right)\|u_1-u_0\|
 $$

Let $\Omega$ be an open and connected set of a Banach space $V$, $\varphi:\Omega \to V$ is differentiable on $\Omega$, and $\varphi'(u) = 0$ for all $u\in \Omega$, the $\varphi$ is constant in $\Omega$. 