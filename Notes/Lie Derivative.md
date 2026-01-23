---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Fields on Smooth Manifolds]], [[Integral Curves, Flows and Flowouts on Smooth Manifolds]], [[Flows and Flowouts on Manifold with Boundary]], [[The Tensor Bundles]], [[Differential Forms on Smooth Manifolds]], [[The Exterior Derivative on Smooth Manifolds]]

**Def:** Suppose $M$ is a smooth manifold, $V$ is a smooth vector field on $M$, and $\theta$ is the flow of $V$. For any a smooth vector field $W$ on $M$, define a rough vector field on $M$, denoted by $\mathcal L_VW$ and called the *Lie derivative of $W$ with respect to $V$,* by $$
\begin{align*}
(\mathcal L_V W)_p &:= \left.\frac{d}{dt}\right\rvert_0 d(\theta_{-t})_{\theta_t(p)}(W_{\theta_t(p)}) \\ &= \lim_{t \to 0}\frac{d(\theta_{-t})_{\theta_t(p)}(W_{\theta_t(p)})- W_p}{t},\end{align*} $$provided the derivatives exists.

If $M$ has a nonempty boundary, this definition of $\mathcal L_VW$ makes sense as $V$ long as $V$ is tangent to $\partial M$ so that its flow exists. 

**Lemma:** Suppose $M$ is a smooth manifold with or without boundary, and $V, W\in {\frak X}(M)$. If $\partial M \neq \varnothing$, assume in addition that $V$ is tangent to $\partial M$. Then $(\mathcal L_VW)_p$ exists for every $p\in M$, and $\mathcal L_VW$ is a smooth vector field.

**Th:** If $M$ is a smooth manifold and $V, W\in {\frak X}(M)$, then $\mathcal L_VW= [V, W]$. 

**Cor:** Suppose $M$ is a smooth manifold with or without boundary, and $V, W, X\in {\frak X}(M)$. 
- $\mathcal L_VW = -\mathcal L_WV$. 
- $\mathcal L_V[W, X] = [\mathcal L_V W, X] + [W, \mathcal L_V X]$ 
- $\mathcal L_{[V, W]} X = \mathcal L_V \mathcal L_W X- \mathcal L_W \mathcal L_V X$. 
- If $g\in \mathcal C^\infty(M)$, then $\mathcal L_V (gW) = (Vg)W + g \mathcal L_V W$. 
- If $F:M \to N$ is a diffeomorphism, then $F_*(\mathcal L_V X) = \mathcal L_{F_*V} F_*X$.

**Prop:** Suppose $M$ is a smooth manifold with or without boundary and $V, W\in {\frak X}(M)$. If $\partial M \neq \varnothing$, assume also that $V$ is tangent to $\partial M$. Let $\theta$ be the flow of $V$. For any $(t_0, p)$ in the domain of $\theta$, $$\left.\frac{d}{dt}\right\rvert_{t_0}d(\theta_{-t})_{\theta_t(p)} (W_{\theta_t(p)}) = d (\theta_{-t_0})_{\theta_{t_0}(p)} \left( (\mathcal L_V W)_{\theta_{t_0}(p)}\right).$$
# Commuting Vector Fields

**Def:** Let $M$ be a smooth manifold and $V, W\in {\frak X}(M)$. We say that *$V$ and $W$ commute* if $VWf = WVf$ for every smooth function $f$, or equivalently if $[V, W] = 0$. If $\theta$ is a smooth flow, a vector field $W$ is said to be *invariant under $\theta$* if $W$ is $\theta_t$-related to itself for each $t$; more precisely, this means that $W|_{M_t}$ is $\theta_t$-related to $W|_{M_{-t}}$ for each $t$, or equivalently that $d(\theta_t)_p(W_p) = W_{\theta_t(p)}$ for all $(t, p)$ in the domain of $\theta$.

**Th:** For smooth vector fields $V$ and $W$ on a smooth manifold $M$, the following are equivalent:
- $V$ and $W$ commute.
- $W$ is invariant under the flow of $V$.
- $V$ is invariant under the flow of $W$.

**Cor:** Every smooth vector field is invariant under its own flow.

**Def:** If $\theta$ and $\psi$ are flows on $M$, we say that *$\theta$ and $\psi$ commute* if the following condition holds for every $p\in M$: whenever $J$ and $K$ are open intervals containing $0$ such that one of the expressions $\theta_t \circ \psi_s (p)$ or $\psi_s \circ \theta_t (p)$ is defined for all $(s, t)\in J \times K$, both are defined and they are equal. For global flows, this is the same as saying that $\theta_t \circ \psi_s = \psi_s \circ \theta_t$ for all $t, s\in \Bbb R$. 

**Th:** Smooth vector fields commute iff their flows commute. 

## Commuting Frames

**Def:** A smooth local frame $(E_i)$ for $M$ is called a *commuting frame* if $[E_i, E_j] = 0$ for all $i$ and $j$. Commuting frames are also called *holonomic frames* by some people. 

The simplest examples of commuting frames are the coordinate frames. Given any smooth chart $(U, (x^i))$ for a smooth manifold $M$, know that the the coordinate frame $\left( \dfrac{\partial}{\partial x^i}\right)$ is a commuting frame. 

**Canonical Form for Commuting Vector Fields:** Let $M$ be a smooth $n$-manifold, and $(V_1,\dots, V_k)$ be a linearly independent $k$-tuple of smooth commuting vector fields on an open subset $W\subseteq M$. For each $p\in W$, there exists a smooth coordinate chart $(U, (s^i))$ centred at $p$ such that $V_i = \dfrac{\partial}{\partial s^i}$ for $i=1,\dots, k$. If $S\subseteq W$ is an embedded codimension-$k$ submanifold and $p$ a point of $S$ such that $T_pS$ is complementary to the span $(V_1|_p,\dots, V_k|_p)$, then the coordinates can also be chosen such that $S \cap U$ is the slice defined by $s^1 = \dots = s^k = 0$. 

The proof of the theorem above suggests a technique for finding explicit coordinates that put a set of commuting vector fields into canonical form, as long as their flows can be found explicitly. Begin with an $(n-k)$-dimensional manifold $S$ whose tangent space at $p$ is complementary to the span $(V_1|_p,\dots, V_k|_p)$. Then we define $\Phi$ by starting at an arbitrary point in $S$ and the following the $k$ flows successively for $k$ arbitrary times. Because the flows commute, it does not matter in which order they are applied. 

## Lie Derivative of Tensor Fields

**Def:** Suppose $M$ is a smooth manifold, $V$ is a smooth vector field on $M$, and $\theta$ is its flow. For any $p\in M$, it is sufficiently close to zero, but $\theta_t$ is a diffeomorphism from a neighbourhood of $p$ to a neighbourhood of $\theta_t(p)$, so that $d(\theta_t)^*_p$ pulls back tensors at $\theta_t(p)$ to ones at $p$.

Given a smooth covariant tensor field $A$ on $M$, we define the *Lie derivative of $A$ with respect to $V$*, denoted by $\mathcal L_VA$, by $$(\mathcal L_VA)_p = \left.\frac{d}{dt}\right\rvert_{t= 0} (\theta^*_t A)_p = \lim_{t\to 0} \frac{d(\theta_t)^*_p (A_{\theta_t(p)})- A_p}t, $$provided the derivative exists.

**Lemma:** Suppose $M$ is a smooth manifold, $V\in {\frak X}(M)$, and $A\in {\cal T}^k T^* M$. If $\partial M \neq \varnothing$, assume also that $V$ is tangent to $\partial M$. Then the Lie derivative of $A$ with respect to $V$ exists for every $p\in M$ and defines $\mathcal L_V A$ as a smooth tensor field on $M$. 

**Prop:**  Let $M$ be a smooth manifold with or without boundary and let $V\in {\frak X}(M)$. If $\partial M \neq \varnothing$, assume also that $V$ is tangent to $\partial M$. Suppose $f$ is a smooth real-valued function (regarded as a $0$-tensor field), and $A, B$ are smooth covariant tensor fields on $M$.
- $\mathcal L_V f = Vf$.
- $\mathcal L_V(fA) = (\mathcal L_V f)A + f(\mathcal L_V A)$.
- $\mathcal L_V(A\otimes B) = (\mathcal L_VA) \otimes B + A\otimes (\mathcal L_VB)$.
- If $X_1,\dots, X_k$ are smooth vector fields and $A$ is a smooth $k$-tensor field,  $$\mathcal L_V(A(X_1,\dots, X_k)) =  (\mathcal L_V A) (X_1,\dots, X_k) + \sum_{i = 1}^k A(X_1,\dots, \mathcal L_VX_i, \dots, X_k).$$

**Cor:** If $V$ is a smooth vector field and $A$ is a smooth covariant $k$-tensor field, then for any smooth vector field $X_1,\dots, X_k$,  $$(\mathcal L_VA)(X_1,\dots, X_k) =  V (A(X_1,\dots, X_k)) - \sum_{i = 1}^k A(X_1,\dots, [V, X_i], \dots, X_k). $$ **Cor:** If $f\in \mathcal C^\infty(M)$, then $\mathcal L_V (df) = d (\mathcal L_V f)$. 

**Def:** If $A$ is a smooth tensor field on $M$ and $\theta$ is a flow on $M$, we say that *$A$ is invariant under $\theta$* if for each $t$, the map $\theta_t$ pulls $A$ back to itself whenever it is defined, more precisely, this means  $$d(\theta_t)^*_p (A_{\theta_t(p)}) = A_p $$for all $(t, p)$ in the domain of $\theta$. If $\theta$ is a global flow, this is equivalent to $\theta_t^* A = A$ for all $t\in\Bbb R$.

**Prop:** Suppose $M$ is a smooth manifold with or without boundary and $V\in {\frak X}(M)$. If $\partial M \neq \varnothing$, assume in addition that $V$ is tangent to $\partial M$. Let $\theta$ be the flow of $V$. For any smooth covariant tensor field $A$ and $t_0, p)$ in the domain of $\theta$,  $$\left. \frac{d}{dt}\right\rvert_{t =t_0}(\theta_t^* A)_p = (\theta_{t_0} (\mathcal L_VA))_p.$$
**Th:** Let $M$ be a smooth manifold and let $V\in {\frak X}(M)$. If $\partial M \neq \varnothing$, assume in addition that $V$ is tangent to $\partial M$. A smooth covariant tensor field $A$ is invariant under the flow of $V$ iff $\mathcal L_V A = 0$. 

**Prop:** Let $M$ is a smooth manifold with or without boundary, $A$ is a smooth covariant tensor field on $M$, and $V, W\in {\frak X}(M)$. If $\partial M \neq \varnothing$, assume in addition that $V$ and $W$ are tangent to $\partial M$.  Then $$\mathcal L_V\mathcal L_W A - \mathcal L_W \mathcal L_V A = \mathcal L_{[V, W]} A.$$
**Prop:** Let $M$ be a smooth manifold and $V\in {\frak X}(M)$. Then the Lie derivative operator on covariant tensor fields, $\mathcal L_V: \mathcal T^k(M)\to \mathcal T^k(M)$ for $k\ge 0$, are uniquely determined by the following properties:
- $\mathcal L_V$ is linear over $\Bbb R$.
- $\mathcal L_V f = Vf$ for $f\in \mathcal T^0(M) = \mathcal C^\infty(M)$.
- $\mathcal L_V(A \otimes B) = (\mathcal L_V A) \otimes B + A \otimes (\mathcal L_V B)$ for $A\in \mathcal T^k(M), B\in \mathcal T^l(M)$.
- $\mathcal L_V(\omega(X)) = (\mathcal L_V \omega)(X) + \omega([V, X])$ for $\omega \in \mathcal T^1(M), X\in {\frak X}(M)$.

We can extend the definition of the Lie derivative to manifolds with boundary, where the flow of $V$ might not be defined.

We can extend the Lie derivative to also mixed tensors, but we must be a little careful. Let $M$ be a smooth manifold with or without boundary, and $V\in {\frak X}(M)$. If $\partial M \neq \varnothing$ assume that $V$ is tangent to $\partial M$. Let $\theta$ be the flow of $V$. For any tensor field $A\in \Gamma(T^{(k, l) }TM)$ we can define its *Lie derivative* as $$(\mathcal L_V A)_p := \left.\frac{d}{dt}\right\rvert_{t = 0} ((\theta_t)^* A)_p·$$
## Differential Forms

**Prop:** Suppose $M$ is a smooth manifold, $V\in {\frak X}(M)$, and $\omega, \eta\in \Omega^*(M)$. Then $$\mathcal L_V(\omega\wedge \eta) = (\mathcal L_V \omega) \wedge \eta + \omega\wedge (\mathcal L_V \eta). $$
**Cartan's Magic Formula:** On a smooth manifold, for any vector field $V$ and any smooth differential form $\omega$,  $$\mathcal L_V \omega = V \;\lrcorner\; (d\omega) + d(V\; \lrcorner\; \omega). $$**The Lie Derivative Commutes with $d$:** If $V$ is a smooth vector field and $\omega$ is a differential form, then $$\mathcal L_V(d\omega) = d(\mathcal L_V\omega) = d(V \; \lrcorner \; d\omega). $$