---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Dual Vector Spaces]], [[Exterior Algebra of Multicovectors]], [[Categories and Functors]]

**Prop:** Suppose $V$, $W$ and $S$ are real vector spaces.
- If $\text{id}_V: V \to V$ is the identity map on $V$, then $\text{id}_V': V' \to V'$ is the identity map on $V'$.
- If $f:V \to W$ and $g: W \to S$ are linear maps, then $(g \circ f)' = f' \circ g'$ 

Then the dual construction $\mathcal F: (\;\;) \to (\;\;)'$ is a contravariant functor from the category of vector spaces to itself: for $V$ a real vector space, $\mathcal F(V) = V'$ and for $f \in \mathcal L(V, W)$, $\mathcal F(f) = f' \in \mathcal L(W', V')$. 

We fix a positive integer $k$. For any linear map $L: V \to W$ of vector spaces, define the *pullback map* $L^*: A_k(W) \to A_k(V)$ to be $$(L^* f)(v_1, \dots, v_k) = f(L v_1, \dots, L v_k))$$for $f\in A_k(W)$ and $v_1, \dots, v_k \in V$. It is easy ti see that $L^*$ is linear map.

**Prop:** The pullback of covectors by a linear map satisfies the two functorial properties:
- if $\text{id}_V: V \to V$ is the identity map on $V$, then $\text{id}_V^* = \text{id}_{A_k(V)}$ , the identity map on $A_k(V)$.
- If $K: U \to V$ and $L:V \to W$ are linear maps of vector spaces, then $$(L \circ K)^* = K^* \circ L^*: A_k(W) \to A_k(V)$$