---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Group Homomorphisms and Isomorphisms]], [[Rings and Fields]], [[Ring Ideals and Quotient Rings]]

**Def:** Let $R$ and $S$ be rings.
- A *ring homomorphism* is a map $\varphi: R \to S$ satisfying
	- $\varphi(a+b) = \varphi(a) +\varphi(b)$ for all $a, b\in R$ (so $\varphi$ is a group homomorphism on the additive groups), and
	- $\varphi(ab) = \varphi(a)\varphi(b)$ for all $a,b\in R$.
- The *kernel* of the ring homomorphism $\varphi$, denoted $\ker \varphi$, is the set of $R$ that map to $0$ in $S$. 
- A bijective ring homomorphism is called an *isomorphism*. 

**Prop:** Let $R$ and $S$ be rings, and let $\varphi: R \to S$ be a homomorphism.
- The image of $\varphi$ is a subring of $S$.
- The kernel of $\varphi$ is an ideal of $R$

**Prop:** Let $\varphi: R \to S$ be a surjective homomorphism of rings. Then the image of the centre of $R$ is contained in the centre of $S$. 

**Prop:** Let $R$ and $S$ be unital rings, and denote their respective identities by $1_R$ and $1_S$. Let $\varphi: R \to S$ be a nonzero homomorphism of rings.
- If $\varphi(1_R) \ne 1_S$, then $\varphi(1_R)$ is a zero divisor in $S$. This means that if $S$ is an integral domain, then every ring homomorphism from $R$ to $S$ sends the identity of $R$ to the identity of $S$.
- If $\varphi(1_R) = 1_S$, then $\varphi(u)\in S^\times$ and $\varphi(u^{-1}) = \varphi(u)^{-1}$ for each $u \in R^\times$. 

**First Isomorphism Theorem for Rings:** If $\varphi: R \to S$ is a homomorphism of rings, then the kernel of $\varphi$ is an ideal of $R$, the image of $\varphi$ is a subring of $S$, and $R/\ker\varphi$ is isomorphic to $\varphi[R]$, or $$R/\ker\varphi \cong \text{Im }\varphi. $$
**Prop:** If $I$ is an ideal of $R$, then the map $\pi_I: R \to R/I$ defined by $r \mapsto r+I$ is a surjective ring homomorphism with kernel $I$, this homomorphism is called the *natural projection of $R$ onto $R/I$*. Thus every ideal is the kernel of a ring homomorphism. 

**Cor:** Let $S$ be a subring of $R$ and $I$ be an ideal of $R$. If $S \cap I = 0$, then $\pi_I[S] \cong S$. 

**Second Isomorphism Theorem:** Let $A$ be a subring and let $B$ be an ideal of $R$. Then $A+B := \{a+b\mid a\in A, b\in B\}$ is a subring of $R$, $A\cap B$ is an ideal of $A$, and $$({A+B})/{B}\cong {A}/({A\cap B}).$$
**Third Isomorphism Theorem:** Let $I$ and $J$ be ideals of $R$ with $I \subseteq J$. Then $J/I$ is an ideal of $R/I$, and $$\frac{R/I}{J/I}\cong R/J.$$
**Fourth Isomorphism Theorem or Lattice Isomorphism Theorem:** Let $I$ be an ideal of $R$. The correspondence $A \leftrightarrow A/I$ is an inclusion preserving bijection between the set of subrings $A$ or $R$ that contain $I$ and the set of subrings $R/I$. Furthermore, $A$ is an ideal of $R$ that contain $I$ iff $A/I$ is an ideal of $R/I$. 

**Prop:** Let $\varphi:R \to S$ be a ring homomorphism.
- If $J\le S$, then $\varphi^{-1}[J]$ is an ideal of $R$. In particular, if $R$ is a subring of $S$, and $\varphi$ is the inclusion then $R \cap J\le R$. 
- If $I \le R$, then $\varphi[I] \le \varphi[R]$. In particular if $\varphi$ is a surjective homomorphism, then $\varphi[I] \le S$. 

From the point of view of category theory we have the following morphisms. 
- Isomorphisms, bijective ring homomorphisms. 
- Monomorphisms, injective homomorphisms,
- Epimorphisms, a right cancellative ring homomorphism.
- Surjective morphisms, which are a special type of epimorphism.
- Bimorphisms, injective epimorphism. 