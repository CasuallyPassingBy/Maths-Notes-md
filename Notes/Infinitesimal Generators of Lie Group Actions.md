---
tags:
  - DifferentialGeometry
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Lie Groups]], [[Lie Group Actions]], [[Tangent Distributions and Involutivity on Smooth Manifolds]], [[The Exponential Map on Lie Groups]], [[Lie Algebra of a Lie Group]]

## Right Actions

Suppose we are given a smooth right action of a Lie group $G$ on a smooth manifold $M$, which we denote either by $\theta: M \times G \to M$ or by $(p, g) \mapsto p \cdot g$, depending on the context. Each element $X\in \text{Lie}(G)$ determines a smooth global flow on $M$: $$(t, p) \mapsto p \cdot \exp tX.$$Let $\widehat X \in \mathfrak X(M)$ be the infinitesimal generator of this flow, so for each $p\in M$, $$\widehat X_p := \left.\frac{d}{dt}\right\rvert_{t= 0} p \cdot \exp tX. $$Thus we obtain a map $\widehat\theta: \text{Lie}(G) \to {\frak X}(M)$, defined by $\widehat \theta(X) = \widehat X$. 

There is useful alternative characeterisation of $\widehat X$ in terms of the orbit map $\theta^{(p)}: G \to M$ defined by $\theta^{(p)}(g) = p \cdot g$. Since $\gamma(t) = \exp tX$ is a smooth curve in $G$ whose initial velocity is $\gamma'(0) = X_e$, we see that for each $p\in M$ we have $$d\left(\theta^{(p)}\right)_e(X_e) = \left(\theta^{(p)} \circ \gamma\right)'(0) = \left.\frac{d}{dt}\right\rvert_{t= 0} p \cdot \exp tX = \widehat X_p. $$
**Lemma:** Suppose $G$ is Lie a group and $\theta$ is a smooth right action of $G$ on a smooth manifold $M$. For any $X\in \text{Lie}(G)$ and $p\in M$, the vector fields $X$ and $\hat\theta(X)$ are $\theta^{(p)}$-related. 

**Th:** Suppose $G$ is a Lie group and $\theta$ is a smooth right action of $G$ on a smooth manifold $M$. Then the map $\hat\theta: \text{Lie}(G) \to {\frak X}(M)$ defined above is a Lie algebra homomorphism.

**Def:** The Lie algebra homomorphism $\hat\theta: \text{Lie}(G) \to {\frak X}(M)$ defined above is known as the *infinitesimal generator of $\theta$.* More generally, if $\frak g$ is an arbitrary finite dimensional Lie algebra, any Lie algebra homomorphism $\hat\theta: {\frak g} \to {\frak X}(M)$ is called a *(right) $\frak g$-action on $M$*. A $\frak g$-action $\hat\theta$ is said to be *complete* if for every $X\in \frak g$, the vector field $\hat\theta(X)$ is complete. 

**Fundamental Theorem on Right Lie Algebra Actions:** Let $M$ be a smooth manifolds, let $G$ be a simply connected Lie group, and let ${\frak g} = \text{Lie}(G)$. Suppose $\hat\theta: {\frak g} \to {\frak X}(M)$ is a complete ${\frak g}$-action on $M$. Then there is a unique smooth right $G$-action whose infinitesimal generator is $\hat \theta$.

The proofs relies heavily on [[Foliations on Smooth Manifolds]]. 

## Left Actions

Let $G$ be a Lie group and $M$ be a smooth manifold. If $\theta: G\times M \to M$ is a smooth left action of $G$ on $M$, define the *infinitesimal generator of $\theta$* as the map $\hat \theta: \text{Lie}(G) \to {\frak X}(M)$ given by $\hat\theta(X) = \widehat X$, where $$\widehat X_p := \left.\frac{d}{dt}\right\rvert_{t= 0} (\exp(tX) \cdot p) = d\left(\theta^{(p)}\right)_e (X_e),$$and $\theta^{(p)}: G \to M$ is the orbit mat $\theta^{(p)} (g) = g\cdot p$.

**Th:** Suppose $G$ is a Lie group and $\theta$ is a smooth left action of $G$ on a smooth manifold $M$. Then the map $\hat\theta: \text{Lie}(G) \to {\frak X}(M)$ defined above is a Lie algebra antihomomorphism.

**Fundamental Theorem on Left Lie Algebra Actions:** Let $G$ is a Lie group and $M$ is a smooth manifold. If $G$ is simply connected, every antihomomorphism $\hat\theta: \text{Lie}(G) \to {\frak X}(M)$ such that $\hat\theta(X)$ is complete for each $X\in\text{Lie}(G)$ is the infinitesimal generator for a unique left $G$-action. 

Because of this theorem, for finite-dimensional Lie algebra $\frak g$ and a smooth manifold $M$, a left $\frak g$-action on $M$ is defined as an antihomomorphims from $\frak g$ to ${\frak X}(M)$.