---
tags:
  - Analysis
  - LinearAlgebra
---
Subjects: [[Metric and Normed Spaces]], [[Linear Algebra]]
Links: [[Bounded Linear Operators]], [[Complete Metric Spaces]], [[Isomorphism of Vector Spaces]]

**Def:** A linear bijective function $T:V \to W$ between two Banach spaces $V$ and $W$, that additionally is a homeomorphism is called a *Banach isomorphism*. 

Let us consider the set of all Banach isomorphisms between $V$ and $W$, and we will denote it as $$\mathcal H(V,W) := \{T \in \mathcal B(V, W) \mid T \text{ is  Banach isomorphism}\}$$
An element of $\mathcal H(V, W)$ is a function $T: V\to W$ linear, continuous, bijective and with linear and continuous inverse. In the case where $$\mathcal H(V) := \mathcal H(V, V)$$ If $T \in \mathcal H(V)$ we denote $$T^0:= I, \qquad T^k := T^{k-1}\circ T \quad \forall k \in \Bbb N^+$$
Where $I = \text{id}_Y$. 

**Lemma:** Let $S \in \mathcal B(V)$ and $\|S\|_{\mathcal B(V)} <1$, then $I - S \in \mathcal H(V)$, $$
\begin{align*}(I-S)^{-1} &= \sum_{k = 0}^\infty S^k \\
 \|(I-S)^{-1}\|_{\mathcal B(V)} &\le \frac{1}{1-\|S\|_{\mathcal B(V)}}
 \end{align*}$$and $$\lim_{S\to 0}\frac{\|(I-S)^{-1}-I-S\|_{\mathcal B(V)}}{\|S\|_{\mathcal B(V)}} = 0$$
 **Prop:** 
 - $\mathcal H(V)$ is an open subset of $\mathcal B(V, W)$
 - The function $$\Phi:\mathcal H(V, W) \to \mathcal B(V, W), \qquad \Phi(T) := T^{-1}$$is differentiable and its derivative at $T_0$ is $$\Phi(T_0)T  =-T_0^{-1} TT_0^{-1}$$
 **Prop:** We have that $\mathcal H(\Bbb R^n, \Bbb R^m)$ is empty when $n \ne m$, and it is the set of all matrix that have determinant nonzero when $n = m$

A way to prove that $\mathcal H(\Bbb R^n, \Bbb R^n)$ is open is by checking that the determinant $\det:\mathcal M_n(\Bbb R) \to \Bbb R$ is continous

