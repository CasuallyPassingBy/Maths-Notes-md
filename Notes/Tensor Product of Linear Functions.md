---
tags:
  - CliffordAlgebra
  - DifferentialGeometry
---
Subjects: [[Clifford Algebra]], [[Differential Geometry]]
Links: [[Tensor Algebra]], [[Tensor Product of Modules]], [[Vectors and Covectors]], [[Dual Vector Spaces]]

# Linear Functions

**Def:** Given a linear map $f: U \to V$, and a vector space $W$, then the *tensor product*: $$f\otimes W : U \otimes W \to V \otimes W $$is the unique linear map such that $$(f \otimes W)(u \otimes w) = f(u)\otimes w. $$The tensor product $W \otimes f$ is defined similarly. 

**Def:** Given two linear maps $f: U \to V$ and $g: W \to Z$, their *tensor product:* $$f\otimes g: U \otimes W \to V \otimes Z $$is the unique linear map that satisfies $$(f \otimes g)(u \otimes w) = f(u)\otimes g(w). $$
Note that we get $$f\otimes g = (f\otimes Z) \circ (U\otimes g) = (V \otimes g) \circ (f\otimes W).$$
If $f$ and $g$ are both injective or surjective, then the same is true for all above the defined linear maps. 

By choosing bases of all vector spaces involved, the linear maps $f$ and $g$ can be represented by matrices. Then, depending on how the tensor $v \otimes w$ is vectorized, the matrix describing the tensor product $f \otimes g$ is the Kronecker product of the two matrices. 

# Linear Functionals

Let $V$ be a $K$-vector space, and the notation $\mathcal L_k(V, K)$ is the space of $k$-linear functionals from $V$ to $K$. By the universal property of the tensor product, we have this isomorphism 
$$\mathcal L_k(V, K) \cong \mathcal L(V^{\otimes k}, K)$$
**Cor:** The $\dim \mathcal L_k(V; \Bbb R) = n^k$. 

**Def:** Let $f \in \mathcal L_k(V; \Bbb R)$ and $g\in \mathcal L_\ell(V; \Bbb R)$. Their *tensor product* is the $(k+\ell)$-linear function $f\otimes g$ defined by: $$(f\otimes g ) (v_1, \dots, v_{k + \ell}) = f(v_1, \dots, v_k) g(v_{k+1}, \dots,v_{k+\ell}) $$
The tensor product is associative: $$f \otimes (g \otimes h) = (f\otimes g) \otimes h$$
**Prop:** Let $V$ be a vector space of dimension $n$ with basis $e_1, \dots, e_n$. Let $\alpha^1, \dots, \alpha^n$ be the dual basis of $V'$. The basis for the space $\mathcal L_k(V; \Bbb R)$ of $k$-linear functions on $V$ is $\{\alpha^{i_1}\otimes \dots \otimes \alpha^{i_k}\}$ for all multi-indices $(i_1, \dots, i_k)$. 

In this case, I am going to consider something change in notation. Let $\mathcal T^2(V) := V' \otimes V'$. Similarly, the space defined by the tensor product between double dual vectors is also a vector space $\mathcal T_2(V) := V'' \otimes V''$. We are going to abuse notation, and if $V$ is finite dimensional, then $V$ is canonically isomorphic to $V''$, then we can say that $\mathcal T_2(V) := V \otimes V$, remember that we are referring to linear functionals in this context.

Let $\mathfrak B := \{e_1, \dots, e_n\}$ be a basis for $V$ and let $\mathfrak B'$ be its dual basis. We know that $\alpha(v) = \alpha_i v^i$, and $\beta(u) = \beta_i u^i$, where $\alpha_i := \alpha(e_i)$; $\beta_i := \beta(e_i)$; $v^i := e^i(v)$; and $u^i := e^i(u)$. This implies that $$ (\alpha \otimes \beta) (v, u) := \alpha_i v^i \beta_j u^j.$$ On the other hand, we have $$(e^i \otimes e^j)(v, u) = v^iu^j.$$Comparing these equations, we can write $$\alpha \otimes \beta = \alpha_i\beta_j e^i \otimes e^j.$$The set of bilinear functionals $\{e^i \otimes e^j \mid 1 \le i, j \le n\}$ is a basis for the space $\mathcal T^2(V)$. If $B$ is an arbitrary bilinear functional, it follows that $B = b_{ij} e^i \otimes e^j,$ where the scalars $b_{ij}$ which are the components of $B$ in this base, are given by $$b_{ij} = B(e_i, e_j).$$Consequently, $B(v, u) = b_{ij} v^iu^j$. Analogously, the set $\{e_i \otimes e_j \mid 1 \le i, j \le n\}$ forms a basis for the space $\mathcal T_2(V)$, namely $A\in \mathcal T_2(V)$, which can be written as $A = a^{ij}e_i \otimes e_j$, where $a^{ij} = A(e^i, e^j)$ are the componentes of $A$ in this basis. 

We know that $V' \otimes V$ and $V \otimes V'$ are canonically isomorphic. Now, we can consider the tensor product of a vector and a covector; this product is called a *mixed bilinear functional.* We denote this space by ${\mathcal {T}^1}_1(V) := V' \otimes V$. A basis for ${\mathcal T^1}_1$ is given by the tensor products $\{e^i \otimes e_j \mid 1 \le i, j \le n\}$. Thus, a tensor $C \in {\mathcal T^1}_1(V)$ can be written as $$C = {c_i}^j e^i \otimes e_j,$$where ${c_i}^j = C(e_i, e^j).$

Similarly, we can define the tensor product of $V \otimes V'$, denoting it by ${\mathcal  T_1}^1 (V)$. An element $D\in {\mathcal T_1}^1 (V)$ can be written as $$D = {d^i}_j e_i\otimes e^j,$$where ${d^i}_j = D(e^i, e_j)$. Although these spaces are naturally isomorphic, we still need to consider the correct positioning of the indices to avoid ambiguity when about which space we are considering when there is a correlation between lowering and raising indices. By convention, we do not take into account the position of the indices, and the notation $\mathcal T^1_1(V)$ refers to the space ${\mathcal T^1}_1(V)$.

The above definitions can be straightforwardly generalised for the tensor product of an arbitrary number of covectors and vectors, defining in such a way the spaces $\mathcal T^p(V) = (V')^{\otimes p}$; $\mathcal T_q(V) = V^{\otimes q}$; ${\mathcal T^p}_q (V) = (V')^{\otimes p} \otimes V^{\otimes q}$; ${\mathcal T_q}^p(V) = V^{\otimes q} \otimes (V')^{\otimes p}$; ${{\mathcal T^1}_q}^p(V) = V' \otimes V^{\otimes q}\otimes (V')^{\otimes p}$; and so on. We adopt the convention that $\mathcal T_q^p(V)$ refers to the space ${\mathcal T^p}_q (V)$.

Consider the space $\mathcal T^p_q(V)$. A basis for this space is given by the set of tensor products $$\{e^{\mu_1} \otimes e^{\mu_2} \otimes \dots \otimes e^{\mu_p} \otimes e_{\nu_1} \otimes e_{\nu_2} \otimes \dots \otimes e_{\nu_q}\mid 1 \le \mu_1, \dots, \mu_p, \nu_1, \dots, \nu_q\le n \}.$$An arbitrary element $T\in \mathcal T^p_q(V)$ can be written as $$T= T^{\nu_1, \dots, \nu_q}_{\mu_1, \dots, \mu_p} e^{\mu_1} \otimes e^{\mu_2} \otimes \dots \otimes e^{\mu_p} \otimes e_{\nu_1} \otimes e_{\nu_2} \otimes \dots \otimes e_{\nu_q},$$where $$T^{\nu_1, \dots, \nu_q}_{\mu_1, \dots, \mu_p} = T(e_{\mu_1},e_{\mu_2}, \dots, e_{\mu_p}, e^{\nu_1}, e^{\nu_2},\dots, e^{\nu_q}).$$The multilinear functional $T\in \mathcal T^p_q(V)$ is called a *tensor of type $(p, q)$*. The quantities $T^{\nu_1, \dots, \nu_q}_{\mu_1, \dots, \mu_p}$ are the components of the tensor $T$ in the given basis.

Tensors of type $(p, 0)$ are sometimes called *covariant tensors*, and tensors of type $(0, q)$ are called *contravariant tensors*. A covector is therefore a tensor of type $(1,0)$ — an example of covariant tensor — whereas a vector is a tensor of type $(0, 1)$ and thus a contravariant tensor.

Under a change of basis $\frak B \to C$, described by $e_j' = B^i_j e_i$, the dual basis transforms according to $e^j = B^j_i e'^i$ , and the components of a vector $v$ and a covector $\alpha$ respectively transform $v^j = B^j_i v'^i$ and $\alpha'_j = B^i_j \alpha_i$. This basis vectors $\frak B$ and the components of a covector transform in a covariant way, and the dual basis vectors $\mathfrak B'$ and the vector components transform in a contravariant way. A generalisation of those results for a type $(p, q)$ is straightforward. 

Indeed, considering a tensor $T$ of type $(p, q)$, the expression for this tensor in the bases $\frak B$ and $\frak C$ is given by $$\begin{align*}
T &= T^{\nu_1, \dots, \nu_q}_{\mu_1, \dots, \mu_p} e^{\mu_1} \otimes e^{\mu_2} \otimes \dots \otimes e^{\mu_p} \otimes e_{\nu_1} \otimes e_{\nu_2} \otimes \dots \otimes e_{\nu_q} \\
&= (T')^{\nu_1, \dots, \nu_q}_{\mu_1, \dots, \mu_p} e^{\mu_1} \otimes e^{\mu_2} \otimes \dots \otimes e^{\mu_p} \otimes e_{\nu_1} \otimes e_{\nu_2} \otimes \dots \otimes e_{\nu_q}
\end{align*}$$