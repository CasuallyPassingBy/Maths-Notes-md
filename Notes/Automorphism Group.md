---
tags:
  - GroupTheory
  - CategoryTheory
---
Subjects: [[Group Theory]], [[Category Theory]]
Links: [[Group Homomorphisms and Isomorphisms]], [[Groups]], [[Categories and Functors]]

**Def:** Let $X$ be an object in the category $\mathsf C$. A morphism $f: X \to X$ is called an *endomorphism*. Additionally, If we $f:X \to X$ is an isomorphism and an endomorphism, then $f$ is called an *automorphism*. The class of automorphism of $X$ is denoted as $\text{Aut}_\mathsf C (X).$ 

**Prop:**  $(\text{Aut}_\mathsf C(X),\circ, \text{id}_X)$  is a group for any category $\mathsf C$ and any object $X$. 

**Examples:**
- If $G$ is a group, then $\text{Aut}_{\mathsf{Grp}}(G)$ is just called the automorphism group. 
- If $X$ is a topological space, then $\text{Aut}_{\mathsf{Top}}(X)$, then we call it the homeomorphism group $\text{Homeo}(X)$.
- If $X$ is a smooth manifold, then $\text{Aut}_{\mathsf{Man}^\infty}(X)$, then we call it the diffeomorphism group and $\text{Diffeo}(X)$.
- If $X$ is a set, then $\text{Aut}_\mathsf{Set}(X)$ is the set of all bijective functions from $X$ to $X$, and it is denoted $\text{Sym}(X)$ or $S_X$. It is usually called the symmetric group of $X$.
- If $V$ is a $F$-vector space, then $\text{Aut}_{\mathsf{Vect}_F}(V)$ is called the linear the general linear group and it is denoted as $\text{GL}(V)$.

**Prop:** Let $G$ a group and for any element $h\in G$ fixed, then we define the function $c_h: G \to G$ defined by $c_h(g) = hgh^{-1}$. $c_h \in \text{Aut}(G)$. The automorphisms of the form $c_h$, defined by conjugation by $h$ are called the internal automorphisms of $G$. 

**Prop:** Let $G$ be a group, and we define the group homomorphism $c : G \to \text{Aut}(G)$, for $h, g\in G$, then $c_h(g) = hgh^{-1}$

