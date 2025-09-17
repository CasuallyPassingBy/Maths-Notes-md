---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Tensor Product of Linear Functions]], [[The Tangent Bundle]], [[The Cotangent Bundle]]

On a manifold $M$, we can perform the same linear algebraic constructions on each tangent space $T_p M$ that we can perform on any vector space, yielding tensors at $p$. For example a $(k, q)$-tensor at $p\in M$ is just an element of $\mathcal T^k_q(T_p M)$. We define the *bundle of $(k,q)$-tensors* on $M$ as $$ T^k_q M := \coprod_{p \in M} \mathcal T^k_q(T_p M).$$
To see that each of these tensor bundles is a vector bundle, we define the projection $\pi: T^k_q M \to M$. If $(x^i)$ are the local coordinates on $U \subseteq M$, and $p \in U$, the coordinate vectors $\left\{\dfrac{\partial}{\partial x^i}\right\}$ for a basis for $T_p M$ whose dual basis is $\{dx^i\}$. Any tensor $F \in \mathcal T^k_q(T_p M)$ can be expressed in terms of this basis as $$F = F^{\nu_1, \dots, \nu_k}_{\mu_1,\dots, \mu_q} \frac{\partial}{\partial x^{\nu_1}} \otimes \dots\otimes  \frac{\partial}{\partial x^{\nu_k}}\otimes dx^{\mu_1}\otimes \dots \otimes dx^{\mu_q}. $$If the coordinate frame is clear, and we don't want to explicit about the dependency we can simplify the notation to $$F = F^{\nu_1, \dots, \nu_k}_{\mu_1,\dots, \mu_q} \partial_{\nu_1}\otimes \dots\otimes  \partial_{\nu_k}\otimes dx^{\mu_1}\otimes \dots \otimes dx^{\mu_q}. $$
We can check that $T^k_qM$ can be made into a smooth vector bundle in a unique way so that all such maps the intuitive trivialisations are the local trivilisation. 

**Def:** A *tensor field* on $M$ is a smooth section of some tensor bundle $T^k_q M$. To avoid confusion between the point $p\in M$ at which a tensor field is evaluated and the vectors and covectors to which it is applied we usually write the value of a tensor field $F$ at $p\in M$ as $F_p \in T^k_q(T_p M)$, or to make it even clearer as $F |_p$. 

**Def:** The space of $(k, q)$-tensor fields is denoted as $\mathcal T^k_q (M)$ (which can be understood by context), the space of covariant $k$-tensor fields by $\mathcal T^k (M)$. In particular, $\mathcal T^1(M)$ is the space of $1$-forms, meaning that $\mathcal T^1(M) = \Omega^1(M)$.

We can also write this definition in a symbolic manner, $\mathcal T^k_q(M) := \Gamma(T^k_q M)$, and $\mathcal T^k (M) := \Gamma(T^k M)$. 

In terms of any local frame, a $(k, q)$-tensor field $F$ can be written in terms of the basis, where now the components $F^{\nu_1, \dots, \nu_k}_{\mu_1, \dots, \mu_q}$ are to be interpreted as functions on $U$. In particular, in terms of a coordinate frame $\{\partial_i\}$ and its duall coframe $\{dx^i\}$, $F$ has the coordinate expression $$F_p = F^{\nu_1, \dots, \nu_k}_{\mu_1,\dots, \mu_q}(p) \partial_{\nu_1}\otimes \dots\otimes  \partial_{\nu_k}\otimes dx^{\mu_1}\otimes \dots \otimes dx^{\mu_q}.$$
**Prop:** Let $F: M \to T^k_qM$ be a section. $F$ is a smooth tensor field iff whenever $\{X_i\}$ are smooth vector fields and $\{\omega^j\}$ are smooth $1$-forms on an open set $U \subseteq M$, the function $F(\omega_1,\dots, \omega^q, X_1\dots, X_k)$ on $U$, defined by $$F(\omega_1,\dots, \omega^q, X_1\dots, X_k)(p) = F_p(\omega_1,\dots, \omega^q, X_1\dots, X_k),$$ is smooth.

**Obs:** Let $F: M \to T^k_qM$ is a section. $F$ is smooth iff every one of its components is smooth.

Given a tensor field $F: \in \mathcal T^k_q(M)$, vector fields $X_i\in \mathcal T(M)$ , and $1$-forme $\mathcal T^1(M)$, $F$ induces a map $$F: \mathcal T^1(M) \times \dots \mathcal T^1(M)  \times \mathcal T(M) \times \mathcal T(M) \to \mathcal C^\infty(M).$$We can see that this map is *multilinear over $\mathcal C^\infty (M)$*. 

**Prop:** A map   $$\tau:\mathcal T^1(M) \times \dots \mathcal T^1(M)  \times \mathcal T(M) \times \mathcal T(M) \to \mathcal C^\infty(M)$$is induced by $(k, q)$-tensor field as above iff it is a multilinear map over $\mathcal C^\infty (M)$. Similarly, a map $$\mathcal T^1(M) \times \dots \mathcal T^1(M)  \times \mathcal T(M) \times \mathcal T(M) \to \mathcal T(M)$$ is induced by a $(k, q+1)$-tensor field iff it is multilinear over $\mathcal C^\infty(M)$. This has the same property as [[Tensor Product of Linear Functions#^5d22c0|tensors]]. 

# Pullbacks

If $F: M \to N$ is a smooth map, for each integer $k \ge 0$ and each $p\in M$ we obtain a map $F^*: T^k(T_{F(p)} N) \to T^k (T_p M)$ called the *pullback* by $$(F^*S)(X_1, \dots, X_k) := S(F_*X_1, \dots, F_*X_k).$$
**Properties of Tensor Pullbacks:** Suppose $F:M \to N$ and $G:N \to P$ are smooth maps, $p\in M$, $S\in T^k(T_{F(p)} N)$ and $T\in T^l(T_{F(p)} N)$. 
- $F^*:T^k(T_{F(p)} N) \to T^k(T_p M)$ is linear over $\Bbb R$.
- $F^*(S \otimes T) = F^* S \otimes F^* T$
- $(G\circ F)^*= F^* \circ G^*: T^k(T_{(G\circ F)(p)} P) \to T^k(T_p M)$
- $(\text{Id}_N)^*S = S$
- $F^*: T^k N \to T^k M$ is a smooth bundle map. 

We see that the assignments $M \mapsto T^k M$ and $F\mapsto F^*$ yield a contravariant functor.

**Properties of Tensor Field Pullbacks:** Suppose $F:M \to N$ and $G:N \to P$ are smooth maps, $p\in M$, $\sigma\in \mathcal T^k(T_{F(p)} N)$,  $\tau\in \mathcal T^l(T_{F(p)} N)$, and $f\in \mathcal C^\infty(N)$. 
- $F^*(f \sigma) = (f \circ F) F^*\sigma$.
- $F^*(\sigma \otimes \tau) = F^*\sigma \otimes F^*\tau$. 
- $F^*\sigma$ is a smooth vector field
- $F^*: \mathcal T^k(N) \to \mathcal T^k(M)$ is linear over $\Bbb R$
- $(G\circ F)^*= F^* \circ G^*$
- $(\text{Id}_N)^*\sigma = \sigma$

**Cor:** Let $F:M \to N$ be smooth, and let 