---
tags:
  - LinearAlgebra
  - CliffordAlgebra
  - DifferentialGeometry
---
Subjects: [[Linear Algebra]], [[Clifford Algebra]], [[Differential Geometry]]
Links: [[Exterior Algebra of Vector Spaces]], [[Symmetric Group]], [[Alternating Groups]]

We ask for $K$ not to have characteristic $2$, for this section.

Remember that $V^{\otimes k}$ is the space of homogeneous tensors of degree $k$. This is spanned by decomposable tensors $$v_1 \otimes v_2 \otimes \dots \otimes v_k,\quad v_i \in V$$
**Def:** The *antisymmetrisation* or *skew-symmetrisation* of decomposable tensors is defined by $$\mathcal A(v_1 \otimes \dots \otimes v_k) := \sum_{\sigma \in S_k} \text{sgn}(\sigma) v_{\sigma(1)} \otimes \dots \otimes v_{\sigma(k)}$$where the sum is taken over the symmetric group and, when the $k! \ne 0$: $$\text{Alt}(v_1 \otimes \dots\otimes v_k) := \frac1{k!} \sum_{\sigma \in S_k} \text{sgn}(\sigma) v_{\sigma(1)} \otimes \dots \otimes v_{\sigma(k)}$$
**Def:** In the language of tensors, a *$p$-vector* is an alternating contravariant tensor of order $p.$ A $p$-vector is denoted by $A_{[p]}$ and characterised by $$A_{[p]} = \text{Alt}(A_{[p]}).$$The brackets here are used to indicate the alternation of the $p$ indices set. Thus, given $A_p \in V^{\otimes p}$, $\text{Alt}(A_p)$ is a $p$-vector. The symbols ${\textstyle \bigwedge}_{p}(V)$ and ${\textstyle \bigwedge}^{\!p}(V)$ respectively denote the space space of $p$-vectors and $p$-covectors.

**Prop:** Let $p\in \Bbb N$, then $$\dim {\textstyle \bigwedge}^{\!p}(V) = \dim {\textstyle \bigwedge}_p(V) = {n \choose p}.$$ 
**Cor:** Let $p\in \Bbb N$, then $$\dim {\bigwedge}_p(V) = \dim {\bigwedge}_{n-p}(V).$$
**Def:** Let $A_{[p]} \in {\textstyle \bigwedge}_p(V)$ be a $p$-vector and let $B_{[q]} \in {\textstyle \bigwedge}_q(V)$ be a $q$ vector. The *exterior product* $\wedge: {\textstyle \bigwedge}_p(V) \times {\textstyle \bigwedge}_q(V) \to {\textstyle \bigwedge}_{p+q}(V)$ is defined by $$A_{[p]} \wedge B_{[q]} := \text{Alt}(A_{[p]} \otimes B_{[q]}).$$
**Prop:** Let $A_{[p]} \in \bigwedge_p(V)$, $B_{[q]}\in {\textstyle \bigwedge}_q(V)$ and $C_{[r]} \in {\textstyle \bigwedge}_r(V)$, then $$(A_{[p]} \wedge B_{[q]}) \wedge C_{[r]} = A_{[p]} \wedge (B_{[q]} \wedge C_{[r]}),$$meaning that $\wedge$ is associative.

**Def:** For $p\in \Bbb N$, we can define a left action and a right action from $S_p$ on ${\textstyle \bigwedge}_p(V)$. 
Let $\sigma\in S_p$, and $A_{[p]} \in {\textstyle \bigwedge}_p(V)$:
- $\sigma(v_1 \otimes \dots \otimes v_p) = \text{sgn}(\sigma) v_{\sigma^{-1}(1)} \otimes \dots v_{\sigma^{-1}(p)}.$
- $(v_1 \otimes \dots \otimes v_p)^\sigma = \text{sgn}(\sigma) v_{\sigma(1)} \otimes \dots \otimes v_{\sigma(n)}.$ 

**Obs:** We get another characterisation of ${\textstyle \bigwedge}_p(V)$, it is a subspace of $V^{\otimes p}$ such that for all $A_{[p]}$ either $\sigma(A_{[p]}) = A_{[p]}$ or $(A_{[p]})^\sigma = A_{[p]}$ for all $\sigma \in S_p$.

**Obs:** The definition of the exterior product is equivalent to $$A_{[p]} \wedge B_{[q]} := \frac{p!q!}{(p+q)!} \sum_{\sigma\in S_{p, q}} \sigma(A_{[p]} \otimes B_{[q]}), $$where $S_{p, q}$ denotes the subset of $S_{p+q}$ containing all $\sigma$ such that $\sigma(i) <\sigma(i+1)$ if $0< i <p$, or $p < i <p+q$. 

**Prop:** From this equation, it follows that $u \wedge v = - v \wedge u$, and $v \wedge v = 0$. 

**Cor:** $A_{[p]} \wedge B_{[q]} = (-1)^{pq} B_{[q]} \wedge A_{[p]}$. 

**Def:** A $p$-vector that can be written as the exterior product of a $p$ number of $1$-vectors is called a *simple* $p$-vector. 

# Bases
Suppose that $V$ is a finite dimensional $K$-vector space, and let $\mathfrak B = \{e_1, \dots, e_n\}$ be a basis for $V$. We can construct the bases for ${\textstyle \bigwedge}_p(V)$. First we need a shortcut in notation, let $\bigwedge_{i \in I} v_i$ is the exterior product of all the elements $\{v_i \mid i \in I\}$ where $I \subseteq \{1, \dots, n\}$ in the order inherited by $I$. With this in mind, we can define the basis of ${\textstyle \bigwedge}_p(V)$ as $$\mathfrak B_p := \left\{\left.\bigwedge_{i \in I} e_i\; \right\rvert \; I \in [\{1, \dots, n\}]^p\right\}$$A consequence of this basis, if $A_{[2]}$, then $$A_{[2]} = \frac12 \sum_{i, j = 1}^n A^{ij} e_i \wedge e_j = \sum_{1 \le i < j \le n} A^{ij} e_i \wedge e_j.$$Notice in the first expression the presence of the factor of $1/2$, which is absent in the second expression. Since, in the sum $\sum_{ij}$, we consider all the values for the indices $i, j \in \{1, \dots, n\}$, as $A^{ij} = -A^{ji}$, and as $e_i \wedge e_j = - e_j \wedge e_i$, we are indeed counting the same term twice. 

We generalise this for ${\textstyle \bigwedge}_p(V)$. An arbitrary element $A_{[p]} \in{\textstyle \bigwedge}_p(V)$ can be written as $$
\begin{align*}
A_{[p]} &:= \frac{1}{p!} \sum_{\mu_1, \dots, \mu_p = 1}^n A^{\mu_1, \dots, \mu_p} e_{\mu_1} \wedge \dots \wedge e_{\mu_p} \\
&= \sum_{1 \le \mu_1 <\dots < \mu_p \le n} A^{\mu_1, \dots, \mu_p} e_{\mu_1} \wedge \dots \wedge e_{\mu_p},
\end{align*}$$where, in the first case, we consider the sum over all posible values for the indices $\mu_i \in \{1, \dots, n\}$ for all $i \in\{1, \dots, p\}$, and, in the second case, we consider the sum over the indices with the restriction that $\mu_1 < \mu_2 < \dots < \mu_p$.

**Convention:** In order to apply the sum convention to $p$-vectors as efficiently as possible, we impose the same restriction on the sum convention with respect to the indices, namely, that $$A^{\mu_1, \dots, \mu_p} e_{\mu_1} \wedge \dots \wedge e_{\mu_p} := \sum_{1 \le \mu_1 <\dots < \mu_p \le n} A^{\mu_1, \dots, \mu_p} e_{\mu_1} \wedge \dots \wedge e_{\mu_p}.$$Thus, we avoid using expressions with the factor $p!$.

An ordered $k$-tuple $I = (i_1,\dots, i_k)$ of a positive integers is called a *[[Multi-index notation|multi-index]]* of length $k.$ If $I$ is such a multi-index and $\sigma\in S_k$ is a permutation we write $I_\sigma$ for the multi-index$$I = (i_{\sigma(1)},\dots, i_{\sigma(k)}).$$
We see that $I_{\sigma\tau} = (I_ \sigma)_\tau$ for $\sigma,\tau\in S_k$. We can extend the Kronecker delta notation in the following way. If $I$ and $J$ are multiindices of length $k$, we define  $$\delta^I_J := \begin{cases}
\text{sgn }\sigma& \text{if neither $I$ nor $J$ has repeadted index and $J = I_\sigma$ for some $\sigma\in S_k$  }\\
0 & \text{If $I$ or $J$ has repated index or $J$ is not a permutation of $I$}. 
\end{cases}
 $$
**Def:** Let $\{e_1,\dots, e_n\}$ be a basis for $V$ and $I$ be a multi-index, we define $$e_I := e_{i_1} \wedge \dots \wedge e_{i_k}. $$
**Obs:** If $J = I_\sigma$, for some multi-indices, then $e_J = (\text{sgn } \sigma )e_I$. 

The significance of this that they provide a more convenient basis for $\bigwedge_p(V)$. We see that the set of $e_I$ is not linearly independent, because some of them are zero and the ones corresponding to different permutations of the same multi-index are constant multiples of each other. A multi-index $I = (i_1,\dots, i_k)$ is said to be *increasing* if $i_1 <\dots <i_k$. This means that using Einstein summation convention we can write a $p$-vector as $$A^I e_I := \sum_{I}' A_I e_I = \sum_{\{I: 1 \le \mu_1 <\dots < \mu_p \le n\}} A^{\mu_1, \dots, \mu_p} e_{\mu_1} \wedge \dots \wedge e_{\mu_p}$$and the set $\{e_I\mid I \text{ is an increasing }p \text{multi-index}\}$ is a basis for $\bigwedge_p(V)$. 

**Def:** Since ${\textstyle \bigwedge}_n(V)$ is a one dimensional $K$-vector space, then we call the elements of ${\textstyle \bigwedge}_n(V)$ are called $n$-vectors, and another usual denomination for $n$-vectors is *psuedoscalars*. 

**Def:** The image $\text{Alt}[T(V)]$ is always the *alternating tensor graded subspace*, it is not algebra yet since we don't have a product, denoted as $A(V)$. 

**Obs:** We have that the kernel of $\mathcal A^{(r)}$ is precisely $I^{(r)}$, the homogeneous subset of the ideal $I$, the kernel of $\mathcal A$ is $I$. 

When $K$ has characteristic $0$, there is a canonical isomorphism $$A(V) \cong {\textstyle \bigwedge}(V).$$With these isomorphisms, we see that exterior algebra of a vector space $V$ over $K$ can be canonically identifies with the vector subspace of $T(V)$ that consists of antisymmetric tensors. With this isomorphism in mind, we don't need to care about ${\textstyle \bigwedge}_p(V)$ as a subspace of $A(V)$ or ${\textstyle \bigwedge}(V)$. 

**Cor:** $\dim {\textstyle \bigwedge}(V) =2^n$.

**Def:** We denote by $\langle \cdot \rangle_p: \bigwedge(V) \to {\textstyle \bigwedge}_p(V)$ as a projection from $\bigwedge (V)$ to a space of $p$-vectors $\langle A\rangle_p := A_{[p]}$.

**Def:** We can define grade involution on ${\textstyle \bigwedge}_p(V)$: $$\#(A_{[p]}) = \widehat A_{[p] } := (-1)^p A_{[p]}. $$For the reversion, it follows that $$\widetilde{(v_1\wedge \dots \wedge v_p)} := v_p \wedge \dots \wedge v_1, $$this implies that $\widetilde A_{[p]} = (-1)^{p(p-1)/2} A_{[p]}$. The conjugation of the two operations $$\overline A_{[p]} := \widetilde{\widehat A}_{[p]} = \widehat{\widetilde A}_{[p]}.$$
# Contraction, or Interior Product

Let $A_{[p]}$ be a $p$-vector and let $\alpha$ be a covector. 

**Def:** The *left contraction* of a $p$-vector $A_{[p]}$ by a covector $\alpha$, denoted from this point on by $\alpha \rfloor$, is defined as $$(\alpha \rfloor A_{[p]})(\alpha_1, \dots, \alpha_{p-1}) := p A_{[p]}(\alpha, \alpha_1, \alpha_2, \dots, \alpha_{p-1}).$$where $\alpha_1, \dots, \alpha_{p-1}$ are arbitrary covectors. Taking $A_{[p]} = v_1 \wedge \dots \wedge v_p$ on the right hand side of the definition  means that $$(v_1\wedge \dots \wedge v_p)(\alpha, \alpha_1, \dots, \alpha_{p-1}) := \frac1{p!} \sum_{\sigma \in S_p} \text{sgn}(\sigma) \alpha(v_{\sigma(1)}) \alpha_1(v_{\sigma(2)})\dots \alpha_{p-1}(v_{\sigma(p)}).$$
This definition shows that $\alpha \rfloor A_{[p]}$ is a $(p-1)$-vector. 

**Lemma:** Let $u, v\in V$ and $\alpha \in V'$, then $$\alpha \rfloor (v \wedge u) = (\alpha \rfloor v)u - v(\alpha \rfloor u) = \alpha(v) u - v \alpha (u).$$
**Prop:** Let $A, B \in {\textstyle \bigwedge}(V)$ and $\alpha \in V'$, then $$(\alpha \rfloor A \wedge B) = (\alpha \rfloor A) \wedge B +\widehat A \wedge (\alpha \rfloor B)
$$
**Def:** The *right contraction* of a $p$-vector $A_{[p]}$ by a covector $\alpha$, denoted from this point on by $\lfloor\alpha$, is defined as $$(A_{[p]} \lfloor \alpha)(\alpha_1, \dots, \alpha_{p-1}) := p A_{[p]}(\alpha_1, \alpha_2, \dots, \alpha_{p-1}, \alpha).$$
**Obs:** Given the definition above, let $v\in V$ and $\alpha \in V'$, then $\alpha \rfloor v = \alpha(v) = v \lfloor \alpha$.

**Prop:** Let $A, B \in \bigwedge(V)$, and $\alpha \in V'$, then $$(A \wedge B) \lfloor \alpha  = A \wedge (B \lfloor \alpha ) + (A \lfloor \alpha ) \wedge\widehat B.$$
**Prop:** Let $A\in \bigwedge (V)$, and $\alpha \in V'$, then $$\alpha \rfloor A = - \widehat A \lfloor \alpha.$$
We can generalise further the left and right contractions to arbitrary covectors. 

**Def:** Given $\alpha_1\wedge \dots \wedge \alpha_p$, we can define $$(\alpha_1 \wedge \alpha_2 \wedge \dots \wedge \alpha_p) \rfloor := \alpha_1 \rfloor \alpha_2\rfloor\cdots \alpha_p\rfloor,$$and $$\lfloor (\alpha_1 \wedge \alpha_2 \wedge \dots \wedge \alpha_p) := \lfloor\alpha_1 \lfloor\alpha_2 \cdots \lfloor \alpha_p.$$
**Obs:** Using this definition of the left contraction of a $2$-covector on $2$-vector we get that $$(\alpha \wedge \beta)\rfloor (u \wedge v) = \alpha(v) \beta(u)- \alpha (u) \beta(v) = 2(\alpha\wedge \beta)(u \wedge v). $$This can generalised further. Let $\Phi^{[p]}$ be a $p$-covector and $A_{[p]}$ a $p$-vector, then $$\Psi^{[p]} (A_{[p]}) = \frac1{p!} \Psi^{[p]}\rfloor A_{[p]}. $$
**Prop:** Let $\Psi^{[p]}$ be a $p$-covector and $A_{[q]}$ a $q$-vector. If $p \le q$, then $$\Psi^{{[p]}}\rfloor A_{[q]} = (-1)^{p(q-1)} A_{[q]} \lfloor \Psi^{[p]}.$$Similarly, if $q \le p$, then $$A_{[q]} \rfloor  \Psi^{[p]} = (-1)^{q(p-1)} \Psi^{[p]}\lfloor A_{[q]}.$$Lastly, $$\widetilde{\Psi^{[p]}\rfloor A_{[q]}} = A_{[q]}\lfloor \Psi^{[p]}. $$

**Obs:** Let us note the equality $$\Psi^{[p]}\rfloor A_{[p]} = A_{[p]} \lfloor\Psi^{[p]} = A_{[p]} \rfloor \Psi^{[p]} = \Psi^{[p]} \lfloor A_{[p]}.$$

### Orientation

In this section we are considering that $K = \Bbb R$. 

There is no criteria that would induce us to prefer the choice of some specific $n$-vector. Ia basis $\mathfrak B := \{e_1, \dots, e_n\}$ of $V$ is taken into account, it is natural to choose the $n$-vector given by the exterior product of the basis vector $\frak B$. No matter the order that such exterior products are taken $e_{\sigma(1)} \wedge \dots \wedge e_{\sigma(n)}$ for every $\sigma \in S_n$, the result is $\pm e_1\wedge \dots \wedge e_n$. 

**Obs:** Let $\{v_1, \dots, v_n\}$ be $n$-linearly independent vectors, then $v_1\wedge \dots \wedge v_n = J e_1\wedge \dots \wedge e_n.$ where $J  > 0$ or $J<0$. 

**Def:** $\Omega$ be a $n$-vector, then we can define two equivalence classes $[\Omega]$ and $[-\Omega]$, as $$\begin{align*}
[\Omega] &:= \left\{\left. A \in { \bigwedge}_n (V)\;\right\rvert\; \exists J >0(A =J\Omega) \right\} \\
[-\Omega] &:= \left\{\left. A \in {\bigwedge}_n (V)\;\right\rvert\; \exists J <0(A =J\Omega) \right\}
\end{align*}.$$These two equivalence classes compromise the *vector space orientation*. 

There exists two possible orientations for a vector space, completely determined once ab $n$-vector has been selected. The choice of an $n$-vector $\Omega_V$ in an equivalence class defines a pair constituted by a vector space $V$ endowed with an $n$-vector $\Omega_V$.

We can define an orientation for the dual space $V'$ via de $n$-covector $\Omega_{V^*}$. The question to be posed is whether the orientation of $V'$ can be related to the orientation of $V$. 

# Duality

If we consider the set of all alternating $k$-linear forms, meaning the set of alternating $k$-linear maps from $V$ to the base field $K$. We see that the set of all alternating $k$-linear forms is a vector space. 

By the universal property the exterior powers, the space of alternating forms of degree $k$ on $V$ is *naturally isomorphic* with the dual space $({\textstyle \bigwedge}_k(V))^*$. Lastly, if $V$ is finite dimensional, then the latter is naturally isomorphic to ${\textstyle \bigwedge}_k(V^*)$. Using the notation, from [[Exterior Algebra of Multicovectors]], then we get that ${\textstyle \bigwedge}^{\!k}(V) = A_k(V) \cong {\textstyle \bigwedge}_k(V^*)$. 