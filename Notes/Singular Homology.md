---
tags:
---
Subjects: [[Algebraic Topology]]
Links: [[Simplicial Complexes]], [[Affine Maps]], [[Free Abelian Groups]], [[Exact Sequences and Chain Complexes]], [[Homotopy Equivalence]]

**Def:** For any integer $p \ge 0$, let $\Delta_p \subseteq \Bbb R^p$ denote the *standard $p$-simplex* $[e_0, e_1,\dots, e_p]$, where $e_0 =0$ and, for $1\le i \le p$. $e_i$ is the $i$the element of the standard basis. If $X$ is a topological space, a *singular $p$-simplex in $X$* is a continuous map $\sigma: \Delta_p \to X$. 

**Obs:** A singular $0$-simplex is just a map from the one-point space $\Delta_0$ into $X$, which we may identify with a point in $X$; and a singular $1$-simples is a map from $\Delta_1 =[0, 1]\subseteq \Bbb R$ into $X$, which is just a path in $X$. 

**Def:** Let $C_p(X)$ be the free abelian group on the set of all singular $p$-simplices in $X$. An element of $C_p(X)$, which can be written as a formal linear combination of singular simplices with integer coefficients , is called a *singular $p$-chain in $X$*, and the group $C_p(X)$ is called the *singular chain group in dimension $p$*.

**Def:** There are some special simplices in Euclidean spaces. Let $K\subseteq \Bbb R^n$ be a convex subset. For any $p+1$ points $v_0, \dots, v_p\in K$, let $A(v_0, \dots, v_p): \Delta_p\to \Bbb R^n$ denote the affine map that $e_i \mapsto v_i$ for $i = 0,\dots, p$. By convexity the image lies in $K$, so this is a singular $p$-simplex in $K$, called an *affine singular simplex*. A singular chain in which every singular simplex appears is affine is called an *affine chain*. 

For each $i = 0,\dots, p$, let $F_{i, p}: \Delta_{p-1}\to \Delta_p$ be the affine singular simplex $$F_{i, p} := A(e_0, \dots \widehat{e_i}, \dots, e_p),$$where the hat indicates that $e_i$ is to be omitted. We see that $e_j \mapsto e_j$ for $0\le j < i$ and $e_j\mapsto e_{j+1}$ for $i \le j < p$. Therefore $F_{i, p}$ maps $\Delta_{p-1}$ homeomorphically onto the boundary face of $\Delta_p$ opposite the vertex $e_i$. We call $F_{i, p}$ the *$i$th face map in dimension $p$.*

We can also use another notation, we can designate $\sigma$ by its vertices $$\sigma= [p_0,\dots, p_n] := [\sigma(e_0), \dots, \sigma(e_n)],$$and let us note that $$\sigma \circ F_{i, n} =[p_0,, \dots, \widehat{p_{i}}, \dots, p_n] = \sigma|_{[p_0,, \dots, \widehat{p_{i}}, \dots, p_n]}$$

**Def:** For any singular simplex $\sigma: \Delta_n \to X$, define a $(n-1)$-chain $\partial \sigma$ called the *boundary of $\sigma$* by $$\partial \sigma = \partial[p_0, \dots, p_n] := \sum_{i = 0}^n (-1)^i \sigma \circ F_{i, n} = \sum_{i = 0}[p_0,\dots, \widehat{p_i},\dots, p_n].$$By the characteristic property of free abelian groups, this extends uniquely to a homeomorphism $\partial: C_n(X) \to C_{n-1}(X)$, called the *singular boundary operator.* We sometimes indicate which chain group the boundary operator is acting on by a subscript, as in $\partial_n: C_n(X) \to C_{n-1}(X)$. The boundary of any $0$-chain is defined to be $0$. 

The kernel of the boundary operator is $Z_n(X) := \ker \partial_n$, and is called the *group of singular $n$-cycles*. the Image of the boundary operator is $B_n(X) = \text{im}\partial_{n+1}$ and is called the *group of singular $n$-boundaries.*

**Lemma:** If $c$ is a singular chain, then $\partial (\partial c) = 0$. 

**Obs:** We see that $B_p(X) \le Z_p(X)$. 

**Def:** The boundary operator together with the $C_n(X)$, for a a chain complex of abelian groups called the *singular complex*. It is often denoted as $(C_\bullet(X), \partial_\bullet)$ or more simply $C_\bullet(X)$. 

**Def:** The *$p$th singular homology group of $X$* is defined to be the quotient group $$H_p(X) := Z_p(X)/B_p(X) = \ker\partial_p/\text{Im}\partial_{p+1}.$$
The equivalence class of a $p$-cycle $c$ in $H_p(X)$ is denoted by $[c]$, and is called its *homology class*. If two $p$-cycles determine the same homology class, they are said to be *homologous*. 

**Def:** Given a continuous map $f:X \to Y$, let $f_\#: C_p(X) \to C_p(Y)$ be homoemorphism defined by setting $f_\sharp\sigma := f\circ \sigma$ for each singular $p$-simplex $\sigma$. 

**Obs:** A key fact is that $f_\sharp$ commutes with the boundary operators $$f_\sharp(\partial \sigma) = \partial(f_\sharp \sigma).$$This means that $f_\sharp$ is actually a chain map, $f_\sharp: C_\bullet(X) \to C_\bullet(Y)$. Thus that $f_\sharp$ maps $Z_p(X)$ to $Z_p(Y)$ and $B_p(X)$ to $B_p(Y)$, and therefore passes to the quotient to define a homomorphism $f_*: H_p(X) \to H_p(Y)$, called the *homomorphism induced by $f$.*

**Functorial Properties of Homology:** Let $X$, $Y$, and $Z$ be topological spaces.
- The homomorphism $(\text{Id}_X)_*: H_p(X) \to H_p(X)$ induced by the identity map of $X$ is the identity of $H_p(X)$. 
- If $f:X \to Y$ and $g:Y\to Z$ are continuous maps, then $$(g\circ f)_* = g_* \circ f_*: H_p(X) \to H_p(Z).$$Thus the $p$the singular homology group defines a covariant functor from the category of topological spaces to the category of abelian groups. 

**Topological Invariance of Singular Homology:** If $f:X \to Y$ is a homeomorphism, then $f_*: H_p(X) \to H_p(Y)$ is an isomorphism.

**Homology of a Retract:** Suppose $X$ is a topological space and $A\subseteq X$ is retract of $X$. Then for each $p$, the homology homomorphism $H_p(A)\to H_p(X)$ induced by inclusion is injective.

## Elementary Computations

**Prop:** Let $X$ be a space, let $\{X_\alpha \mid \alpha <\kappa\}$ be the set of path components of $X$, and let $\iota_\alpha: X_\alpha \hookrightarrow X$ be inclusion. Then for each $p\ge 0$ the map $$\bigoplus_{\alpha <\kappa} H_p(X_\alpha) \to H_p(X)$$ whose restriction to $H_p(X_\alpha)$ is $(\iota_\alpha)_*: H_p(X_\alpha) \to H_p(X)$, is an isomorphism. 

**Zero-Dimensional Homology:** For any topological space $X$, $H_0$ is a free abelian group with basis consisting of an arbitrary point in each path component. 

**Homology of a Discrete Space:** If $X$ is a discrete space, then $H_0(X)$ is a free abelian group with one generator for each point of $X$, and $H_p(X) = 0$ for $p >0$. 

## Homotopy Invariance

**Th:** If $f_0, f_1: X \to Y$ are homotopic maps, then for each $p \ge 0$ the induced homomorphism $(f_0)_*, (f_1)_*: H_p(X) \to H_p(Y)$ are equal. 

**Homotopy Invariance of Singular Homology:** Suppose $f: X \to Y$ is a homotopy equivalence. Then for each $p \ge 0$, $f_*:H_p(X) \to H_p(Y)$ is an isomorphism.

**Cor:** Suppose $X$ is a contractible topological space. Then $H_p(X) = 0$ for all $p > 0$. 