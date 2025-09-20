---
tags:
  - GeometricAlgebra
---
Subjects: [[Geometric Algebra]]
Links: [[Tensor Algebra]], [[Quadratic Forms]], [[Exterior Algebra]], [[Bilinear Forms]]

**Def:** Let $K$ be a field with , $V$ be a vector space over $K$, and $Q$ be a quadratic form. We consider the *Clifford algebra of $V$ over $Q$* is defined as $$\text{Cl}(V, Q) := T(V)/I_Q,$$where $T(V)$ is tensor algebra, and $I_Q := \langle v\otimes v - Q(v)1 \mid v\in V\rangle$.

Let $(V, Q)$ be a quadratic space over the field $K$. Remember, if $K$ has characteristic not equal to $2,$ is equivalent to a diagonal form $$Q(x) = \sum_{i = 1}^n a_i x_i^2 \qquad a_i \in K.$$from [[Quadratic Forms#^c01a68|this]]. This implies that we only need to care about the diagonal case, since we can just change the basis to one that is diagonal. Since $(V, Q)$ is a quadratic space, if the $K$ has characteristic different from $2$, then  we can writhe the *fundamental Clifford identity*: for $v, w\in V$
$$uv+ vu = 2\langle u, v\rangle,$$

where$$\langle u, v\rangle := \frac12(Q(u+v)- Q(u)- Q(v))$$is $\langle \cdot, \cdot\rangle$ is the symmetric bilinear form associated with $Q$. 

**Universal Property:** A Clifford algebra $\text{Cl}(V, Q)$ is a pair $(B, i)$ where $B$ is a unital associative algebra over $K$ and $i$ is a linear map $i:V \to B$ that satisfies $i(v)^2 = Q(v) 1_B$ for all $v\in V$, defined by the following universal property: given any unital associative algebra $A$ over $K$ and any linear map $j: V \to A$ such that $j(v)^2 = Q(v) 1_A$ for all $v\in V$, there is a unique morphism $f:B \to A$ such that the following diagram commutes
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
V \arrow[dr, "j"] \arrow[r, hook, "i"] & C\ell(V, Q) \arrow[d, dashed, "f"]\\
& A
\end{tikzcd}
\end{document}
```

The quadratic form $Q$ may be replaced by a bilinear form $\langle \cdot, \cdot \rangle$ that has the property $\langle v, v\rangle = Q(v)$, for $v\in V$, in which case an equivalent requirement on $j$ is $j(v) j(v) = \langle v, v\rangle 1_A$ for all $v\in V$. When the characteristic of the field is not $2$, this may be replaced by what is then an equivalent requirement $$j(v) j(w) + j(w)j(v) = (\langle v, w\rangle+ \langle w, v\rangle)1_A \qquad \forall v, w\in V,$$where the bilinear form may be additionally restricted to being symmetric without loss of generality.

From the universal property we get two things. Firstly, since $\text{Cl}(V, Q)$ contains $V$ and satisfies the above universal property, so that $\text{Cl}(V, Q)$ is unique up to a unique isomorphism. We also see that the map $i$ is injective, so we treat $V$ as a subspace of $\text{Cl}(V, Q)$. 

Secondly, we can consider $\text{Cl}$ as a functor from the category of quadratic spaces with linear maps that preserve the quadratic form to the category of associative algebras. The universal property guarantees that linear maps between quadratic spaces extend uniquely to algebra homomorphisms between associated Clifford algebras.

# Basis and Dimension

Let $(V, Q)$ be a quadratic space.

**Def:** Let $v, w\in V$. We say that $v, w$ are *orthongonal* if $\langle v, w\rangle = 0$, where $\langle\cdot, \cdot, \rangle$ is the associated symmetric bilinear form of $Q$.

Since $(V, Q)$ is a quadratic space, in a characteristic not equal to $2$ there exist orthogonal bases. An orthogonal basis is one that for a symmetric bilinear form $\langle e_i, e_j \rangle = 0$ for $i \neq j$. 

We see that the fundamental Clifford identity implies that for an orthogonal basis $$e_i e_j =-e_j e_i \qquad \forall i \neq j,$$and $$e_i^2 = Q(e_i).$$

This makes working with orthogonal bases quite simple, since given a product $e_{i_1}e_{i_2}\cdots e_{i_k}$ of *distinct* orthogonal basis vectors of $V$, one can put them into a standard order while including an overall sign determined by the sign of the permutation.

We can see that $\dim \text{Cl}(V, Q) = 2 ^n$, where $\dim V = n$.

