---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Fields on Smooth Manifolds]], [[Integral Curves, Flows and Flowouts on Smooth Manifolds]], [[Flows and Flowouts on Manifold with Boundary]]

**Def:** Suppose $M$ is a smooth manifold, $V$ is a smooth vector field on $M$, and $\theta$ is the flow of $V$. For any a smooth vector field $W$ on $M$, define a rough vector field on $M$, denoted by $\mathcal L_VW$ and called the *Lie derivative of $W$ with respect to $V$,* by $$
\begin{align*}
(\mathcal L_V W) &:= \left.\frac{d}{dt}\right\rvert_0 d(\theta_{-t})_{\theta_t(p)}(W_{\theta_t(p)}) \\ &= \lim_{t \to 0}\frac{d(\theta_{-t})_{\theta_t(p)}(W_{\theta_t(p)})- W_p}{t},\end{align*} $$provided the derivatives exists.

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
## Commuting Vector Fields

**Def:** Let $M$ be a smooth manifold and $V, W\in {\frak X}(M)$. We say that *$V$ and $W$ commute* if $VWf = WVf$ for every smooth function $f$, or equivalently if $[V, W] = 0$. If $\theta$ is a smooth flow, a vector field $W$ is said to be *invariant under $\theta$* if $W$ is $\theta_t$-related to itself for each $t$; more precisely, this means that $W|_{M_t}$ is $\theta_t$-related to $W|_{M_{-t}}$ for each $t$, or equivalently that $d(\theta_t)_p(W_p) = W_{\theta_t(p)}$ for all $(t, p)$ in the domain of $\theta$.

**Th:** For smooth vector fields $V$ and $W$ on a smooth manifold $M$, the following are equivalent:
- $V$ and $W$ commute.
- $W$ is invariant under the flow of $V$.
- $V$ is invariant under the flow of $W$.

**Cor:** Every smooth vector field is invariant under its own flow.

**Def:** If $\theta$ and $\psi$ are flows on $M$, we say that *$\theta$ and $\psi$ commute* if the following