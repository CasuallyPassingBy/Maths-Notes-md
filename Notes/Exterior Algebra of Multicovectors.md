---
tags:
  - DifferentialGeometry
  - LinearAlgebra
  - CliffordAlgebra
---
Subjects: [[Differential Geometry]], [[Linear Algebra]], [[Clifford Algebra (Subject)]]
Links: [[Dual Vector Spaces]], [[Exterior Algebra of Vector Spaces]], [[Multilinear Transformations]], [[Tensor Product of Modules]],  [[Graded Ring]], [[Tensor Product of Linear Functions]], [[Symmetric Group]]

Let $K$ be characteristic $0$ field. We are going to drop, the fact that the codomain is $K$ for the rest of the note, since this notation is a bit cumbersome. 

**Def:** A covariant $k$-tensor on $V$ is said to be *alternating* if its value changes sign whenever two arguments are interchanged, or equivalently if any permutation of the arguments causes its value by the sign of the permutation. Alternating covariant $k$-tensors are also called *exterior forms, multicovectors* or *$k$-covectors*. The space of all $k$-covectors on $V$ is denoted by $\bigwedge^k(V^*)$. All $0$-tensors and $1$-tensors are alternating. 

**Lemma:** Let $\alpha$ be a covariant $k$-tensor on a finite-dimensional vector space $V$. The following are equivalent.
- $\alpha$ is alternating.
- $\alpha(v_1,\dots, v_k) = 0$ whenever the $k$-tuple $(v_1,\dots, v_k)$ is linearly independent.
- $\alpha$ gives the value zero whenever two of its arguments are equal: $$\alpha(v_1,\dots, w,\dots, w, \dots v_k) = 0.$$

**Def:** We define a projection $\text{Alt}: T^k(V^*) \to \bigwedge^k(V^*)$, called *alternation* as follows:  $$\text{Alt } \alpha =  \frac1{k!} \sum_{\sigma \in S_k} \text{sgn }\sigma (\sigma \alpha),$$where $S_k$ is the symmetric group on $k$ elements. More explicitly, this means $$(\text{Alt } \alpha)(v_1,\dots, v_k) =  \frac1{k!} \sum_{\sigma \in S_k} \text{sgn }\sigma  \alpha(v_{\sigma(1)},\dots, v_{\sigma(k)}). $$
**Properties of Alternation:** Let $\alpha$ be a covariant tensor on a finite-dimension $K$-vector space.
- $\text{Alt }\alpha$ is alternating.
- $\text{Alt }\alpha = \alpha$ iff $\alpha$ is alternating. 

## Elementary Alternating Tensors

**Def:** Given a positive integer $k$, an ordered $k$-tuple $I=(i_1,\dots, i_k)$ of positive integers is called a *multi-index of length $k$*. If $I$ is such a multi-index and $\sigma\in S_k$, we write $I_\sigma$ for the following multi-index: $$I_\sigma := (i_{\sigma(1)},\dots, i_{\sigma(k)}) $$Note that $I_{\sigma\tau} := (I_\sigma)_\tau$ for $\sigma,\tau\in S_k$. 

**Def:** Let $V$ be a finite-dimensional $K$-vector space, and suppose $(\varepsilon^1,\dots, \varepsilon^n)$ is any basis for $V^*$. We know define a collection of $k$-covectors on $V$ that generalise the determinant function on $\Bbb R^n$. For each multi-index $I = (i_1,\dots, i_k)$ of length $k$ such that $1\le i_1 \dots, i_k \le n$, define a covariant $k$-tensor $\varepsilon^I = \varepsilon^{i_1,\dots, i_k}$ by $$\varepsilon^I(v_1,\dots, v_k) = \det \begin{pmatrix}
\varepsilon^{i_1}(v_1)& \cdots & \varepsilon^{i_1}(v_k) \\
\vdots & \ddots & \vdots \\ \varepsilon^{i_k}(v_1) & \cdots & \varepsilon^{i_k}(v_k)
\end{pmatrix} = \det \begin{pmatrix}
v_1^{i_1}& \cdots & v_k^{i_1} \\
\vdots & \ddots & \vdots \\ v_1^{i_k} & \cdots & v_k^{i_k}
\end{pmatrix}.$$In other words, if $\mathbb v$ is denotes the $n\times k$ matrix whose columns are the components of the vectors $v_1,\dots, v_k$ with respect to the basis $(E_i)$ dual to $(\varepsilon^i)$, then $\varepsilon^I(v_1,\dots, v_k)$ is the determinant of the $k\times k$ submatrix consisting of the rows $i_1,\dots, i_k$ of $\Bbb v$ . We call $\varepsilon^I$ an *elementary alternating tensor* or *elementary $k$-covector*.

In order to streamline the computations with the elementary $k$-covectors, we can extend the Kronecker delta notation in the following way. If $I$ and $J$ are multi-indices of length $k$, we define$$\delta^I_J := \det \begin{pmatrix}
\delta_{j_1}^{i_1}& \cdots & \delta_{j_k}^{i_1} \\
\vdots & \ddots & \vdots \\ \delta_{j_1}^{i_k} & \cdots & \delta_{j_k}^{i_k}
\end{pmatrix} .$$
**Obs:** We see that $$\delta^I_J = \begin{cases}\text{sgn }\sigma & \text{if neither } I \text{ nor } J \text{ has repeated index and } J = I_\sigma \text{ for some }\sigma\in S_k, \\
0 & \text{if }I \text{ or }J \text{ has a repeated index or } J \text{ is not a permutation of }I.
\end{cases} $$
**Properties of Elementary $k$-covectors:** Let $(E_i)$ be a basis for $V$ and let $(\varepsilon^i)$ be the dual basis for $V^*$, and let $I$ be a multi-index.
- If $I$ has a repeated index, then $\varepsilon^I = 0$.
- If $J = I_\sigma$, for some $\sigma\in S_k$, then $\varepsilon^J = (\text{sgn }\sigma) \varepsilon^J.$
- The result of evaluating $\varepsilon^I$ on a sequence of basis vectors is $$\varepsilon^I(E_{j_1},\dots, E_{j_k}) = \delta^I_J. $$
**Def:** A multi-index $I = (i_1,\dots, i_k)$ is said to be *increasing* if $i_1<\dots <i_k$. 

**A Basis for $\bigwedge^k(V^*)$:** Let $V$ be a $n$-dimensional $K$-vector space. If $(\varepsilon^i)$ is any basis for $V^*$, then for each positive $k \le n$, the collection of $k$-covectors $$\mathcal E:= \{\varepsilon^I\mid I \text{ is an increasing multi-index of length }k\} $$is a basis for $\bigwedge^k(V^*)$. Therefore $$\dim {\displaystyle \bigwedge}^{\!k}(V^*) = {n\choose k}. $$If $k > n$, then $\dim \bigwedge^k(V^*) = 0$. 

**Prop:** Suppose $V$ is an $n$-dimensional $K$-vector space and $\omega\in \bigwedge^k(V^*)$. If $T: V \to V$ is any linear map and $v_1,\dots, v_n$ are arbitrary vectors in $V$, then $$\omega(Tv_1,\dots, Tv_n) = (\det T) \omega(v_1,\dots, v_n). $$
## The Wedge Product

**Determinant Convention:** Given $\omega\in \bigwedge^k(V^*)$ and $\eta \in \bigwedge^l(V^*)$, we define their *wedge product* or *exterior product* to be the following $(k+k)$-covector: $$\omega \wedge \eta := \frac{(k+l)!}{k!l!}\text{Alt }(\omega\otimes \eta).$$
**Alt Convention:**  Given $\omega\in \bigwedge^k(V^*)$ and $\eta \in \bigwedge^l(V^*)$, we define their *wedge product* or *exterior product* to be the following $(k+k)$-covector: $$\omega \wedge \eta := \text{Alt }(\omega\otimes \eta).$$

**Lemma:** Let $V$ be a $n$-dimensional $K$-vector space and let $(\varepsilon^1,\dots, \varepsilon^n)$ be a basis for $V^*$. For any multi-indices $I = (i_1,\dots, i_k)$ and $J = (j_1,\dots, j_l)$, $$\varepsilon^I \wedge \varepsilon^J = \varepsilon^{IJ}, $$where $IJ := (i_1,\dots, i_k,j_1,\dots, j_l)$ is obtained by concatenating $I$ and $J$. (under the determinant convention). $$\varepsilon^I \wedge \varepsilon^J =\frac{k!l!}{(k+l)!} \varepsilon^{IJ},   $$under the Alt convention. 

**Properties of the Wedge Product:** Suppose $\omega$, $\omega'$, $\eta$, $\eta'$ and $\xi$ are multicovectors on a finite-dimensional $K$-vector space $V$.
- *Bilinearity:* For $a, b\in \Bbb R$,  $$\begin{align*}
  (a\omega+ b\omega')\wedge \eta &= a(\omega\wedge \eta) + b(\omega' \wedge \eta), \\ \eta\wedge (a\omega + b\omega') &= a(\eta \wedge \omega)+ b(\eta\wedge \omega').
  \end{align*} $$
- *Associativity:*  $$\omega \wedge (\eta \wedge \xi) = (\omega \wedge \eta ) \wedge\xi. $$
- Anticommutativity: $$\omega \wedge\eta = (-1)^{kl}\eta\wedge\omega. $$
- If $(\varepsilon^i)$ is any basis for $V^*$ and $I =(i_1,\dots, i_k)$ is any multi-index, then $$\varepsilon^{i_1}\wedge\dots \wedge\varepsilon^{i_k} = \varepsilon^I. $$
- For any covectors $\omega^1,\dots, \omega^k$ and vectors $v_1,\dots, v_k$, $$\omega^1\wedge\dots \wedge \omega^k(v_1,\dots, v_k) = \det(\omega^j(v_i)), $$under the determinant convention. We also have $$\omega^1\wedge\dots \wedge \omega^k(v_1,\dots, v_k) =\frac{1}{k!} \det(\omega^j(v_i)). $$
**Def:** A $k$-covector is *decomposable* if it can be expressed in the form $\eta = \omega^1\wedge\dots\wedge\omega^k$, where $\omega^1,\dots, \omega^k$ are covectors. 

**Def:** For any $n$-dimensional $K$-vector space $V$, define a vector space $\bigwedge (V^*)$ by  $$\bigwedge(V^*) := \bigoplus_{k = 0}^n {\textstyle \bigwedge}^{\!k} (V).$$We see that $\bigwedge (V)$ is a $K$-vector space with dimension $2^n$. 

**Obs:** We see that $(\bigwedge (V),\wedge)$ is an anticommutative graded algebra, and it is called the *exterior algebra* or *Grassmann algebra of $V$*. 

## Interior Multiplication

**Def:** Let $V$ be a finite-dimensional $K$-vector space. For each $v\in V$, we define a linear map $i_v: \bigwedge^{k}(V^*) \to \bigwedge^{k-1}(V^*)$, called *interior multiplication by $v$*, as follows: $$i_v\omega(w_1,\dots, w_{k-1}) := \omega(v, \omega_1,\dots, w_{k-1}). $$In other words, $i_v\omega$ is obtained from $\omega$ by inserting $v$ into the first slot. By convention, we interpret $i_v \omega$ to be zero when $\omega$ is a $0$-covector. Another common notation is $$v\;\lrcorner \;\omega := i_v \omega .$$This is often read as '$v$ into $w$'.

**Lemma:** Let $V$ be a finite-dimensional $K$-vector space and $v\in V$. 
- $i_v \circ i_v = 0$.
- If $\omega\in \bigwedge^k(V^*)$ and $\eta\in \bigwedge^l(V^*)$, $$i_v(\omega\wedge\eta) = (i_v \omega)\wedge \eta + (-1)^k\omega\wedge(i_v \eta). $$

when the wedge product is defined using the Alt convention, interior multiplication of a vector with a $k$-form has to be defined with an extra $k$: $$\bar i_v \omega(w_1,\dots, w_{k-1}) = k\omega(v, w_1,\dots, w_{k-1}). $$This definition ensures that the interior multiplication $\bar i_v$ still satisfies $$\bar i_v(\omega\wedge\eta) = (\bar i_v \omega)\wedge \eta + (-1)^k\omega\wedge(\bar i_v \eta). $$

# Duality

Let $V$ be a space with inner product.

For each natural $k$, we can define an interior product on ${\textstyle \bigwedge}^{\!k} (V)$. Let $\omega^1\wedge\dots \omega^k, \eta^1\wedge\dots\eta^k \in {\textstyle \bigwedge}^{\!k} (V)$, then $$\langle \omega^1\wedge\dots \wedge\omega^k,\eta^1\wedge\dots\wedge\eta^k\rangle := \det(\langle(\omega^i)^\sharp, (\eta^j)^\sharp\rangle). $$So basically, we are calculating pulling the covectors in the original vector space using the [[Correlations, Musical Isomorphisms|musical isomorphisms]], and then calculating the inner product there.

