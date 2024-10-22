---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[The Riemann Sphere]]

**************Def:************** An Möbius transformation is of the form $T:\widehat{\Bbb C} \to \widehat{\Bbb C}$

$$ T(z) =\frac{az+b}{cz+d} $$

with $ad-bc \ne0$. Each Möbius function is associated with a matrix $M \in \cal M_2(\Bbb C)$ that is invertible of the form

$$ M= \begin{pmatrix} a & b \\ c & d \end{pmatrix} $$

If $c \ne0$, then it is defined

$$ T\left(\frac{-d}{c}\right) = \infty \quad \text{ and } \quad T(\infty) =\frac{a}{c} $$

If $c =0$, the it is defined

$$ T(\infty) = \infty $$

************Prop:************ Any Möbious transformation

$$ T(z) =\frac{az+b}{cz+d} $$

is injective. If $c=0$, then $T$ is a bijection from $\widehat{\Bbb C}$ to $\widehat{\Bbb C}$. $T^{-1}$ is also an Möbius transformation, and the matrix associated to $T^{-1}$ is of the form

$$ M' = \begin{pmatrix} d &-b \\ -c & a \end{pmatrix} = \operatorname{adj}(M) $$

************Prop:************ Let $L$ and $T$ be Möbius transformations with matrices associated matrices $S$ and $K$, then $L\circ T$ is a Möbius Transformation and the corresponding matrix is $SK$.

******************Cor:****************** The set of Möbius transformations forms a group.

************Prop:************ Let $z_1, z_2, z_3 \in \widehat{\Bbb C}$ and $w_1, w_2, w_3 \in \widehat{\Bbb C}$ such that $z_j \ne z_k$ and $w_j \ne w_k$ when $j \ne k$, then there’s a Möbius transformation such that $T(z_j) = w_j$ for all $j\in \{1,2,3\}$

************Prop:************ If $T$ is a Möbius transformation disctinct of the identity then $T$ has at most two fixed points.

************Prop:************ Any Möbius transformation $T$ can be decomposed into a composition of elemenetary Möbius transformations:

- Transaltions, $T_1 (z) = z+a$
- Rotations/Scaling, $T_2(z) = az$
- Inversion, $T_3(z) = 1/z$

where $c = 0$

We can decompose $T$ with $T_1 (z) = z+\frac{b}{a}$ and $T_2(z) =\frac{a}{d}z$, then ${T_2 \circ T_1 = T}$

Where $c \ne 0$

We can decompose $T$ with $T_1(z) = z + \frac{d}{c}$, $T_2(z) =1/w$ , ${T_3 (z) =((bc-ad)/c^2)z}$ , and finally ${T_4(z) = z + \frac{a}{c}}$. With this we have that ${T = T_4 \circ T_3 \circ T_2 \circ T_1}$

**********Prop:********** Let $T(z) =1/z$, and $R$ be the rotation of $\Bbb R^3$ with the matrix

$$ \begin{pmatrix} 1 & 0 & 0\\ 0 & -1 & 0 \\ 0 & 0 & -1 \end{pmatrix} $$

and $E$ be the stereographic projection of $S$ to $\widehat{\Bbb C}$, then

$$ T(z) =(E\circ R\circ E^{-1})(z) $$

**********Cor:********** Let $T$ be the Möbius function $T(z) =1/z$. If $C \subseteq \widehat{\Bbb C}$ is a straight line or circumference, then $T(C)$ is also a straight line or a circle, more specifically:

- If $C \subseteq \widehat{\Bbb C}$ is a straight line that doesn’t pass throught the origin, then $T(C)$ is a circumference that passes through the origin
- If $C \subseteq \widehat{\Bbb C}$ is a straight line that passes through the origin, then $T(C)$ is a straightline that passes through the origin
- If $C \subseteq \widehat{\Bbb C}$ is a circumference that doesn’t pass through the origin, then $T(C)$ is a circumference that doesn’t pass through the origin
- If $C \subseteq \widehat{\Bbb C}$ is a cirumferenc that passes through the origin, then $T(C)$ is a straight line that doens’t pass through the origin.

### More to add about Möbius functions