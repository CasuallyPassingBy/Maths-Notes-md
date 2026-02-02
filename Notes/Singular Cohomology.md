---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Singular Homology]], [[Chain Complexes and Cochain Complexes]], [[Group Homomorphisms and Isomorphisms]]

Given a topological space $X$ and an abelian group $G$, for any integer $p \ge 0$ let $C^p(X; G)$ denote the group $\text{Hom}(C_p(X), G)$. Elements of $C^p(X; G)$ are called *$p$-dimensional singular cochains with coefficients in $G$*, or $p$-cochains for short.

The boundary operator $\partial: C_{p+1}(X) \to C_p(X)$ induces a group homomorphism $\delta: C^p(X; G) \to C^{p+1}(X; G)$, called the *coboundary operator*, characterised by $$(\delta \varphi)(c) := \varphi(\partial c).$$It is immediate that $\delta\circ \delta = 0$, so we have a cochain complex $$\cdots \stackrel{\delta}{\longrightarrow}C^{p-1}(X; G) \stackrel{\delta}{\longrightarrow} C^p(X; G) \stackrel{\delta}{\longrightarrow} C^{p+1}(X; G) \longrightarrow \cdots.$$
A $p$-cochain $\varphi$ is called a *cocycle* if $\delta \varphi = 0$, and a *coboundary* if there exists $\psi \in C^{p-1}(X; G)$ such that $\delta \psi = \varphi$. The subgroups of $C^p(X; G)$ consisting of cocycles and coboundaries are denoted by $Z^p(X; G)$ and $B^p(X; G)$, respectively.

We define the *$p$th singular cohomology of $X$ with coefficients in $G$* to be the quotient $$H^p(X; G) := Z^p(X; G)/B^p(X; G). $$
If $f:X \to Y$ is a continuous map, we obtain a map $f^\#: C^p(Y; G) \to C^p(X; G)$ by $$(f^\#\varphi)(c) := \varphi(f_\# c).  $$This map commutes with the coboundary operators because $$(f^\#\delta\varphi)(c) = \delta  \varphi(f_\# c) = \varphi(\partial f_\# c) = \varphi(f_\#\partial c) = (f^\#\varphi)(\partial c) = (\delta f^\# \varphi)(c).  $$A map that commutes with $\delta$ is called a *cochain map*. Therefore, $f^\#$ induces a cohomology homomorphism $f^*: H^p(Y, G) \to H^p(X; G)$ by $$f^*[\varphi] = [f^\#\varphi].$$
**Functorial Properties of Cohomology:** The induced cohomology homomorphism satisfies the following properties.
- If $f:X \to Y$ and $g: Y \to Z$ are continuous, then $(g\circ f)^* = f^*\circ g^*$.
- The homomorphism induced by the identity map is the identity.
Therefore, the assignments $X \mapsto H^p(X; G)$, $f\mapsto f^*$ define a contravariant functor from the category of topological spaces to the category of abelian groups.

**Topological Invariance of Cohomology:** If $f: X \to Y$ is a homeomorphism, then for every abelian group $G$ and every integer $p\ge 0$, the map $f^*: H^p(Y; G) \to H^p(X; G)$ is an isomorphism.

In full generality, the relationship between singular homology and singular cohomology with coefficients in an abelian group $G$ is described by the **Universal Coefficient Theorem**, which expresses $H^p(X;G)$ in terms of $H_p(X)$ via a short exact sequence involving both $\mathrm{Hom}$ and $\mathrm{Ext}$ groups. In particular, for arbitrary coefficient groups, singular cohomology may contain additional information arising from torsion in homology.

In these notes, we will often restrict attention to coefficients in a field $F$ (typically $\mathbb R$, $\mathbb C$, or $\mathbb Q$). 

**Lemma:** Let $F$ be a field of characteristic $0$.
- For any abelian group, the set $\mathrm{Hom}(G, F)$ of group homomorphism from $G$ to $F$ is a vector space over $F$ with scalar multiplication defined pointwise$$(a\varphi)(g) = a(\varphi(g))  $$for $a\in F$.
- If $f: G_1 \to G_2$ is a group homomorphism, then the induced homomorphism $f^*: \mathrm{Hom}(G_2, F) \to \mathrm{Hom}(G_1, F)$ is an $F$-linear map.
- If $G$ is a finitely generated abelian group, the dimension of $\mathrm{Hom}(G, F)$ is equal to the rank of $G$. 

Applying this to $C^p(X; F) = \mathrm{Hom}(C_p(X), F)$, we see that the cochain groups are $F$-vector spaces and the coboundary operators are linear maps. It follows that $Z^p(X;F)$ and $B^p(X; F)$ are vector spaces as is the quotient $H^p(X; F)$. Moreover, for any continuous map $f: X \to Y$, the induced cohomology map $f^*: H^p(Y; F) \to H^p(X; F)$ is also linear.

**Extension Lemma for Fields:** Let $F$ be a field of characteristic $0$. If $G$ is an abelian group, any group homomorphism from a subgroup of $G$ to $F$ admits an extension to all of $G$. 

**Th:** Let $F$ be a field of characteristic $0$. For any topological space $X$, the vector space $H^p(X; F)$ and $\mathrm{Hom}(H_p(X); F)$ are naturally isomorphic under the map that sends $[\varphi]\in H^p(X; F)$ to the homomorphism defined by $[c] \mapsto \varphi(c)$. Hence if $H_p(X)$ is finitely generated, then the dimension of $H^p(X; F)$ is equal to the rank of $H_p(X)$. 

**Cor:** If $X$ is a topological space such that $H_p(X)$ is finitely generated for all $p$ and zero for $p$ sufficiently large, then for any field $F$ of characteristic zero, $$\chi(X) = \sum_p (-1)^p \dim H^p(X; F). $$
**Mayer-Vietoris Theorem for Singular Cohomology:** Let $X$ be a topological space, and let $U, V$ be open subsets of whose union is $X$. Then there is an exact Mayer-Vietoris Sequence for cohomology coefficients in a field $F$ of characteristic $0$:  $$\cdots \to H^{p-1}(U \cap V; F) \to H^p(X;F) \to H^p(U;F) \oplus H^p(V; F) \to H^p(U \cap V) \to \cdots.$$