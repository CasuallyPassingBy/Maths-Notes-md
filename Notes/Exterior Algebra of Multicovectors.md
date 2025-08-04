---
tags:
  - DifferentialGeometry
  - LinearAlgebra
  - CliffordAlgebra
---
Subjects: [[Differential Geometry]], [[Linear Algebra]], [[Clifford Algebra]]
Links: [[Dual Vector Spaces]], [[Exterior Algebra]], [[Multilinear Transformations]], [[Tensor Product of Modules]],  [[Graded Ring]], [[Tensor Product of Linear Functions]]

Let $K$ be characteristic $0$ field. We are going to drop, the fact that the codomain is $K$ for the rest of the note, since this notation is a bit cumbersome. 

**Def:** Let us consider a covariant tensor of the form $X_1\otimes X_2 \otimes \dots \otimes X_p$, where $X$ denotes respectively either a vector or a covector, and the indices enumerate such elements. The operator $\text{Alt}$ is called *alternator* if defined in the following way: $$\text{Alt}(X_1\otimes X_2 \otimes \dots \otimes X_p) := \frac{1}{p!} \sum_{\sigma \in S_p} \text{sgn}(\sigma) X_{\sigma(1})\otimes X_{\sigma(2)} \otimes \dots \otimes X_{\sigma(p)}.$$

**Def:** In the language of tensors, a *$p$-covector* is an alternating covariant tensor of order $p.$ A $p$-covector is denoted by $\Psi^{[p]}$ and characterised by $$\Psi^{[p]} = \text{Alt}(\Psi^{[p]}).$$The brackets here are used to indicate the alternation of the $p$ indices set. Thus, given $\Psi^p \in (V')^{\otimes p}$, $\text{Alt}(\Psi^p)$ is a $p$-covector.The symbols ${\textstyle \bigwedge}^{p}(V)$ and ${\textstyle \bigwedge}_{p}(V)$ respectively denote the space space of $p$-vectors and $p$-covectors.

**Prop:** Let $p\in \Bbb N$, then $$\dim {\textstyle \bigwedge}^{\!p}(V) = \dim {\textstyle \bigwedge}_p(V) = {n \choose p}.$$ 
**Cor:** Let $p\in \Bbb N$, then $$\dim {\textstyle \bigwedge}^{\!p}(V) = \dim {\textstyle \bigwedge}^{\!n-p}(V).$$
**Def:** Let $\Psi^{[p]} \in {\textstyle \bigwedge}^{\!p}(V)$ be a $p$-covector and let $\Phi^{[q]} \in {\textstyle \bigwedge}^{\!q}(V)$ be a $q$ vector. The *exterior product* $\wedge: {\textstyle \bigwedge}_p(V) \times {\textstyle \bigwedge}_q(V) \to {\textstyle \bigwedge}^{\!p+q}(V)$ is defined by $$\Psi^{[p]} \wedge \Phi^{[q]} := \text{Alt}(\Phi^{[p]} \otimes \Phi^{[q]}).$$
**Prop:** Let $\Psi^{[p]} \in {\textstyle \bigwedge}^{\!p}(V)$, $\Phi^{[q]}\in {\textstyle \bigwedge}^{\!q}(V)$ and $\Xi^{[r]} \in {\textstyle \bigwedge}^{\!r}(V)$, then $$(\Psi^{[p]} \wedge \Phi^{[q]}) \wedge \Xi^{[r]} = \Psi^{[p]} \wedge (\Phi^{[q]})  \wedge \Xi^{[r]}),$$meaning that $\wedge$ is associative.

**Def:** For $p\in \Bbb N$, we can define a left action and a right action from $S_p$ on ${\textstyle \bigwedge}^{\!p}(V)$. 
Let $\sigma\in S_p$, and $A_{[p]} \in {\textstyle \bigwedge}^{\!p}(V)$:
- $\sigma(\alpha_1 \otimes \dots \otimes \alpha_p) = \text{sgn}(\sigma) \alpha_{\sigma^{-1}(1)} \otimes \dots \alpha_{\sigma^{-1}(p)}.$
- $(\alpha_1 \otimes \dots \otimes \alpha_p)^\sigma = \text{sgn}(\sigma) \alpha_{\sigma(1)} \otimes \dots \otimes \alpha_{\sigma(n)}.$ 

**Obs:** We get another characterization of ${\textstyle \bigwedge}^{\!p}(V)$, it is a subspace of $(V')^{\otimes p}$ such that for all $\Psi^{[p]}$ either $\sigma(\Psi^{[p]}) = \Psi^{[p]}$ or $(\Psi^{[p]})^\sigma = \Psi^{[p]}$ for all $\sigma \in S_p$.

**Obs:** The definition of the exterior product is equivalent to $$\Psi^{[p]} \wedge \Phi^{[q]} := \frac{p!q!}{(p+q)!} \sum_{\sigma\in S_{p, q}} \sigma(\Psi^{[p]} \otimes \Phi^{[q]}), $$where $S_{p, q}$ denotes the subset of $S_{p+q}$ containing all $\sigma$ such that $\sigma(i) <\sigma(i+1)$ if $0< i <p$, or $p < i <p+q$. 

**Prop:** From this equation, it follows that $u \wedge v = - v \wedge u$, and $v \wedge v = 0$. 

**Cor:** $\Psi^{[p]} \wedge \Phi^{[q]} = (-1)^{pq} \Phi^{[q]} \wedge \Psi^{[p]}$. 

**Def:** A $p$-covector that can be written as the exterior product of a $p$ number of $1$-covectors is called a *simple* $p$-covector. 

#### Bases
Suppose that $V$ is a finite dimensional $K$-vector space, and let $\mathfrak B = \{e_1, \dots, e_n\}$ be a basis for $V$. We can construct the bases for ${\textstyle \bigwedge}^{\!p}(V)$. First we need a shortcut in notation, let $\bigwedge_{i \in I} v_i$ is the exterior product of all the elements $\{v_i \mid i \in I\}$ where $I \subseteq \{1, \dots, n\}$ in the order inherited by $I$. With this in mind, we can define the basis of ${\textstyle \bigwedge}^{\!p}(V)$ as $$\mathfrak B'_p := \left\{\left.\bigwedge_{i \in I} e^i\; \right\rvert \; I \in [\{1, \dots, n\}]^p\right\}$$A consequence of this basis, if $\Psi^{[2]}$, then $$\Psi^{[2]} = \frac12 \sum_{i, j = 1}^n \Psi_{ij} e^i \wedge e^j = \sum_{1 \le i < j \le n} \Psi_{ij} e^i \wedge e^j.$$Notice in the first expression the presence of the factor of $1/2$, which is absent in the second expression. Since, in the sum $\sum_{ij}$, we consider all the values for the indices $i, j \in \{1, \dots, n\}$, as $\Psi_{ij} = -\Psi_{ji}$, and as $e_i \wedge e_j = - e_j \wedge e_i$, we are indeed counting the same term twice. 

We generalise this for ${\textstyle \bigwedge}^{\!p}(V)$. An arbitrary element $\Psi^{[p]} \in{\textstyle \bigwedge}^{\!p}(V)$ can be written as $$
\begin{align*}
\Psi^{[p]} &:= \frac{1}{p!} \sum_{\mu_1, \dots, \mu_p = 1}^n \Psi_{\mu_1, \dots, \mu_p} e^{\mu_1} \wedge \dots \wedge e^{\mu_p} \\
&= \sum_{1 \le \mu_1 <\dots < \mu_p \le n} \Psi_{\mu_1, \dots, \mu_p} e^{\mu_1} \wedge \dots \wedge e^{\mu_p},
\end{align*}$$where, in the first case, we consider the sum over all posible values for the indices $\mu_i \in \{1, \dots, n\}$ for all $i \in\{1, \dots, p\}$, and, in the second case, we consider the sum over the indices with the restriction that $\mu_1 < \mu_2 < \dots < \mu_p$.

**Convention:** In order to apply the sum convention to $p$-covectors as efficiently as possible, we impose the same restriction on the sum convention with respect to the indices, namely, that $$\Psi_{\mu_1, \dots, \mu_p} e^{\mu_1} \wedge \dots \wedge e^{\mu_p} := \sum_{1 \le \mu_1 <\dots < \mu_p \le n} \Psi_{\mu_1, \dots, \mu_p} e^{\mu_1} \wedge \dots \wedge e^{\mu_p}.$$Thus, we avoid using expressions with the factor $p!$.

**Def:** Since ${\textstyle \bigwedge}^{\!n}(V)$ is a one dimensional $K$-vector space, then we call the elements of ${\textstyle \bigwedge}^{\!n}(V)$ are called $n$-vectors, and another usual denomination for $n$-vectors is *psuedoscalars*. 

**Def:** Let us consider the vector space ${\textstyle \bigwedge}^{\!*}(V)$ defined by the direct sum of the vector spaces: $${\textstyle \bigwedge}^{\!*}(V) := \bigoplus_{p = 0}^\infty {\textstyle \bigwedge}^{\!p}(V).$$
**Def:** The image $\text{Alt}[\mathcal T^*(V)]$ is always the *alternating tensor graded subspace*, it is not algebra yet since we don't have a product, denoted as $A^*(V)$. 

**Obs:** We have that the kernel of $\mathcal A^{(r)}$ is precisely $I^{(r)}$, the homogeneous subset of the ideal $I$, the kernel of $\mathcal A$ is $I$. 

When $K$ has characteristic $0$, there is a canonical isomorphism $$A^*(V) \cong {\textstyle \bigwedge}^{\!*}(V).$$With these isomorphisms, we see that exterior algebra of a vector space $V$ over $K$ can be canonically identifies with the vector subspace of $T(V)$ that consists of antisymmetric tensors. With this isomorphism in mind, we don't need to care about ${\textstyle \bigwedge}_p(V)$ as a subspace of $A^*(V)$ or ${\textstyle \bigwedge}^{\!*}(V)$. 

**Cor:** $\dim {\textstyle \bigwedge}(V) =2^n$.

**Def:** We can define grade involution on ${\textstyle \bigwedge}_p(V)$: $$\#(\Psi^{[p]}) = \widehat \Psi^{[p] } := (-1)^p \Psi^{[p]}. $$For the reversion, it follows that $$\widetilde{(\alpha_1\wedge \dots \wedge \alpha_p)} := \alpha_p \wedge \dots \wedge \alpha_1, $$this implies that $\widetilde \Psi^{[p]} = (-1)^{p(p-1)/2} \Psi^{[p]}$. The conjugation of the two operations $$\overline \Psi^{[p]} := \widetilde{\widehat \Psi}^{[p]} = \widehat{\widetilde \Psi}^{[p]}.$$

If two multilinear forms $f$ and $g$ on a vector space $V$ are alternating, then we would like to have a product that is also alternating as well. This motives the definition of the *wedge product*, also called the *exterior product*, for $f\in A_k(V)$ and $g\in A_\ell(V)$: $$f \wedge g := \frac1{k! \ell !} A(f\otimes g)$$To avoid redundancies of $f\wedge g$ is to stipulate that in the sum, $\sigma(1), \dots, \sigma(k)$ be in ascending order and $\sigma(k+1), \dots, \sigma(k+\ell)$ also be in ascending order. We call a permutation $\sigma \in S_{k + \ell}$ a $(k, \ell)$*-shuffle* if: $$\sigma(1) < \cdots < \sigma(k) \quad \text{and} \quad \sigma(k+1) < \cdots < \sigma(k+\ell)$$We get that: $$f\wedge g = \sum_{\substack{(k, \ell)-\text{shuffles}\\ \sigma \in S_{k+\ell}}} \sigma (f\otimes g)$$
**Prop:** The wedge product is anti-commutative: if $f\in A_k(V)$ and $g\in A_\ell(V)$, then $$f \wedge g = (-1)^{k\ell} g\wedge f$$
**Cor:** If $f$ is a multicovector of odd degree on $V$, then $f\wedge f = 0$.

**Lemma:** Suppose $f$ is a $k$-linear function and $g$ an $\ell$-linear function on a vector space $V$. Then:
- $A(A(f) \otimes g) = k! A(f\otimes g)$
- $A(f\otimes A(g)) = \ell ! A(f\otimes g)$

**Associativity of wedge product:** Let $V$ be a real vector a space and $f, g, h$ alternating multilinear maps on $V$ of degree $k, \ell, m$, respectively. Then $$(f\wedge g) \wedge h= f \wedge (g \wedge h) $$
**Cor:** Under the hypothesis of the proposition: $$f\wedge g \wedge h = \frac1{k!\ell ! m!} A(f\otimes g \otimes h) $$
This corollary easily generalises to an arbitrary number of factors: if $f_i \in A_{d_i}(V)$, then $$f_1 \wedge \dots \wedge f_r = \frac1{(d_1)!\cdots (d_r)!} A(f_1 \otimes \cdots \otimes f_r)$$
**Cor:** For $a, b\in \Bbb R$, $f \in A_k(V)$ and $g\in A_\ell (V)$, then $af \wedge bg = (ab) f\wedge g$.

**Wedge product of $1$-covectors:** If $\alpha^1, \dots, \alpha^k$ are linear functionals on a vector space $V$ and $v_1, \dots, v_k \in V$, then $$(\alpha^1\wedge \cdots \wedge \alpha^k) (v_1, \dots, v_k) = \det[\alpha^i(v_j)]$$
**Cor:** Suppose two sets of covectors of the vector space $\beta^1, \dots, \beta^k$ and $\gamma^1, \dots, \gamma^k$ are related by $$\beta^i = a_j^i \gamma^j$$for a $k\times k$ matrix $A = [a^i_j]$. Then $$\beta^1 \wedge \cdots \wedge \beta^k = (\det A) \gamma^1 \wedge \dots \wedge \gamma^k$$
**Cor:** Let $f$ be a $k$-covector on a vector space $V$. Suppose two sets of vectors $u_1, \dots, u_k$ and $v_1, \dots, v_k$ in $V$ are related by $$u_j = \sum_{i = 1}^k a^ i_j v_i$$for a $k\times k$ matrix $A = [a^i_j]$. Then $$f(u_1, \dots, u_k) = (\det A)f(v_1,\dots, v_k)$$
**Cor:** Let $\alpha^1, \dots, \alpha^k$ be $1$-covectors on space $V$. Then, $\alpha^1 \wedge \dots \wedge \alpha^k\neq 0$ iff $\alpha^1, \dots, \alpha^k$ are linearly independent in the dual space $V'$. 

**Prop:** Let $\alpha$ be a non-zero $1$-covector and $\gamma$ a $k$-covector on a finite-dimensional vector space $V$. Then $\alpha \wedge \gamma = 0$ iff $\gamma = \alpha \wedge \beta$ for some $(k-1)$-covector $\beta$ on $V$. 

For a finite-dimensional vector space $V$, say dimension $n$, define $$A_* (V) =\bigoplus_{k = 0}^\infty A_k(V) = \bigoplus_{k = 0}^n A_k(V)$$with the wedge product of multicovectors as multiplication, $A_*(V)$ becomes [[Graded Ring|anticommutative graded algebra,]] called the *exterior algebra* or the *Grassman algebra* of multicovectors on the vector space $V$. 
# Basis for $k$-Covectors

Let $e_1, \dots, e_n$ be a basis for a real vector space $V$, let $\alpha^1, \dots, \alpha^n$ be the dual basis for $V'$. We use the [[Multi-index notation|multi-index notation]], let $I = (i_1, \dots, i_k)$ and write $e_I := (e_{i_1}, \dots,e_{i_k})$ and $\alpha^I := \alpha^{i_1}\wedge \cdots \wedge \alpha^{i_k}$. 

A $k$-linear functional $f$ on $V$ is completely determined by its values on all $k$-tuples $(e_{i_1}, \dots, e_{i_k}).$ If $f$ is alternating, then it is completely determined by its values on $(e_{i_1}, \dots, e_{i_k})$ with $1 \le i_1 < \cdots < i_k \le n$; it suffices to consider $e_I$ with $I$ in strictly ascending order.

**Lemma:** Let $e_1, \dots, e_n$ be a basis for a vector space $V$ and let $\alpha^1, \dots, \alpha^n$ be the dual basis in $V'$. If $I =(1 \le i_1 < \cdots < i_k \le n)$ and $J = (1 \le j_1 < \cdots < j_k \le n)$ are strictly ascending multi-indices of length $k$, then $$\alpha^I(e_J) = \delta^I_J = \begin{cases} 1 & I = J \\0 & I \neq J \end{cases}$$
**Prop:** The alternating $k$-linear functions $\alpha^I$, $I = (1 \le i_1 < \cdots < i_k \le n)$, form a basis for the space $A_k(V)$ of alternating $k$-linear functions on $V$.

**Cor:** If the vector space $V$ has dimension $n$, then the vector space $A_k(V)$ of $k$-covectors on $V$ has dimension $n \choose k$.

**Cor:** If $k > \dim V$, then $\dim A_k(V) = 0$. 
