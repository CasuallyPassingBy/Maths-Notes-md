---
tags:
  - "#CategoryTheory"
---
Subjects: [[Category Theory]]

**Def**: A *category* $\mathsf C$ consists of:
- a class $\text{ob}(\mathsf C)$ of objects
- a class $\text{mor}(\mathsf C)$ of morphisms or arrows
- Two class functions
	- A *domain* or a *source* class function $\text{dom}: \text{mor}(\mathsf C) \to \text{ob}(\mathsf C)$
	-  A *codomain* or a *target* class function $\text{dom}: \text{mor}(\mathsf C) \to \text{ob}(\mathsf C)$
	Which assign to each morphism $f \in \text{mor}(\mathsf C)$ a unique pair of objects $A, B\in \text{ob}(\mathsf C)$ such that $\text{dom}(f)= A$ and $\text{cod}(f) = B$. We write the $f:A \to B$ to indicate that $f$ has domain $A$ and codomain $B$. We use the notation $\text{Hom}_{\mathsf C}(A,B)$ to denote the class of al morphisms from $A$ to $B$.
- A class function called *composition*, denoted as $\circ$, and assigns to each pair of morphisms $f, g\in \text{mor}(\mathsf C)$ a composite morphism $g\circ g$ whenever $\text{dom}(g) = \text{cod}(f)$. Composition, must satisfy the following properties:
	- *Identity*: For each object $A\in \text{ob}(\mathsf C)$, there exists an identity morphism $\text{id}_A : A \to A$ such that for every morphism $f: A \to B$ and $g: C\to A$,$$f \circ \text{id}_A = f, \qquad \text{id}_A \circ g = g$$
	- *Associativity:* For any morphisms $f:A \to B$, $g: B \to C$ and $h: C \to D$, we have that: $$h\circ (g\circ f) = (h\circ g) \circ f$$
We say that a category is *small* if $\text{ob}(\mathsf C)$ is a set. Additionally, we say that $\mathsf C$ is *locally small* if for any two objects $A$ and $B$ the class $\text{Hom}_{\mathsf C}(A, B)$ is a set. 

There are several examples for categories:
- $\mathsf{Set}$, the class of [[Set Theory|sets]] and functions.
- $\mathsf{Poset}$, the class of [[Orderings|partially ordered]] and monotone-increasing functions.
- $\mathsf{Top}$, the class of all [[topological spaces]] and continuous functions.
- $\mathsf{Top}_*$, the class of all pointed topological spaces and pointed continuous functions. 
- $\mathsf{HTop}$, the class of topological spaces and [[Homotopy|homotopy classes]].
- $\mathsf{HTop}_*$, the class of pointed topological spaces and pointed continuous maps modulo [[Fundamental Group of a Topological Space#^0f8fb7|homotopy relative to the base point]]. 
- $\mathsf{Man}^0$, the class of [[topological manifolds]] and continuous maps.
- $\mathsf{Man}^0_*$, the class of pointed topological manifolds and pointed continuous functions
- $\mathsf{Man}^\infty$, the class of [[Smooth Manifolds|smooth manifolds]] and smooth maps between them.
- $\mathsf{Man}^\infty_*$, the class of pointed smooth manifolds and pointed smooth functions
- $\mathsf{Met}$, the class of [[metric spaces]] and short maps. 
- $\mathsf{VB}$, the class of [[Vector Bundles on Smooth Manifolds]] and smooth bundle maps.}
- $\mathsf{Grp}$, the class of [[Group Theory|groups]] and group homomorphisms.
- $\mathsf{Ab}$, the class of [[Groups#^58586b|abelian groups]] and group homomorphism.
- $\mathsf{Vect}_K$, the class of all [[vector spaces]] over a field $K$ and $K$-linear maps.
- Given a ring $R$, $R\mathsf{-Mod}$, the category of all left $R$-modules and $R$-module homomorphism. 
- $\mathsf{Ring}$, the class of [[Rings and Fields]] and ring homomorphisms.
- $\mathsf{Field}$, the class of [[Rings and Fields|Fields]] and field homomorphisms.
- $\mathsf{Meas}$, the class of [[Measure Spaces and Measurable Spaces|measure spaces]] and measurable functions. 
- $\mathsf{LIE}$, the class of [[Lie groups]] and Lie group homomorphisms.
- $\mathsf{lie}$, the class of [[Lie Algebra|Lie algebras]] and Lie algebra homomorphisms.
- $\mathsf{CW}$, the class of [[Cell Complexes and CW Complexes|CW complexes]] and continuous maps.
- $\mathsf{Smp}$, the class of [[simplicial complexes]] and simplicial maps.

**Def:** Two objects $A$ and $B$ in a category are said to be *isomorphic* if there are morphism $f: A \to B$ and $g: B \to A$ such that: $$g \circ f = \text{id}_A, \qquad f \circ g = \text{id}_B$$in this case both $f$ and $g$ are called *isomorphisms*. The usual notation for an isomorphism is $\simeq$. Thus $A\simeq B$ can different things depending on the category. 

**Def:** A *subcategory of $\mathsf C$* is a category $\sf D$ whose objects are objects of $\sf C$ and whose morphism are just some of those in $\sf C$, with the composition law and identities inherited from $\sf C$. A *full subcategory* is one in which $\text{Hom}_{\sf D}(A, B) = \text{Hom}_{\sf C}(A, B)$ are objects in $\sf C$. 

Def: A *covariant functor* $\mathcal F$ from one category to another category $\mathsf D$ is a map $\mathcal {F}:\mathsf C \to \mathsf D$ that assigns: ^66a925
- To each $A \in \text{ob}(\mathsf C)$, an object $\mathcal F(A) \in \text{ob}(\mathsf D)$
- To each morphism $f: A \to B$ in $\mathsf C$ and a morphism $\mathcal F(f): \mathcal F(A) \to \mathcal F(B)$ in $\mathsf D$
This assignment must satisfy the following conditions:
- *Preservation of Composition*: For any pair of composable morphisms $f: A\to B$ and $g:B \to C$ in $\mathsf C$, we have $$F(g\circ f) = F(g) \circ F(f) $$
- *Preservation of identity morphisms:* For every object $A\in\mathsf C$, we have $$F(\text{id}_A) = \text{id}_{F(A)}$$
An example of a functor is from the category of pointed manifolds to the category of real vector spaces, is the tangent space construction. To each pointed manifold $(N, p)$ it transforms into $T_p N$, for each smooth map $f: (N, p) \to (M, f(p))$ we associate the differential map $df_p: T_p N \to T_{f(p)} M$. 

**Prop:** Let $\mathcal {F: C \to D}$ be a functor from a category $\mathsf C$ to a category $\mathsf D$ If $f:A \to B$ is an isomorphism in $\mathsf C$, then $\mathcal F(f): \mathcal F(A) \to \mathcal F(B)$ is an isomorphism in $\mathsf D$. 

**Example:** The *[[Fundamental Group of a Topological Space|fundamental group]] functor* $\pi_1: \mathsf{Top_*} \to \mathsf{Grp}$ assigns to each pointed topological space $(X, p)$ its fundamental group based at $p$, and to each pointed continuous map its induced homomorphism; and $\pi_1$ is a covariant functor.

**Def:** A *contravariant functor* $\mathcal F$ from the category $\mathsf C$ to another category $\mathsf D$ is a map $\mathcal {F: C \to D}$ that assigns:
- To each $A \in \text{obj}(\mathsf C)$ , an object $\mathcal F(A) \in \text{obj}(\mathsf D)$
- To each morphism $f: A \to B$ in $\mathsf C$ and a morphism $\mathcal F(f): \mathcal F(A) \to \mathcal F(B)$ in $\mathsf D$
This assignment must satisfy the following conditions:
- *Preservation of Composition*: For any pair of composable morphisms $f: A\to B$ and $g:B \to C$ in $\mathsf C$, we have $$F(g\circ f) = F(f) \circ F(g) $$
- *Preservation of identity morphisms:* For every object $A\in\mathsf C$, we have $$\mathcal F(\text{id}_A) = \text{id}_{\mathcal F(A)}$$
