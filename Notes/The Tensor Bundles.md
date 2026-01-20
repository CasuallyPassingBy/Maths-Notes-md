---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Tensor Product of Linear Functions]], [[The Tangent Bundle]], [[The Cotangent Bundle]] [[Local and Global Sections of Vector Bundles]], [[Covector Fields on Smooth Manifolds]]

**Def:** Let $M$ be a smooth manifold with or without boundary. We define the *bundle of covariant $k$-tensors on $M$* by $$T^k T^*M := \coprod_{p\in M} T^k(T^*_p M) = \coprod_{p\in M} (T_p^*M)^{\otimes k}. $$Analogously, we define the *bundle of contravariant $k$-tensors* by $$T^k TM := \coprod_{p\in M} T^k(T_p M) = \coprod_{p\in M} (T_pM)^{\otimes k},$$and the *bundle of mixed tensors of type $(k, l)$* by $$T^{(k, l)} TM := \coprod_{p\in M} T^{(k, l)} (T_p M) = \coprod_{p\in M} \mathcal T^k_l (T_p M). $$

Any one of these bundle is called a *tensor bundle over $M$*. A section of a tensor bundle is called a *(covariant, contravariant, or mixed) tensor field on $M$*. A *smooth tensor field* is a section that is smooth in the usual sense of smooth sections of vector bundles. 

**Prop:** The spaces of smooth sections of these tensor bundles, $\Gamma(T^k T^*M)$, $\Gamma(T^k TM)$ and $\Gamma(T^{(k, l)}TM)$, are infinite-dimensional vector spaces over $\Bbb R$, and modules over ${\cal C}^\infty (M)$. 

In any smooth local coordinates $(x^i)$, sections of these bundles can be written as $$A = \begin{cases} A_{i_1,\dots, i_k} dx^{i_1}\otimes \dots\otimes dx^{i_k}, & A\in \Gamma(T^k T^* M); \\ A ^{i_1,\dots, i_k} \dfrac{\partial}{\partial x^{i_1}}\otimes \dots \otimes\dfrac{\partial}{\partial x^{i_k}}, & A\in \Gamma(T^kTM); \\
A ^{i_1,\dots, i_k}_{j_1,\dots, j_l} \dfrac{\partial}{\partial x^{i_1}}\otimes \dots \otimes\dfrac{\partial}{\partial x^{i_k}} \otimes dx^{j_1}\otimes \dots\otimes dx^{j_l}, & A\in \Gamma(T^{(k, l)}TM).
\end{cases} $$The functions $A_{i_1,\dots i_k}$, $A^{i_1,\dots, i_k}$, or $A ^{i_1,\dots, i_k}_{j_1,\dots, j_l}$ are called the *component functions of $A$* in the chosen coordinates. 

Because smooth covariant tensor fields occupy most of our attention, we adopt the following shorthand notation for the space of all smooth covariant $k$-tensor fields: $$\mathcal T^k (M) := \Gamma(T^k T^* M). $$
**Smoothness Criteria for Tenser Fields:** Let $M$ be a smooth manifold with or without boundary, and let $A: M \to T^k T^*M$ be a rough section. The following are equivalent.
- $A$ is smooth.
- In every smooth coordinate chart, the component functions of $A$ are smooth.
- Each point of $M$ is contained in some coordinate chart in which $A$ has smooth component functions.
- If $X_1,\dots, X_k \in {\frak X}(M)$, then the function $A(X_1,\dots, X_k): M \to \Bbb R$, defined by $$A(X_1,\dots, X_k)(p) = A_p(X_1|_p,\dots, X_k|_p), $$is smooth.
- Whenever $X_1,\dots, X_k$ are smooth vector fields defined on some open subset $U\subseteq M$, the function $A(X_1,\dots, X_k)$ is smooth on $U$. 

**Prop:** Suppose $M$ is a smooth manifold with or without boundary, $A\in {\cal T}^k(M)$, $B\in {\cal T}^l(M)$ and $f\in {\cal C}^\infty(M)$. Then $fA$ and $A \otimes B$ are also smooth tensor fields, whose components in any smooth local coordinate chart are $$\begin{align*} (fA)_{i_1,\dots, i_k} &= fA_{i_1,\dots, i_k}, \\ (A \otimes B)_{i_1, \dots, i_{k+l}} &= A_{i_1,\dots, i_k} B_{i_{k+1},\dots, i_{k+l}}.\end{align*} $$
**Tensor Characterisation Lemma:** A map $${\cal A}: {\frak X}(M)^k \to \mathcal C^\infty(M), $$is induced by a smooth covariant $k$-tensor field iff it is a multilinear over ${\cal C}^\infty(M)$. 

**Def:** A *symmetric tensor field* on a manifold with or without boundary is simply a covariant tensor field whose value at each point is a [[Tensor Product of Linear Functions#Symmetric Tensors|symmetric tensor]]. The symmetric product of two or more tensor field is defined pointwise, just like the tensor product. 

## Pullbacks of Tensor Fields

Just like covector fields, covariant tensor fields can be pulled back by a smooth map to yield a tensor field on the domain. 

Suppose $F: M \to N$ is a smooth map. For any point $p\in M$ and any $k$-tensor $\alpha\in T^k(T^*_{F(p)} N)$, we define a tensor $dF^*_p(\alpha) \in T^k(T^*_p M)$, called the *pullback of $\alpha$ by $F$ at $p$*, by $$dF^*_p(\alpha)(v_1,\dots, v_k) = \alpha (dF_p(v_1),\dots, dF_p(v_k)) $$for any $v_1,\dots, v_k\in T_p M$. If $A$ is a covariant $k$-tensor field on $N$, we define a rough $k$-tensor field $F^*A$ on $M$, called the *pullback of $A$ by $F$*, by  $$(F^*A)_p := dF^*_p(A(_{F(p)}).$$This tensor fields acts on vectors $v_1,\dots, v_k\in T_p M$ by  $$(F^* A)_p (v_1,\dots, v_k) = A_{F(p)}(dF_p(v_1),\dots, dF_p(v_k)). $$
**Properties of Tensor Pullbacks:** Suppose $F: M \to N$ and $G: N \to P$ are smooth maps, and $A$ and $B$ are covariant tensor fields on $N$, and $f$ is a real-valued function on $N$. 
- $F^*(fB) = (f\circ F) F^* B$.
- $F^*(A \otimes B) = F^* A \otimes F^* B$. 
- $F^*(A+B) = F^*A+ F^* B$.
- $F^*B$ is a continuous tensor field, and is smooth if $B$ is smooth.
- $(G \circ F)^* B = F^* (G^* B)$.
- $(\text{id}_N)^*B = B$. 
- If $A$ and $B$ are symmetric tensor fields on $N$, then $F^*A$ and $F^*B$ are symmetric, and $F^*(AB) = (F^*A)(F^*B)$.

**Cor:** Let $F: M \to N$ be smooth, and let $B$ be a covariant $k$-tensor field on $N$. If $p\in M$ and $(y^i)$ are smooth coordinates for $N$ on a neighbourhood of $F(p)$, then $F^*B$ has the following expression in a neighbourhood of $p$:  $$F^*(B_{i_1,\dots, i_k} dy^{i_1}\otimes \dots \otimes dy^{i_k}) = (B_{i_1,\dots, i_j} \circ F) d(y^{i_1}\circ F) \otimes d(y^{i_k}\circ F).$$
**Cor:** Let $M$ be a smooth $n$-manifold and let $A$ be a smooth tensor field on $M$. If $(U, (x^i))$ and $(V, (y^j))$ are overlapping smooth charts on $M$, we can write $$\begin{align*}
A &= A ^{i_1,\dots, i_k}_{j_1,\dots, j_l} \dfrac{\partial}{\partial x^{i_1}}\otimes \dots \otimes\dfrac{\partial}{\partial x^{i_k}} \otimes dx^{j_1}\otimes \dots\otimes dx^{j_l} \\
&= \widetilde A ^{i_1,\dots, i_k}_{j_1,\dots, j_l} \dfrac{\partial}{\partial y^{i_1}}\otimes \dots \otimes\dfrac{\partial}{\partial y^{i_k}} \otimes dy^{j_1}\otimes \dots\otimes dy^{j_l}\end{align*}.$$We can calculate the relation ship between $A^{i_1,\dots, i_k}_{j_1,\dots, j_l}$ and $\widetilde A ^{i_1,\dots, i_k}_{j_1,\dots, j_l}$, as $$\widetilde A ^{i_1,\dots, i_k}_{j_1,\dots, j_l} = A^{m_1,\dots, m_k}_{n_1,\dots, n_l} \frac{\partial y^{i_1}}{\partial x^{m_1}}\cdots \frac{\partial y^{i_k}}{\partial x^{m_k}} \frac{\partial x^{n_1}}{\partial y^{j_1}} \dots \frac{\partial x^{n_l}}{\partial y^{j_l}}.$$
**Prop:** For every pair of nonnegative integers $k, l$ and every diffeomorphism $F: M \to N$ are the pushforward and pullback isomorphisms.
- $F_*: \Gamma(T^{(k, l)} TM) \to \Gamma(T^{(k, l)} TN),$
- $F_*: \Gamma(T^{(k, l)} TN) \to \Gamma(T^{(k, l)} TM)$,
such that $F^*$ agrees with the usual pullback on covariant tensor fields, $F_*$ agrees with the usual pushforward on contravariant $1$-tensor fields, and the following conditions are satisfied:
- $F_* = (F^*)^{-1}$.
- $F^*(A \otimes B) = F^* A \otimes F^* B$.
- $(F\circ G)_* = F_* \circ G_*$.
- $(F\circ G)^* = G^* \circ F^*$.
- $(\text{id}_M)^* = (\text{id}_M)_* = \text{id}: \Gamma(T^{(k, l)} TM)\to \Gamma(T^{(k, l)} TM)$. 
- $F^*(A(X_1,\dots, X_k)) = F^*A (F_*^{-1}(X_1),\dots, F_*^{-1}(X_k))$ for $A\in \mathcal T^k(N)$ and $X_1,\dots, X_k\in {\frak X}(N)$. 