---
tags:
  - GroupTheory
  - ModuleTheory
---
Subjects: [[Group Theory]], [[Module Theory]]
Links: [[Free Groups]], [[Generation of Modules, Direct Sum, and Free Modules]], [[Module and Algebra]], [[Finite Abelian Groups]]

Let $G$ be an abelian group. 

**Def:** A *linear combination of elements of $G$* is a finite sum of the form $\sum_{i = 1}^k n_i g_i$, where $g_1,\dots, g_k\in G$ and $n_1,\dots, n_k\in\Bbb Z$.

Given a nonempty set $S$. A *formal linear combination of elements of $S$* is a map from $S$ to $\Bbb Z$ that has finite support. Under the operation of pointwise addition the set of all such functions is an abelian group denoted by $\Bbb Z\langle S\rangle$ called the *free abelian group on $S$*. Let us note that we know that the category $\sf Ab$ and $\Bbb Z\sf-Mod$ are isomorphic, and that the notation is no coincidence either. The free abelian group on $S$ is the free $\Bbb Z$-module, and thus it inherits a lot of the nice properties of free modules.

**Characteristic Property:** Given any abelian group $H$ and any map $\varphi: S \to H$, there exists a unique homomorphism $\Phi: \Bbb Z\langle S\rangle \to H$ extending $\varphi$.

**Prop:** The free abelian group $\Bbb Z\langle\sigma_1, \dots,\sigma_n\rangle$ on a finite set is isomorphic to $\Bbb Z^n$. 

**Def:** Let $G$ be an abelian group. A nonempty subset $S\subseteq G$ is said to be *linearly independent* if the only linear combination of elements of $S$ that equals zero is the one for which all the coefficients are zero. A *basis for $G$* is a linearly independent subset that generates $G$.

The set of elements $e_i$ is a basis for $\Bbb Z^n$ which we calle the *standard basis*.

If $G$ is an abelian group and there is a subset $S\subseteq G$ such that the homomorphism $\Bbb Z\langle S\rangle \to G$ induces by the inclusion $S \hookrightarrow G$ is an isomorphism, then $G$ is also said to be a *free abelian group*. 

Note that $G$ is a free abelian group iff $G$ is a free $\Bbb Z$-module.

**Lemma:** If an abelian group $G$ has a finite basis, then every finite basis has the same number of elements. 

**Def:** If $G$ is a free abelian group with finite basis, we say that $G$ has *finite rank*, and we define the *rank of $G$* to be the number of element in any basis. If $G$ has no finite basis, we say it has *infinite rank*.

**Prop:** Suppose $G$ is a free abelian group of finite rank. Every subgroup of $G$ is a free abelian group of rank less or equal to that of $G$.

**Cor:** Every subgroup of a finitely generated abelian group is finitely generated.

**Def:** We say that an element $g$ of an abelian group $G$ is a *torsion element* if $ng = 0$ for some nonzero $n \in\Bbb Z$. If $ng = n'g' = 0$, then $nn'(g+g') = 0$, os the set of all torsion elements is a subgroup $G_\text{tor}$ of $G$, called the *torsion subgroup*. We say that $G$ is *torsion-free* if the only torsion element is $0$. We see that $G/G_\text{tor}$ is torsion-free.

**Prop:** Any abelian group that is finitely generated and torsion-free is free abelian of finite rank. 

**Prop:** Suppose $G$ and $H$ are abelian groups and $f: G \to H$ is a homomorphism. Then $G$ is finitely generated iff both $\text{Im}f$ and $\ker f$ are finitely generated, in which case $\text{rank}(G) = \text{rank}(\text{Im} f) + \text{rank}(\ker f)$. 