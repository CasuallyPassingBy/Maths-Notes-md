---
tags:
---
Subjects: [[Ring Theory]]
Links: [[Module and Algebra (Structure)]], [[Rings]], [[Ring homomorphisms]]

**Def:** A ring $S$ is called a *graded ring* if it is the direct sum of additive subgroups: $$ S = \bigoplus_{n < \omega} S_n$$such that $S_i S_j \subseteq S_{i+j}$ for all $i, j < \omega$. The elements of $S_k$ are said to be *homogeneous of degree $k$*, and $S_k$ is called *homogeneous components of $S$ of degree $k$.*

**Def:** An ideal $I$ of the graded ring $S$ is called a *graded ideal* if $$ I = \bigoplus_{n < \omega}I \cap S_n$$
**Def:** A ring homomorphism $\varphi: S \to T$ between two graded rings is called a *homomorphism of graded rings* if it respects the grading structures of $S$ and $T$, i.e., if $\varphi[S_k] \subseteq T_k$ for $k < \omega$. 

**Obs:** We note that $S_0 S_0 \subseteq S_0$ this implies that $S_0$ is a subring of the graded ring $S$ and then $S$ is an $S_0$-module. If $S_0$ is in the centre of $S$ and it contains an identity of $X$, then $S$ is an $S_0$*-algebra*. 

**Def:** A graded algebra $A = \bigoplus_{k <\omega} A_k$ is said to be *anitcommutative* or *graded commutative* if for all $a\in A_k$ and $b\in A_\ell$, $$ab = (-1)^{k \ell} ba$$
A *homomorphism of graded algebras* is an algebra homomorphism that preserves the degree. 

**Prop:** Let $S$ be a graded ring, let $I$ be a graded ideal in $S$ and let $I_k = I \cap S_k$ for all $k \ge 0$. Then $S/I$ is naturally a graded ring whose homogeneous component of degree $k$ is isomorphic $S_k/I_k$. 

**Def:** Let $(G,+,0)$ be an abelian group. A ring $R$ is said to be *$G$-graded* if there exists a subspace $R_g$ for each $g \in G$ such that $$R = \bigoplus_{g \in G}R_g,$$and if given $x_g\in R_g$ and $y_h \in R_h$, it follows that $x_gy_l \in A_{g+h}$. The elements of $R_g$ are said to be *homogeneous of degree $g$*. In general, we use the notation $g = \deg(x_g)$ for $x_g \in R_g$. Since $G$ is abelian, $$\deg(x_g y_h) = \deg(x_g) + \deg(y_h).$$