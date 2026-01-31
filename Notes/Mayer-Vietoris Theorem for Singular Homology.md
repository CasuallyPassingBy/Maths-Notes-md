---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Singular Homology]], [[The Seifert-Van Kampen Theorem]], [[The Zigzag Lemma]], [[Simplicial Complexes]], [[Abstract Simplicial Complexes]]

**Def:** Suppose $\mathcal U$ is an open cover of $X$. A singular chain $c$ is said to be *$\mathcal U$-small* if every singular simplex that appears in $c$ has image lying entirely in one of the open subsets in $\cal U$. Let $C^{\cal U}_p (X)$ denote the subgroup of $C_p(X)$ consisting of $\cal U$-small chains, and let $H^{\cal U}_p(X)$ denote the homology of the complex $C^{\cal U}_\bullet (X)$. 

**Def:** If $\alpha = A(v_0,\dots, v_p)$ is an affine singular $p$-simplex in some convex set $K \subseteq \Bbb R^m$ and $w$ is any point in $K$, we define an affine singular $(p+1)$-simplex $w*\alpha$ called the *cone on $\alpha$ from $w$* by $$w* \alpha := w* A(v_0,\dots, v_p) = A(w, v_0,\dots, v_p). $$In other words, $w*\alpha: \Delta_{p+1}\to K$ is the unique affine simplex that sends $e_0$ to $w$ and whose $0$th dace map is equal $\alpha$. We extend this operator to affine chains by linearity  $$w* \left(\sum_i n_i\alpha_i\right) := \sum_i n_i (w *\alpha_i).$$It is not defined for arbitrary singular chains.

**Lemma:** If $c$ is an affine chain. then $$\partial(w*c) + w*\partial c= c. $$
**Def:** For any $k$-simplex $\sigma = [v_0,\dots, v_k]\in \Bbb R^n$, we define the *barycentre of $\sigma$* to be the points $b_\sigma\in \text{Int }\sigma$ whose barycentric coordinates are all equal:  $$b_\sigma := \sum_{i = 0}^k \frac1{k+1} v_i. $$
Noe we define an operator $s$ taking affine $p$-chains to affine $p$-chains, called the *singular subdivision operator*. For $p = 0$, simply set $s = \text{id}$. For $p>0$, assuming that $s$ has been defined for chains of dimensions less than $p$, for any affine $p$-simplex $\alpha: \Delta_p \to \Bbb R^n$ we set $$s\alpha := \alpha(b_p)* s (\partial \alpha),   $$where $b_p$ is the barycentre of $\Delta_p$, and extend linearly to affine chains. 

**Lemma:** Suppose $\alpha: \Delta_p \to \Bbb R^n$ is an affine simplex that is a homeomorphism onto a $p$-simplex $\sigma\subseteq\Bbb R^n$. Let $\beta: \Delta_p \to\Bbb R^n$ be any one of the affine singular $p$-simplices that appear in the chains $s\alpha$. 
- $\beta$ is an affine homeomorphism onto a $p$-simplex of the form $[b_p, \dots, b_0]$, where each $b_i$ is the barycentre of an $i$-dimensional face of $\sigma$.
- The diameter of any such simplex $[b_p, \dots, b_0]$ is at most $p/(p+1)$ times the diameter of $\sigma$. 

Now we need to extend the singular subdivision operator to arbitrary, not necessarily affine, singular chains. For a singular $p$-simples $\sigma$ in any space $X$, note that $\sigma = \sigma_\# i_p$, where $i_p : \Delta_p\to \Delta_p$ is the the identity map considered as an affine singular $p$-simplex in $\Delta_p$, and $\sigma_\#: C_p(\Delta_p) \to C_p(X)$ is the chain map obtained from the continuous map $\sigma: \Delta_p \to X$. we define $$s\sigma := \sigma_\# (si_p),$$and extend by linearity to all of $C_p(X)$. We can iterate $s$ to obtain operators $s^2 := s\circ s$ and more generally $s^{k+1} := s^k \circ s$. 

**Lemma:** The singular subdivision operators $s:C_p(X) \to C_p(X)$ have the following properties.
- $s \circ f_\# = f_\#\circ s$ for any continuous map $f$.
- $\partial \circ s = s\circ \partial$.
- Given an open cover $\cal U$ of $X$ and any $c\in C_p(X)$, there exists $m$ such that $s^m c\in C^\mathcal U_p(X)$. 

**Prop:** Suppose $\cal U$ is any open cover of $X$. The inclusion map $C^\mathcal U_\bullet (X)\to C_\bullet (X)$ induces a homology isomorphism $H^\mathcal U_p(X) \cong H_p(X)$ for all $p$. 

We are given a space $X$ and two open subsets $U, V\subseteq X$ whose union is $X$. There are four inclusion maps 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}
& U\arrow[dr, "k"] & \\
U \cap V\arrow[ur, "i"]\arrow[dr, "j"] && X \\
&V\arrow[ur,"\ell"']&
\end{tikzcd}
\end{document}
```

**Mayer-Vietoris Theorem:** Let  be a topological space, and let $U, V$ be open subsets of  whose union is $X$. Then for each $p$ there is a homomorphism $\partial_*: H_p(X) \to H_{o-1}(U \cap V)$ such that the following sequence is exact:  $$\cdots \stackrel{\partial_*}{\longrightarrow}H_p(U \cap V) \stackrel{i_* \oplus j_*}{\longrightarrow} H_p(U) \oplus H_p(V)\stackrel{k_*- l_*}{\longrightarrow}H_p(X)\stackrel{\partial_*}{\longrightarrow} H_{p-1}(U\cap V)\stackrel{i_* \oplus j_*}{\longrightarrow}\cdots$$
