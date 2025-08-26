---
tags:
  - CliffordAlgebra
  - DifferentialGeometry
  - LinearAlgebra
---
Subjects: [[Clifford Algebra]], [[Differential Geometry]], [[Linear Algebra]]
Links: [[Tensor Algebra]], [[Tensor Product of Modules]], [[Vectors and Covectors]], [[Dual Vector Spaces]], [[Correlations, Musical Isomorphisms]]
# Linear Functions

**Def:** Given a linear map $f: U \to V$, and a vector space $W$, then the *tensor product*: $$f\otimes W : U \otimes W \to V \otimes W $$is the unique linear map such that $$(f \otimes W)(u \otimes w) = f(u)\otimes w. $$The tensor product $W \otimes f$ is defined similarly. 

**Def:** Given two linear maps $f: U \to V$ and $g: W \to Z$, their *tensor product:* $$f\otimes g: U \otimes W \to V \otimes Z $$is the unique linear map that satisfies $$(f \otimes g)(u \otimes w) = f(u)\otimes g(w). $$
Note that we get $$f\otimes g = (f\otimes Z) \circ (U\otimes g) = (V \otimes g) \circ (f\otimes W).$$
If $f$ and $g$ are both injective or surjective, then the same is true for all above the defined linear maps. 

By choosing bases of all vector spaces involved, the linear maps $f$ and $g$ can be represented by matrices. Then, depending on how the tensor $v \otimes w$ is vectorized, the matrix describing the tensor product $f \otimes g$ is the Kronecker product of the two matrices. 

**Prop:** Let $T$ and $S$ be two diagonalizable linear operators, then $T \otimes S$ is also diagonalizable, in fact, its eigenvalues are $\{\lambda_i \mu_j \mid 1 \le i \le n \ \land \ 1 \le j \le m\}$ where $\{\lambda_i \mid i \le i \le n \}$ and $\{\mu_j \mid 1 \le j \le m\}$ are the set of all eigenvalues of $T$ and $S$ respectively. Even more so, If $\{v_i \mid i \le n\}$ and $\{w_j \mid 1 \le j \le m\}$ be the eigenvalues of $T$ and $S$, respectively, then $\{v_i \otimes  w_j \mid 1 \le i \le n \ \land \ 1 \le j \le m\}$ is the set of eigenvectors of $T \otimes S$.

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
T &= T^{\nu_1, \dots, \nu_q}_{\mu_1, \dots, \mu_p} \ e^{\mu_1} \otimes e^{\mu_2} \otimes \dots \otimes e^{\mu_p} \otimes e_{\nu_1} \otimes e_{\nu_2} \otimes \dots \otimes e_{\nu_q} \\
&= (T')^{\nu_1, \dots, \nu_q}_{\mu_1, \dots, \mu_p} \ e'^{\mu_1} \otimes e'^{\mu_2} \otimes \dots \otimes e'^{\mu_p} \otimes e'_{\nu_1} \otimes e'_{\nu_2} \otimes \dots \otimes e'_{\nu_q}.
\end{align*}$$Now, when we substitute the basis change $e'_{\mu_i} = B_{\mu_i}^{\nu_i}e_{\nu_i}$ and the corresponding transformation $e'^{\mu_i} = (B^{-1})_{\nu_i}^{\mu_i}e^{\nu_i}$ in the expression, it then reads $$T^{\rho_1, \rho_2, \dots, \rho_q}_{\sigma_1, \sigma_2, \dots, \sigma_p} = (T')^{\nu_1, \nu_2, \dots, \nu_q}_{\mu_1, \mu_2, \dots, \mu_p}(B^{-1})_{\sigma_1}^{\mu_1} \cdots (B^{-1})_{\sigma_p}^{\mu_p} B^{\rho_1}_{\nu_1} \cdots B^{\rho_q}_{\nu_q},$$and $$(T')^{\rho_1, \rho_2, \dots, \rho_q}_{\sigma_1, \sigma_2, \dots, \sigma_p} = T^{\nu_1, \nu_2, \dots, \nu_q}_{\mu_1, \mu_2, \dots, \mu_p} B_{\sigma_1}^{\mu_1} \cdots B_{\sigma_p}^{\mu_p} (B^{-1})^{\rho_1}_{\nu_1} \cdots (B^{-1})^{\rho_q}_{\nu_q}.$$Hence, the *covariant* components transform in the same way as a covector. On the other had the *contravariant* component transform in the same way as the vector components do. 

Note that $V\otimes V'$ is isomorphic to $\mathcal L(V)$. The isomorphism in question is $\phi_V: V \otimes V' \to \mathcal L(V)$, for any $v\in V$ and $\alpha\in V'$, then $\phi_V(v \otimes \alpha)(u) = v\alpha(u)$ for all $u \in V$. We see that $T = \phi_V(T^i_j e_i \otimes e^j)$, where $T e_i = T^j_i e_j$. 

We can generalise this result further to $\mathcal T^p_{q+1}(V)$ is naturally isomorphic to $\mathcal L(V'^{\otimes q} \otimes V^{\otimes k}, V)$.  ^5d22c0

We can use this last result to get a natural operation called *trace* or *contraction*, which lowers the rank of a tensor by $2$. We define $\text{tr}: \mathcal T^{p+1}_{q+1}(V) \to \mathcal T^p_q(V)$ to be the trace of the endomorphism $$F(\omega^1, \dots, \omega^q, \cdot, V_1, \dots, V_p, \cdot) \in \mathcal T^1_1(V).  $$
In terms of a basis the components of $\text{tr}(F)$ are $$\text{tr}(F)^{\nu_1, \dots, \nu_p}_{\mu_1, \dots, \mu_q} = F^{\nu_1, \dots, \nu_p, m}_{\mu_1, \dots, \mu_q, m}$$
# Tensor Algebra of Linear Functionals

**Def:** Given two tensors $T$ and $S$ of type $(p, q)$, it is possible to define their sum as the tensor $T+S$ of type $(p, q)$ in terms of their components by $$(T+S)^{\nu_1, \nu_2, \dots, \nu_q}_{\mu_1, \mu_2, \dots, \mu_p} := T^{\nu_1, \nu_2, \dots, \nu_q}_{\mu_1, \mu_2, \dots, \mu_p}+ S^{\nu_1, \nu_2, \dots, \nu_q}_{\mu_1, \mu_2, \dots, \mu_p}.$$
**Def:** If $T$ is tensor of type $(p,q )$ and $S$ is a tensor of type $(r,s)$, we can define a tensor product $T \otimes S$ which is a tensor of type $(p+r, q+s)$. In terms of components it follows that $$(T \otimes S)^{\nu_1, \nu_2, \dots, \nu_q\rho_1, \rho_2, \dots, \rho_s}_{\mu_1, \mu_2, \dots, \mu_p, \sigma_1, \sigma_2, \dots, \sigma_r} := T^{\nu_1, \nu_2, \dots, \nu_q}_{\mu_1, \mu_2, \dots, \mu_p} S^{\rho_1, \rho_2, \dots, \rho_s}_{\sigma_1, \sigma_2, \dots, \sigma_r}.$$
**Obs:** The tensor product is distributive with respect to the sum, namely $(T+ S) \otimes R = T \otimes R + S \otimes R$ and $T \otimes (S+R) = T \otimes S + T\otimes R$; in addition it is associative: $T \otimes (S \otimes R) = (T \otimes S ) \otimes R$. 

**Def:** The direct sum of all vector spaces $\mathcal T^p_q(V)$ endowed with the operations of sum and tensor product is called the *tensor algebra of linear functionals* associated with the vector space $V$. The tensor algebra of linear functionals is graded algebra. In the general case, the grading is given $\Bbb Z \times \Bbb Z$, and it is positive. The are two cases particularly important: the algebra of the covariant tensors and that of the contravariant tensors.
- The algebra of the covariant tensors is denoted by $\mathcal T^*(V) := \bigoplus_{p = 0}^\infty \mathcal T^p(V)$.
- The algebra of the contravariant tensors is denoted by $\mathcal T(V) := \bigoplus_{q = 0}^\infty \mathcal T_q(V)$.
The graded algebra of the contravariant tensors, and the algebra of the contravariant tensors are $\Bbb Z$-graded algebras.

**Def:** Let us consider the algebra of the covariant tensors $\mathcal T^*(V)$. Since it is $\Bbb Z$-graded, it allows us to define a mapping called the *grade involution* as $$\# (T_p) (-1)^{\deg T_p} T_p = (-1)^p T_p,$$where $T_p \in \mathcal T^p(V) \subseteq\mathcal T^*(V)$. Another notation can be used for grade involution is $$\widehat{T_p} = \#( T_p).$$
**Obs:** The mapping $\#$ is an automorphism. Since $\#(T_p \otimes S_q) = \#(T_p) \otimes \#(S_q)$. Additionally, it also satisfies $\#^2 = 1$, where $1$ represents the identity mapping.

Since $\#^2 = 1$, there is a refinement in the grading of $\mathcal T^*(V)$. An element $T_p \in \mathcal T^p(V)$ is said to be *even* of *odd* if $(-1)^p$ is respectively positive or negative. In this way, the operators $\Pi_+$ and $\Pi_-$ can be defined as $$\Pi_+ := \frac12 (1+\#), \qquad \Pi_- := \frac12(1-\#).$$These operators $\Pi_+$ and $\Pi_-$ are projectors, as can be straightforwardly verified. The subspace $\mathcal T^*_+(V) := \Pi_+[\mathcal T^*(V)]$  consists of the even elements in $\mathcal T^*(V)$, and the subspace $\mathcal T^*_-(V) := \Pi_-[\mathcal T^*(V)]$ consists of all odd elements. It is then possible to write $\mathcal T^*(V) = \mathcal T^*_+(V) \oplus \mathcal T^*_-(V)$, and $$\mathcal T^*_\pm(V) \otimes \mathcal T^*_\pm(V) \subseteq \mathcal T^*_+(V), \qquad \mathcal T^*_\pm(V) \otimes \mathcal T^*_\mp (V) \subseteq T^*_-(V).$$The grade involution endows both the algebras of covariant and contravariant tensors with $\Bbb Z/ 2\Bbb Z$-grading.

**Def:** Another prominent and very useful mapping is called *reversion*, denoted by a tilde and defined by $$\widetilde{(T_p \otimes S_q)} := \widetilde{S_q} \otimes \widetilde{T_p},$$for all $T_p \in \mathcal T^p(V)$, and $S_q \in \mathcal T^q(V)$, where
- for all $a\in K$, $\widetilde a = a$.
- $\widetilde \alpha = \alpha$ for all $\alpha \in V' = \mathcal T^1(V)$.

**Obs:** This definition implies that $$\widetilde{(\alpha_1 \otimes \alpha_2 \otimes \dots \otimes \alpha_p)} = \alpha_p \otimes \dots\otimes \alpha_2 \otimes \alpha_1,$$for $\{\alpha_k \mid 1\le k\le p\} \subseteq V'$, which justifies the name reversion. 

**Def:** The composition of grade involution and the reversion is called *conjutation* and it is denoted by a bar: $$\overline  T_p := \#\left(\widetilde{T_p}\right) = \widetilde{\#(T_p)}. $$