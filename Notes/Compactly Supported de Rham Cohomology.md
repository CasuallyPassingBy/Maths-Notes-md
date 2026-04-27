---
tags:
  - DifferentialGeometry
  - Topology/AlgebraicTopology
---
Subjects: [[Differential Geometry]], [[Algebraic Topology]]
Links: [[The de Rham Cohomology Groups]], [[Integration of Differential Forms on Smooth Manifolds]], [[Mayer-Vietoris Theorem for de Rham Cohomology]], [[The de Rham Theorem and Stokes's Theorem on Chains]], [[Space of Compactly Supported Functions]]

**Poincaré Lemma with Compact Support:** Let $1 \le p \le n$, and suppose $\omega$ is a compactly supported closed $p$-form on $\Bbb R^n$. If $p =  n$, suppose in addition that $$\int_{\Bbb R^n}\omega = 0.$$Then there exists a compactly supported smooth $(p-1)$-form $\eta$ on $\Bbb R^n$ such that $d\eta = \omega$.

**Def:** Let $M$ be a smooth manifold with or without boundary and let $\Omega_c^p(M)$ denote the vector space of compactly supported smooth $p$-forms on $M$. The *$p$th compactly supported de Rham cohomology group of $M$* is the quotient space $$H_c^p(M) := \frac{\ker (d : \Omega^p_c(M) \to \Omega^{p+1}_c(M))}{\text{Im}(d: \Omega^{p-1}_c (M) \to \Omega^p_c(M))}.  $$Of course, when $M$ is compact, this just reduces to ordinary de Rham cohomology. 

**Compactly Supported Cohomology of $\Bbb R^n$:** For $n \ge 1$, the compactly supported de Rham cohomology groups of $\Bbb R^n$ are $$H_c^p(\Bbb R^n) \cong \begin{dcases}
0 & 0\le p < n, \\
\Bbb R  & p = n.
\end{dcases}$$
We see that a smooth map doesn't pull back compactly supported forms to compactly supported smooth ones. so it doesn't induce a map on compactly supported cohomology. A [[Proper Maps|proper map]] does pull back compactly supported forms to compactly supported ones, so for a proper smooth map $F: M \to N$ there is an induced cohomology map $F^*: H_c^p(N) \to H_c^p(M)$ for each $p$. 

**Top Cohomology, Orientable Compact Support Case:** If $M$ is a connected oriented smooth $n$-manifold, then the integration map $I: H_c^n(M) \to \Bbb R$ is an isomorphism, so $H_c^n(M)$ is $1$-dimensional.

**Top Cohomology, Orientable Compact Case:** If $M$ is a compact connected orientable smooth $n$-manifold, then $H_\text{dR}^n(M)$ is $1$-dimensional, and is spanned by the cohomology class of any smooth orientation form.

**Top Cohomology, Orientable Noncompact Case:** If $M$ is a noncompact connected orientable smooth $n$-manifold, then $H_\text{dR}^n(M)=0$. 

**Lemma:** Suppose $M$ is a connected nonorientable smooth manifold and $\widehat\pi: \widehat  M \to M$ is its orientation covering. For each $p$, the induced cohomology maps $\widehat\pi^*: H_\text{dR}^p(M) \to H_\text{dR}^p(\widehat M),$ and  $\widehat\pi^*: H_c^p(M)\to H_c^p(\widehat M)$ are injective.

**Top Cohomology, Nonorientable Case:** If $M$ is a connected nonorientable smooth $n$-manifold, then $H_c^n (M) = 0$ and $H_\text{dR}^n(M)=0$. 

**Prop:** Let $M$ be a connected smooth manifold of dimension $n \ge 3$. For any $x\in M$ and $0\le p\le n-2$, the map $H_\text{dR}^p(M) \to H_\text{dR}^p(M\setminus\{x\})$ induced by the inclusion $M \setminus\{x\}\hookrightarrow M$ is an isomorphism. If in addition, $M$ is compact and orientable then it is true when $p = n-1$. 

**Cor:** Let $M_1, M_2$ be connected smooth manifolds of dimension $n\ge 3$, and let $M_1\#M_2$ denote their smooth connected sum. Then $H_\text{dR}^p(M_1\#M_2) \cong H_\text{dR}^p(M_1) \oplus H_\text{dR}^p(M_2)$ for $0 < p <n-1$. If in addition, $M_1$ and $M_2$ are compact and orientable, then it is also true for $p = n-1$. 

**Prop:** Suppose $M$ is a compact, connected, orientable, smooth $n$-manifolds.
- There is a one-to-one correspondence between orientations of $M$ and orientations of the vector space $H_\text{dR}^n(M)$, under which the cohomology class of a smooth orientation form is an oriented basis for $H_\text{dR}^n(M)$.
- Suppose $M$ and $N$ are smooth $n$-manifolds with given orientations. A diffeomorphism $F: M \to N$ is orientation preserving iff $F^*: H_\text{dR}^n(N) \to H_\text{dR}^n(M)$.

**Lemma:** Given an open subset $U\subseteq M$, let $\iota: U \hookrightarrow M$ denote the inclusion map, and define a linear map $\iota_\sharp: \Omega_c^p(U) \to \Omega^p_c(M)$ by extending each compactly supported from to be zero on $M \setminus U$. Then we get that $d\circ\iota_\sharp = \iota_\sharp\circ d$, and so $\iota_\sharp$ induces a linear map on compactly supported cohomology, denoted by $\iota_*: H^p_c(U) \to H_c^p(M)$. 

**Mayer-Vietoris with Compact Supports:** Suppose $M$ is a smooth manifold and $U, V\subseteq M$ are open subsets whose union is $M$. For each nonnegative integer $p$, there is a linear map $\delta_*: H_c^p(M) \to H_c^{p+1}(U \cap V)$ such that the following sequence is exact $$\cdots 
\stackrel{\delta_*}{\longrightarrow} H_c^p(U \cap V) \stackrel{i_* \oplus(-j_*)}{\longrightarrow}H_c^p(U) \oplus H_c^p(V)\stackrel{k_*+ l_*}{\longrightarrow} H_c^p(M) \stackrel{\delta_*}{\longrightarrow} H_c^p(U \cap V) \stackrel{i_* \oplus(-j_*)}{\longrightarrow}\cdots,$$where $i, j, k, l$ are the inclusion maps
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}
& U\arrow[dr, "k"] & \\
U \cap V\arrow[ur, "i"]\arrow[dr, "j"] && M \\
&V\arrow[ur,"\ell"']&
\end{tikzcd}
\end{document}
```
**Cor:** Let $H_c^p(M)^*$ denote the algebraic dual space of $H_c^p(M)$. The following sequence is also exact:$$\cdots \stackrel{(\delta_*)^*}{\longrightarrow} H_c^p(M)^* \stackrel{(k_*)\oplus (l_*)^* }{\longrightarrow} H_c^p(U) \oplus H_c^p(V)^* \stackrel{(i_*)^*-(j_*)^*}{\longrightarrow} H_p^c(U \cap V)^* \stackrel{(\delta_*)^*}{\longrightarrow} H^{p-1}_c(M)^*\stackrel{(k_*)\oplus (l_*)^* }{\longrightarrow}\cdots. $$
**Def:** Let $M$ be an oriented smooth $n$-manifold. We define a map $\text{PD}:\Omega^p(M) \to \Omega_c^{n-p}(\Omega)^*$ by $$\text{PD}(\omega)(\eta) := \int_M \omega \wedge \eta.  $$
**The Poincaré Duality Theorem:** $\text{PD}$ descends to an isomorphism $\text{PD}: H_\text{dR}^p(M) \to H_c^{n-p}(M)^*.$ 

**Prop:** Let $M$ be a compact smooth $n$-manifold.
- All of the de Rham groups of $M$ are finite-dimensional. 
- If $M$ is orientable, then $\dim H_\text{dR}^p(M) = \dim H_\text{dR}^{n-p}(M)$ for all $p$. 

**Cor:** If $M$ is a compact, orientable, and odd dimensional smooth manifold, then $\chi(M) = 0.$ 