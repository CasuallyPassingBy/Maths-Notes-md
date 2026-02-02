---
tags:
  - GroupTheory
  - HomologicalAlgebra
---
Subjects: [[Group Theory]], [[Homological Algebra]]
Links: [[Group Homomorphisms and Isomorphisms]]

**Def:** A sequence of abelian groups and homomorphisms $$ \cdots \stackrel{}{\longrightarrow} G_{p+1} \stackrel{\alpha_{p+1}}{\longrightarrow}  G_p \stackrel{\alpha_p}{\longrightarrow}  G_{p-1}\stackrel{}{\longrightarrow} \cdots $$is said to be *exact* if $\text{Im }\alpha_{p+1} = \ker \alpha_p$ for each $p$. A $5$-term exact sequence fo the form$$  0\to A \stackrel{\alpha}{\to} B \stackrel{\beta}{\to} C \to 0 $$is called a *short exact sequence*. Because the image of the zero homomorphism is $\{0\}$, exactness at $A$ means that $\alpha$ is injective, and similarly exactness at $C$ means that $\beta$ is surjective. Exactness at $B$ means that $\ker \beta = \text{Im } \alpha$, and the first isomorphisms theorem then tell us that $C \cong B/\text{Im }\alpha$. A short exact sequence is thus a graphic summary of the first isomorphism theorem. 
