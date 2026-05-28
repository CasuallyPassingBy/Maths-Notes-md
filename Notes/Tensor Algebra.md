---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]], [[Ring Theory]], [[Module Theory]]
Links: [[Tensor Product of Modules]], [[Tensor Product of Modules]], [[Graded Ring]], [[Modules and Algebras]], [[Bases and Dimension]]

Our goal is to create an algebra where the tensor product. For the rest of this note, $R$ is a commutative ring with a unit, and we assume left and right actions of $R$ on each $R$-module are the same.

**Def:** Let $M$ be an $R$-module, then by recursion, we define the *tensor powers of $M$*
- $M^{\otimes 0} = T^0(M) :=R$
- $M^{\otimes 1} = T^1(M) := M$
- $M^{\otimes (k+1)} = T^{k+1}(M) = M^{\otimes k} \otimes_R M = T^k (M) \otimes_R M$. 
The elements fo $T^k(M)$ are called $k$-*tensors*. Then: $$T(M) := \bigoplus_{k = 0}^\infty M^{\otimes k}.$$
**Prop:** If $M$ is any $R$-module over the commutative ring $R$ then $T(M)$ is an $R$-algebra containing $M$ with multiplication defined by mapping $$(m_1 \otimes \dots \otimes m_i) (m_1' \otimes \dots \otimes m_j') = m_1 \otimes \dots \otimes m_i\otimes m'_1 \otimes \dots \otimes m_j'$$and extended to sums via the distributive laws. With respect to multiplications $M^{\otimes i} M^{\otimes j} \subseteq M^{\otimes (i+j)}$ 

**Def:** The ring $T(M)$ is called the *tensor algebra of $M$.*

**Universal property of the tensor algebra:** If $A$ is any $R$-algebra and $\varphi: M \to A$ is an $R$-module homomorphism, then there is a unique $R$-algebra homomorphism $\Phi: T(M) \to A$ such that $\Phi|_M = \varphi$. or such that the diagram commutes:

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]     
M \arrow[dr, "\phi"] \arrow[r, hook, "\iota"] & T(M) \arrow[d, dashed, "\Phi"]\\
& A
\end{tikzcd}
\end{document}
```

**Prop:** Let $V$ be a finite dimensional vector space over the field $F$ with basis $\beta = \{v_1, \dots, v_n\}$. Then the $k$-tensors $$v_{i_1} \otimes v_{i_2} \otimes  \dots \otimes v_{i_k} \qquad \text{with } v_{i_j} \in \beta$$are a vector space basis for $V^{\otimes k}$ over $F$. In particular, $\dim_F (V^{\otimes k}) = n^k$. 
