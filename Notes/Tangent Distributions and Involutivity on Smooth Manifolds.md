---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Integral Curves, Flows and Flowouts on Smooth Manifolds]], [[Integral Curves, Flows and Flowouts on Smooth Manifolds]], [[The Tangent Bundle]], [[Vector Subbundles on Smooth Manifolds]], [[Differential Forms on Smooth Manifolds]], [[Covector Fields on Smooth Manifolds]], [[Lie Derivative]], [[Immersed Smooth Submanifolds]]

**Def:** Let $M$ be a smooth manifold. A *distribution on $M$ of rank $k$* is a rank-$k$ subbundle of $TM$. It is called a *smooth distribution* if it is a smooth subbundle. Distributions are also sometimes called *tangent distributions*, especially if there is any opportunity for confusion with the use of the term 'distribution' for generalised functions in analysis, *$k$-plane fields*, or *tangent subbundles.*

Often a rank-$k$ distribution is described by specifying for each $p\in M$ a linear subspace $D_p \le T_p M$ of dimension $k$, and letting $D = \bigcup_{p\in M} D_p$. It then  follows from the local frame criterion for subbundles that $D$ is a smooth distribution iff each point of $M$ has a neighbourhood $U$ on which there are smooth vector fields $X_1,\dots, X_k: U \to TM$ such that $X_1|_q,\dots, X_k|_q$ form a basis for $D_q$ at each $q\in U$. This case, we say that $D$ is the distribution *(locally) spanned by the vector fields $X_1,\dots, X_k$.*

## Integral Manifolds and Involutivity

**Def:** Suppose $D\subseteq TM$ is a smooth distribution. A nonempty immersed submanifold $N \subseteq M$ si called an *integral manifold of $D$* if $T_p N = D_p$ at each point $p\in N$. 

**Def:** We say that $D$ is *involutive* if given any pair of smooth local sections of $D$, their Lie bracket is also a local section of $D$.

**Prop:** Let $D\subseteq TM$ be a smooth distribution, and let $\Gamma(D) \subseteq {\frak X}(M)$ denote the space of smooth global sections of $D$. Then $D$ is involutive iff $\Gamma(D)$ is a Lie subalgebra of ${\frak X}(M)$. 

**Def:** A smooth distribution $D$ on $M$ is said to be *integrable* if each point of $M$ is contained in an integral manifold of $D$. 

**Prop:** Every integrable distribution is involutive.

**Local Frame Criterion for Involutivity:** Let $D\subseteq TM$ be a distribution. If in a neighbourhood of every point of $M$ there exists a smooth local frame $(V_1,\dots, V_k)$ for $D$ such that $[V_i, V_j]$ is a section of $D$ for each $i, j =1,\dots, k$, then $D$ is involutive. 

### Relationship with Differential Forms

**$1$-Form Criterion for Smooth Distribution:** Suppose $M$ is a smooth $n$-manifold and $D\subseteq TM$ is a distribution of rank $k$. Then $D$ is a smooth iff each point $p\in M$ has a neighbourhood $U$ on which there are smooth $1$-forms $\omega^1,\dots, \omega^{n-k}$ such that for each $q\in U$, $$D_q = \bigcap_{i = 1}^{n-k} \ker(\omega^i|_q). $$
**Def:** If $D$ is a rank-$k$ distribution on a smooth $n$-manifold $M$, any $n-k$ linearly independent $1$-forms $\omega^1,\dots, \omega^{n-k}$ defined on an open subset $U\subseteq M$ and satisfying for each $q\in U$ are called *local defining forms for $D$*. More generally, if $0\le p \le n$, we say that a $p$-form $\omega\in \Omega^p(M)$ *annihilates $D$* if $\omega(X_1,\dots, X_p) = 0$ whenever $X_1,\dots, X_p$ are local sections of $D$.

**Lemma:** Suppose $M$ is a smooth $n$-manifold and $D$ is a smooth rank-$k$ distribution on $M$. Let $\omega^1,\dots, \omega^{n-k}$ be smooth local defining forms for $D$ over an open subset $U\subseteq M$. A smooth $p$-form $\eta$ on $U$ annihilates $D$ iff it can be expressed in the form $$\eta = \sum_{i = 1}^{n-k}\omega^i\wedge\beta^i  $$for some smooth $(p-1)$-forms $\beta^1,\dots, \beta^{n-k}$ on $U$.

**$1$-Form Criterion for Involutivity:** Suppose $D\subseteq TM$ is a smooth distribution. The following statements are equivalent.
- $D$ is involutive.
- If $\eta$ is any smooth $1$-form that annihilates $D$ on an open subset $U\subseteq M$, then $d\eta$ annihilates $D$ on $U$. 

**Local Coframe Criterion for Involuvilty:** Let $D$ be a smooth distribution of rank $k$ on a smooth $n$-manifold $M$, and let $\omega^1,\dots, \omega^{n-k}$ be smooth defining for $D$ on an open subset $U\subseteq M$. The following are equivalent:
- $D$ is involutive on $U$.
- $d\omega^1,\dots,d\omega^{n-k}$ annihilate $D$.
- There exist smooth $1$-forms $\{\alpha^i_j \mid i, j = 1,\dots, n-k\}$ such that $$d\omega^i = \sum_{j = 1}^{n-k} \omega^j\wedge \alpha^i_j, \qquad \text{for each }i = 1,\dots, n-k.$$

**Def:** An *[[Ring Ideals and Quotient Rings|ideal]] in $\Omega^*(M)$* is a linear subspace ${\scr I} \subseteq \Omega^*(M)$ is a linear subspace ${\scr I} \subseteq \Omega^*(M)$ that is closed under wedge products with arbitrary elements of $\Omega^*(M)$: that is $\omega \in {\scr I}$ implies that $\eta\wedge \omega\in {\scr I}$ for every $\eta\in \Omega^*(M)$. 

**Def:** Suppose $D$ is a smooth distribution on a smooth $n$-manifolds $M$. Let ${\scr I}^p(D) \subseteq\Omega^p(M)$ denote the space of smooth $p$-forms that annihilate $D$, and let $$\mathscr I(D) := \bigoplus_{p = 0}^n \mathscr I^p(D).$$
**Obs:** For any smooth distribution $D\subseteq TM$, then $\mathscr I(D)$ is an ideal in $\Omega^*(M)$.

**Def:** Any ideal of the form $\mathscr I(D)$ for some smooth distribution $D$ is sometimes called a *Pfaffian system*. 

**Def:** An ideal $\mathscr I\subseteq \Omega^*(M)$ is said to be a *differential ideal* if $d[\mathscr I] \subseteq I$, that is, if $\omega\in \mathscr I$, implies that $d\omega \in \scr I$. 

**Differential Ideal Criterion for Involutivity:** Let $M$ be a smooth manifold. A smooth distribution $D\subseteq TM$ is involutive off $\mathscr I(D)$ is a differential ideal in $\Omega^*(M)$. 

# The Frobenius Theorem

**Def:** Given a rank-$k$ distribution $D\subseteq TM$, let us say that a smooth coordinate chart $(U, \varphi)$ on $M$ is *flat fo $D$* if $\varphi[U]$ is a cube in $\Bbb R^n$, and at points of $U$, $D$ is spanned by the first $k$ coordinate vector fields $\partial/\partial x^1,\dots, \partial/\partial x^k$. In any such chart, each slice $x^{k+1} = c^{k+1},\dots, x^n = c^n$ for constants $c^{k+1},\dots, c^n$ is integral manifold of $D$. This is the nicest possible local situation of integral manifolds. We say that a distribution $D\subseteq TM$ is *completely integrable* if there exists a flat chart for $D$ in a neighbourhood of each point of $M$.

**Obs:** Every completely integrable distribution is integrable and therefore involutive. 

**Frobenius Theorem:** Every involutive distribution is completely integrable,

Embedded in the proof of the Frobenius theorem is a technique for finding integral manifolds. The idea is to use the coordinate projection to find commuting vector fields spanning the same distribution, and then use the technique in to find [[Lie Derivative#^afb34f|Canonical Form for Commuting Vector Field]]. 

**Example:** Let $D\subseteq T\Bbb R^3$ be the distribution spanned by the vector fields$$\begin{align*}X &= x\frac{\partial}{\partial x} + \frac{\partial}{\partial y}+ x(y+1) \frac{\partial}{\partial z} \\
Y&= \frac{\partial}{\partial x}+ y \frac{\partial}{\partial z}.\end{align*} $$We see that $[X, Y] = -Y$. So $D$ is involutive. Let us try to find a flat chart in a neighbourhood of the origin. Since $D$ is complementary to the span of $\partial/\partial z$, the coordinate projection $\pi: \Bbb R^3 \to\Bbb R^2$ given by $\pi(x, y, z) := (x,y)$ induces an isomorphism $D_(x, y,z) \to T_{(x, y)}\Bbb R^2$ for each $(x, y,z)\in\Bbb R^3$. If we can find smooth local sections $V$, $W$ of $D$ that are $\pi$-related to $\partial/\partial x$ and $\partial/\partial y$, respectively, they will be commuting vector fields spanning $D$. It is easy to check that $V, W$ have this property iff they take their values in $D$ and are of the form$$\begin{align*} V&=  \frac{\partial}{\partial x}+  u(x, y, z) \frac{\partial}{\partial z}, \\
W &= \frac{\partial}{\partial y}+ v(x, y, z) \frac{\partial}{\partial z}\end{align*}, $$for some smooth functions $u, v$. We can do a little bit of linear algebra remembering they must span $D$, and get that $$\begin{align*}V &= Y = \frac{\partial}{\partial x}+ y \frac{\partial}{\partial z}, \\ W &= X-xY = \frac{\partial}{\partial y}+ x\frac{\partial}{\partial z},\end{align*}  $$do the trick. We can calculate their flows. The flow of $V$ is given by $$\alpha_t(x, y, z) = (x+t, y+ z+ty), $$and the flow of $W$ is given by  $$\beta_t(x, y, z) = (x, y+t, z+tx).$$Composing their flows we get that  $$\Phi(u, v, w) := \alpha_u \circ \beta_v(0,0,w) = (0, v,w) = (u, v, w+uv).$$The flat coordinates we seek are given by the inverse map $(x, y, z) = \Phi(u, v, w)$, to yield that  $$(u, v, w) = \Phi^{-1}(x, y, z) = (x, y, z-xy). $$We see that the integral manifolds of $D$ are the level sets of $w(x, y,z) = z-xy$. 

**Cor:** Suppose $M$ is a smooth manifold, $D$ is an involutive rank-$k$ distribution on $M$, and $S\subseteq M$ is a codimension-$k$ embedded submanifold. If $p\in S$ is a point such that $T_pS$ is complementary to $D_p$, then there is a flat chart $(U, (s^i))$ for $D$ centred at $p$ in which $S\cap U$ is the slice $s^1= \dots = s^k = 0$. 

**Local Structure of Integral Manifolds:** Let $D$ be an involutive distribution of rank $k$ on a smooth manifold $M$, and let $(U, (x^i))$ be a flat chart for $D$. If $H$ is any integral manifold of $D$, then $H \cap U$ is a union of countably many disjoint open subsets of parallel $k$-dimensional slices of $U$, each of which is open in $H$ and embedded in $M$. 

**Th:** Every integral manifold of an involutive distribution is [[Smooth Maps on and Between Submanifolds#^089be9|weakly embedded]].