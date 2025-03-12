---
tags:
  - "#CategoryTheory"
---
Subjects: [[Category Theory]]

**Def**: A *category* $\mathcal C$ consists of:
- a class $\text{ob}(\mathcal C)$ of objects
- a class $\text{mor}(\mathcal C)$ of morphisms or arrows
- Two class functions
	- A *domain* or a *source* class function $\text{dom}: \text{mor}(\mathcal C) \to \text{ob}(\mathcal C)$
	-  A *codomain* or a *target* class function $\text{dom}: \text{mor}(\mathcal C) \to \text{ob}(\mathcal C)$
	Which assign to each morphism $f \in \text{mor}(\mathcal C)$ a unique pair of objects $A, B\in \text{ob}(\mathcal C)$ such that $\text{dom}(f) A$ and $\text{cod}(f) = B$. We write the $f:A \to B$ to indicate that $f$ has domain $A$ and codomain $B$.
- A class function called *composition*, denoted as $\circ$, and assigns to each pair of morphisms $f, g\in \text{mor}(\mathcal C)$ a composite morphism $g\circ g$ whenever $\text{dom}(g) = \text{cod}(f)$. Composition, must satisfy the following proporties:
	- *Identity*: For each object $A\in \text{ob}(\mathcal C)$, there exists an identity morphism $\text{id}_A : A \to A$ such that for every morphism $f: A \to B$ and $g: C\to A$,$$f \circ \text{id}_A = f, \qquad \text{id}_A \circ g = g$$
	- *Associativity:* For any morphisms $f:A \to B$, $g: B \to C$ and $h: C \to D$, we have that: $$h\circ (g\circ f) = (h\circ g) \circ f$$
There are several examples for categories:
- $\mathsf{Set}$, the class of [[Set Theory|sets]] and functions.
- $\mathsf{Poset}$, the class of [[Orderings|partially ordered]] and order homomorphisms
- $\mathsf{Top}$, the class of all [[topological spaces]] and continuous functions.
- $\mathsf{TM}$, the class of [[topological manifolds]] and continuous maps.
- $\mathsf{SM}$, the class of [[Smooth or Differentiable Manifolds|smooth manifolds]] and smooth maps between them.
- $\mathsf{Met}$, the class of [[metric spaces]] and short maps. 
- $\mathsf{VB}$, the class of [[Vector Bundles on Smooth Manifolds]] and smooth bundle maps.}
- $\mathsf{Grp}$, the class of [[Group Theory|groups]] and group homomorphisms.
- $\mathsf{Ab}$, the class of [[Groups#^58586b|abelian groups]] and group homomorphism.
- $\mathsf{Vect}_K$, the class of all [[vector spaces]] over a field $K$ and $K$-linear maps.
- Given a ring $R$, $R\mathsf{-Mod}$, the category of all left $R$-modules and $R$-module homomorphism. 
- $\mathsf{Ring}$, the class of [[rings]] and ring homomorphisms
- $\mathsf{Meas}$, the class of [[Measure Spaces and Measurable Spaces]] and measurable functions. 
- We call a pair $(M, q)$, where $M$ is a manifold and $q$ a point in $M$, a *pointed manifold*. Given two such pairs $(N, p)$ and $(M, p)$, let $f: (N, p) \to (M, q)$ is a smooth map from $N$ to $M$ and $f(p) = q$. 
- $\mathsf{LIE}$, the class of [[Lie groups]] and Lie group homomorphisms.
- $\mathsf{lie}$, the class of [[Lie Algebra|Lie algebras]] and Lie algebra homomorphisms.

**Def:** Two objects $A$ and $B$ in a category are said to be *isomorphic* if there are morphism $f: A \to B$ and $g: B \to A$ such that: $$g \circ f = \text{id}_A, \qquad f \circ g = \text{id}_B$$in this case both $f$ and $g$ are called *isomorphisms*. The usual notation for an isomorphism is $\simeq$. Thus $A\simeq B$ can different things depending on the category. 


Def: A *covariant functor* $\mathcal F$ from one category to another category $\mathcal D$ is a map $\mathcal {F: C \to D}$ that assigns:
- To each $A \in \text{ob}(\mathcal C)$, an object $\mathcal F(A) \in \text{ob}(\mathcal D)$
- To each morphism $f: A \to B$ in $\mathcal C$ and a morphism $\mathcal F(f): \mathcal F(A) \to \mathcal F(B)$ in $\mathcal D$
This assignment must satisfy the following conditions:
- *Preservation of Composition*: For any pair of composable morphisms $f: A\to B$ and $g:B \to C$ in $\mathcal C$, we have $$F(g\circ f) = F(g) \circ F(f) $$
- *Preservation of identity morphisms:* For every object $A\in\mathcal C$, we have $$F(\text{id}_A) = \text{id}_{F(A)}$$
An example of a functor is from the category of pointed manifolds to the category of real vector spaces, is the tangent space construction. To each pointed manifold $(N, p)$ it transforms into $T_p N$, for each smooth map $f: (N, p) \to (M, f(p))$ we associate the differential map $df_p: T_p N \to T_{f(p)} M$. 

**Prop:** Let $\mathcal {F: C \to D}$ be a functor from a category $\mathcal C$ to a category $\mathcal D$ If $f:A \to B$ is an isomorphism in $\mathcal C$, then $\mathcal F(f): \mathcal F(A) \to \mathcal F(B)$ is an isomorphism in $\mathcal D$. 

**Def:** A *contravariant functor* $\mathcal F$ from the category $\mathcal C$ to another category $\mathcal D$ is a map $\mathcal {F: C \to D}$ that assigns:
- To each $A \in \text{obj}(\mathcal C)$ , an object $\mathcal F(A) \in \text{obj}(\mathcal D)$
- To each morphism $f: A \to B$ in $\mathcal C$ and a morphism $\mathcal F(f): \mathcal F(A) \to \mathcal F(B)$ in $\mathcal D$
This assignment must satisfy the following conditions:
- *Preservation of Composition*: For any pair of composable morphisms $f: A\to B$ and $g:B \to C$ in $\mathcal C$, we have $$F(g\circ f) = F(f) \circ F(g) $$
- *Preservation of identity morphisms:* For every object $A\in\mathcal C$, we have $$\mathcal F(\text{id}_A) = \text{id}_{\mathcal F(A)}$$
