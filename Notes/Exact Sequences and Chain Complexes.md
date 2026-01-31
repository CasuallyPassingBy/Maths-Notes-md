---
tags:
  - HomologicalAlgebra
---
Subjects: [[Homological Algebra]]
Links: [[Group Homomorphisms and Isomorphisms]]

**Def:** A sequence of abelian groups and homomorphisms $$ \cdots \stackrel{}{\longrightarrow} G_{p+1} \stackrel{\alpha_{p+1}}{\longrightarrow}  G_p \stackrel{\alpha_p}{\longrightarrow}  G_{p-1}\stackrel{}{\longrightarrow} \cdots $$is said to be *exact* if $\text{Im }\alpha_{p+1} = \ker \alpha_p$ for each $p$. A $5$-term exact sequence fo the form$$  0\to A \stackrel{\alpha}{\to} B \stackrel{\beta}{\to} C \to 0 $$is called a *short exact sequence*. Because the image of the zero homomorphism is $\{0\}$, exactness at $A$ means that $\alpha$ is injective, and similarly exactness at $C$ means that $\beta$ is surjective. Exactness at $B$ means that $\ker \beta = \text{Im } \alpha$, and the first isomorphisms theorem then tell us that $C \cong B/\text{Im }\alpha$. A short exact sequence is thus a graphic summary of the first isomorphism theorem. 

**Def:** A sequence of abelian groups and homomorphisms $$ \cdots \stackrel{}{\longrightarrow} C_{p+1} \stackrel{\partial_{p+1}}{\longrightarrow}  C_p \stackrel{\partial_p}{\longrightarrow}  C_{p-1}\stackrel{}{\longrightarrow} \cdots   $$is called a *chain complex* if the composition of any two consecutive homomorphisms is the zero map: $\partial_p\circ \partial_{p+1} = 0$. This is equivalent to the requirement that $\text{Im }\partial_{p+1}\le \ker \partial_p$. The homomorphisms $\partial_p$ are often called 'boundary operators' by analogy with the case of [[singular homology]]. We denote such a chain complex by $C_\bullet$, with the boundary maps being understood by context. In many applications, $C_p$ is defined only for $p\ge 0$, but it is sometimes convenient to extend this to all $p$ by defining $C_p$ to be the trivial group and the associated homomorphisms to be zero for $p <0$.

**Def:** The *$p$th homology group of the chain complex $C_\bullet$* is $$H_p(C_\bullet) := \ker \partial_p /\text{Im }\partial_{p+1}.  $$

**Obs:** The chain complex is exact iff $H_p(C_\bullet) = 0$ for all $p$; thus the homology groups provide a precise quantitative measurement of the failure of exactness.

**Def:** Suppose $C_\bullet$ and $D_\bullet$ are chain complexes. A chain map $F_\bullet: C_\bullet \to D_\bullet$ is a collection of homomorphisms $F_p: C_p \to  D_p$ such that $\partial_p \circ F_p = F_{p-1}\circ \partial_p$ for all $p$
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\cdots\arrow[r] & C_p\arrow[r, "\partial_p"] \arrow[d, "F_{p}"'] & C_{p-1}\arrow[d, "F_{p-1}"]\arrow[r] & \cdots \\
\cdots\arrow[r] & D_p\arrow[r, "\partial_p"] & D_{p-1}\arrow[r] & \cdots
\end{tikzcd}
\end{document}
```
Any chain map that takes $\ker \partial$ to $\ker \partial$ and $\text{Im }\partial$ to $\text{Im }\partial$, and therefore induced a homology homomorphism $F_*: H_p(C_\bullet) \to H_p(D_\bullet)$ for each $p$. 

**Def:** Suppose $C_\bullet$ and $D_\bullet$ are chain complexes, and $F_\bullet, G_\bullet: C_\bullet \to D_\bullet$ are chain maps. A collection of homomorphism $h: C_p \to D_{p+1}$ is called a *chain homotopy from $F_\bullet$ to $G_\bullet$* if the following identity is satisfies on each group $C_p$: $$h \circ \partial + \partial \circ h = G_p- F_p. $$ If there exists such a map, $F$ and $G$ are said to be *chain homotopic*. 

**Obs:** If $F_\bullet, G_\bullet: C_\bullet \to D_\bullet$ are chain maps are homotopic chain maps, then $F_* = G_*: H_p(C_\bullet) \to H_p(D_\bullet)$. 

So th $h$ is behaving like a natural transformation between the chain maps. 

# Cochain Complexes

