---
tags:
  - GroupTheory
  - HomologicalAlgebra
---
Subjects: [[Group Theory]], [[Homological Algebra]]
Links: [[Group Homomorphisms and Isomorphisms]]

**Def:** A sequence of abelian groups and homomorphisms $$ \cdots \stackrel{}{\longrightarrow} G_{p+1} \stackrel{\alpha_{p+1}}{\longrightarrow}  G_p \stackrel{\alpha_p}{\longrightarrow}  G_{p-1}\stackrel{}{\longrightarrow} \cdots $$is said to be *exact* if $\text{Im }\alpha_{p+1} = \ker \alpha_p$ for each $p$. A $5$-term exact sequence fo the form$$  0\to A \stackrel{\alpha}{\to} B \stackrel{\beta}{\to} C \to 0 $$is called a *short exact sequence*. Because the image of the zero homomorphism is $\{0\}$, exactness at $A$ means that $\alpha$ is injective, and similarly exactness at $C$ means that $\beta$ is surjective. Exactness at $B$ means that $\ker \beta = \text{Im } \alpha$, and the first isomorphisms theorem then tell us that $C \cong B/\text{Im }\alpha$. A short exact sequence is thus a graphic summary of the first isomorphism theorem. 

**The Five Lemma:** Let $A$ be a commutative ring with unity. Let
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
A_1\arrow[r, "\alpha_1"]\arrow[d, "f_1"] & A_2\arrow[d, "f_2"]\arrow[r, "\alpha_2"] & A_3\arrow[d, "f_3"]\arrow[r, "\alpha_3"] & A_4\arrow[d, "f_4"]\arrow[r, "\alpha_4"] & A_5\arrow[d, "f_5"] \\
B_1\arrow[r, "\beta_1"] & B_2\arrow[r, "\beta_2"] & B_3\arrow[r, "\beta_3"] & B_4\arrow[r, "\beta_4"] & B_5 
\end{tikzcd}
\end{document}
```
be a commutative diagram of $A$-modules. Suppose that the rows are exact.
- If $f_2$ and $f_4$ are surjective and $f_5$ is injective, then $f_3$ is surjective. 
- If $f_2$ and $f_4$ are injective and $f_1$ is surjective then $f_3$ is injective. 