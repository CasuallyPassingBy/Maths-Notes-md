---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Vector Spaces]], [[Product of Vector Spaces]], [[Multilinear Transformation]]

Let $V, W$ be vector spaces over the field $\Bbb F$and where we can define a vector space $V * W$ that has ${V\times W}$ as a basis. $V *W$ can be thought as the space of functions of the form ${(v *w): V\times W \to \Bbb F}$, that

$$ (v'*w')(v,w) = \begin{cases} 1 &\quad (v', w') =(v,w) \\ 0 &\quad \text{otherwise} \end{cases} $$

$V_W=\operatorname{span}\{v_w \mid v \in V \land w \in W\}$ , this brings some properties, such that:
- Let $v \in V$ , $w_1, w_2 \in W$, and $a, b \in \Bbb F$, then ${v*(aw_1 + bw_2) \ne a(v* w_1) + (bv* w_2)}$
- Let $v_1 , v_2 \in V$, $w \in W$, and $a,b\in \Bbb F$, then ${(av_1 +bv_2)*w\ne a(v_1*w) +b(v_2*w)}$

We can create a subspace with these things in mind, such that the we can get product properties out of the free vector space.

$$ Z =\operatorname{span}\{v*(aw_1+bw_2) - a(v*w_1) -b(v*w_2),\newline (av_1+bv_2)*w - a(v_1*w) -b(v_2*w) \mid \newline a,b\in \Bbb F \land v, v_1, v_2\in V \land w, w_1, w_2\in W\} $$

Then we can define $V\otimes W := (V_W)/Z$, then ${v \otimes w := v_w + Z}$. This can be used to get the following properties:

- $v\otimes (aw_1 +w_2) = a(v\otimes w_1) +b(v\otimes w_2)$
- $(av_1+bv_2)\otimes w = a(v_1\otimes w) +b(v\otimes w)$

Some properties that arise of these definition of $V \otimes W$ is that:
- Let $\mathcal{B}_V$be a basis for $V$, similarly $\mathcal{B}_W$ be a basis for $W$, then the set $\mathcal{B}_{V\otimes W}$ defined as the set that contains all $v\otimes w$, such that $v \in \mathcal{B}_V$ and $w \in \mathcal{B}_W$, then $\mathcal B_{V\otimes W}$is a basis for $V\otimes W$. In particular if $V$ and $W$ are finite dimensional, then ${\dim V\otimes W= \dim V \cdot \dim W}$.
- It is associative on vector spaces, in the sense that given vector spaces $U, V$ and $W$ then there’s a canonical isomorphism ${U \otimes (V \otimes W) \cong (U \otimes V) \otimes W}$, where $u\otimes(v\otimes w)$ is mapped to $(u \otimes v)\otimes w$, this makes it possible to ignore parenthesis.
- It is commutative on vector spaces, in the sense that given vector spaces $V, W$, then there’s a canonical isomorphism $V\otimes W \cong W \otimes V$, where $v\otimes w$ is mapped to ${w \otimes v}$. In general $v \otimes w \ne w \otimes v$.

As a piece of notation then $V^{\otimes k} =T^k V$ is the $k$th tensor power of $V$, which is defined as $V^{\otimes 0} = \Bbb F$, and $V^{\otimes(n+1)}= V^{\otimes n} \otimes V$.

We can define the ******_Tensor Algebra of $V$ as_
$$ T(V) = \bigoplus_{k = 0}^\infty T^k V $$

The multiplication in $T(V)$ is determined by the canonical isomorphisms

$$ T^k V\otimes T^lV \to T^{k+l} V $$
## Universal property
The tensor product of two vector spaces $V$ and $W$ is a vector space denoted as $V\otimes W$, together with a bilinear map $\otimes: (v, w) \mapsto v\otimes w$ from $V\times W$ to $V\otimes W$, such that, for every bilinear map $h:V\times W \to Z$, there is a *unique* linear map $\tilde h:V\otimes W \to Z$ such that $h = \tilde h \circ \otimes$.

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}
V \times W \arrow[r,"\otimes"] \arrow[dr, "h"']& V \otimes W \arrow[d, dashed,"\tilde h"]\\ 
& Z
\end{tikzcd}
\end{document}
```
