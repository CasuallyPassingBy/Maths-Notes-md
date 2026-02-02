---
tags:
  - HomologicalAlgebra
---
Subjects: [[Homological Algebra]]
Links: [[Group Homomorphisms and Isomorphisms]], [[Exact Sequences]]
# Chain Complexes

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
Any chain map induces a homology homomorphism $F_*: H_p(C_\bullet) \to H_p(D_\bullet)$ for each $p$. 

**Def:** Suppose $C_\bullet$ and $D_\bullet$ are chain complexes, and $F_\bullet, G_\bullet: C_\bullet \to D_\bullet$ are chain maps. A collection of homomorphism $h: C_p \to D_{p+1}$ is called a *chain homotopy from $F_\bullet$ to $G_\bullet$* if the following identity is satisfies on each group $C_p$: $$h \circ \partial_C + \partial_D \circ h = G_p- F_p. $$If there exists such a map, $F_\bullet$ and $G_\bullet$ are said to be *chain homotopic*. 

We can visualise this diagrammatically as 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\cdots\arrow[r, "\partial_C"] & C_{p+1}\arrow[r, "\partial_C"]\arrow[dr, "h"]\arrow[d, xshift = +0.75ex, "G_{p+1}"]\arrow[d, xshift = -0.75ex, "F_{p-1}"'] & C_p\arrow[d, xshift = +0.75ex, "G_{p}"]\arrow[d, xshift = -0.75ex, "F_{p}"']\arrow[dr, "h"]\arrow[r, "\partial_C"] & C_{p-1}\arrow[r, "\partial_C"]\arrow[d, xshift = +0.75ex, "G_{p-1}"]\arrow[d, xshift = -0.75ex, "F_{p-1}"'] & \cdots \\
\cdots\arrow[r, "\partial_D"] & D_{p+1}\arrow[r, "\partial_D"] & D_p\arrow[r, "\partial_D"] & D_{p-1}\arrow[r, "\partial_D"] & \cdots 
\end{tikzcd}
\end{document}
```
This diagram is not commutative. 

**Obs:** If $F_\bullet, G_\bullet: C_\bullet \to D_\bullet$ are chain maps are homotopic chain maps, then $F_* = G_*: H_p(C_\bullet) \to H_p(D_\bullet)$. 

So th $h$ is behaving like a natural transformation between the chain maps. 

# Cochain Complexes

Let $R$ be a commutative ring, and suppose we are given a sequence of $R$-modules and $R$-linear maps: $$\cdots \longrightarrow A^{p-1} \stackrel{d}{\longrightarrow} A^p  \stackrel{d}{\longrightarrow} A^{p+1}\longrightarrow \cdots. $$
Such a sequence is said to be a *cochain complex* if the composition of two successive applications of $d$ is the zero map:  $d\circ d = 0: A^p \to A^{p+2}$ for each $p$. 

Let us denote $A^\bullet$ the sequence above. If it is a cochain complex, then the image of each map $d$ in the kernel of the next, so we define the *$p$th cohomology of $A^\bullet$* to be quotient module$$H^p(A^\bullet) := \frac{\ker(d: A^p \to A^{p+1})}{\text{Im}(d: A^{p-1}\to A^p)}. $$It can be thought of as a quantitative measure of the failure of exactness at $A^p$. 

If $A^\bullet$ and $B^\bullet$ are cochain complexes, a *cochain map from $A^\bullet$ to $B^\bullet$,* denoted by $F^\bullet: A^\bullet \to B^\bullet$, is a collection of linear maps $F^p: A^p \to B^p$ such that the following diagram commutes for each $p$:
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\cdots\arrow[r] & A^p\arrow[r, "d_A"] \arrow[d, "F^{p}"'] & A^{p+1}\arrow[d, "F^{p+1}"]\arrow[r] & \cdots \\
\cdots\arrow[r] & B^p\arrow[r, "d_B"] & B^{p+1}\arrow[r] & \cdots
\end{tikzcd}
\end{document}
```
The fact that $F\circ d = d\circ F$ means that any cochain map induces a linear map on cohomology $F^*: H^p(A^\bullet) \to H^p(B^\bullet)$ for each $p$. 

**Def:** Suppose $A^\bullet$ and $B^\bullet$ are cochain complexes, and $F^\bullet, G^\bullet: A^\bullet \to B^\bullet$ are chain maps. A collection of homomorphism $h: A^p \to B^{p-1}$ is called a *chain homotopy from $F^\bullet$ to $G^\bullet$* if the following identity is satisfies on each group $A^p$: $$h \circ d_A + d_B \circ h = G^p- F^p. $$If there exists such a map, $F^\bullet$ and $G^\bullet$ are said to be *cochain homotopic*. 

We can visualise this diagrammatically as 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\cdots\arrow[r, "d_A"] & A^{p-1}\arrow[r, "d_A"]\arrow[d, xshift = +0.75ex, "G^{p-1}"]\arrow[d, xshift = -0.75ex, "F^{p-1}"'] & A^p\arrow[d, xshift = +0.75ex, "G^{p}"]\arrow[d, xshift = -0.75ex, "F^{p}"']\arrow[dl, "h"']\arrow[r, "d_A"] & A^{p+1}\arrow[dl, "h"']\arrow[r, "d_A"]\arrow[d, xshift = +0.75ex, "G^{p+1}"]\arrow[d, xshift = -0.75ex, "F^{p+1}"'] & \cdots \\
\cdots\arrow[r, "d_B"] & B^{p-1}\arrow[r, "d_B"] & B^p\arrow[r, "d_B"] & B^{p+1}\arrow[r, "d_B"] & \cdots 
\end{tikzcd}
\end{document}
```
This diagram is not commutative. 

**Obs:** If $F^\bullet, G^\bullet: A^\bullet \to B^\bullet$ are cochain maps are cochain homotopic maps, then $F^* = G^*: H^p(A^\bullet) \to H^p(B^\bullet)$. 
