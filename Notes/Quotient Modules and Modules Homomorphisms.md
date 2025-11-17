---
tags:
---
Subjects: [[Module Theory]]
Links: [[Module and Algebra]], [[Space of Linear Transformations]], [[Endomorphism Ring]], [[Quotient of Vector Spaces]], [[Normal Subgroups and Quotient Groups]]

**Def:** Let $R$ be a ring and let $M$ and $N$ be $R$-modules.
- A map $\varphi: M \to N$ is an $R$*-module homomorphism* if it respects the $R$-module structure of $M$ and $N$, i.e., 
	- $\varphi(x+y) = \varphi(x)+\varphi(y)$, for all $x,y \in M$, and
	- $\varphi(rx) = r\varphi(x)$ for all $r \in R$ and all $x\in M$. 
- An $R$-module homomorphism is an *isomorphism* (of $R$-module) if it is both injective and surjective. The modules $M$ and $N$ are said to be *isomorphic*, denoted $M \cong N$, if there is $R$-module isomorphism $\varphi: M \to N$.
- If $\varphi: M \to N$ is an $R$-module homomorphism, let $\ker \varphi := \varphi^{-1}\{0\}$ (the *kernel* of $\varphi$) and let $\varphi[M]$ (the *image* of $\varphi$, as usual)
- Let $M$ and $N$ be $R$-modules and define $\text{Hom}_R(M, N)$ be the set of all $R$-module homomorphism from $M$ to $N$.

**Prop:** Let $M, N$ and $L$ be $R$-modules.
- A map $\varphi: M \to N$ is an $R$-module homomorphism iff $\varphi(rx+y) = r\varphi(x)+\varphi(y)$ for all $x, y \in M$ and all $r\in R$.
- Let $\varphi, \psi$ be elements of $\text{Hom}_R(M, N)$. Define $\varphi + \psi$ by $$(\varphi+\psi)(x) = \varphi(m) + \psi(m) \qquad \text{for all } m \in M.$$Then $\varphi + \psi \in \text{Hom}_R(M, N)$ and this operation $\text{Hom}_R(M, N)$ is an abelian group. If $R$ is a commutative ring then for $r\in R$ define $r\varphi$ by $$(r\varphi)(m) = r\varphi(m) \qquad \text{for all }m \in M.$$Then $r\phi \in \text{Hom}_R(M, N)$ and with this action of the commutative ring $R$ the abelian group $\text{Hom}_R(M, N)$ is an $R$-module.
- If $\varphi \in \text{Hom}_R(L, M)$ and $\psi \in \text{Hom}_R(M, N)$ then $\psi \circ \varphi \in \text{Hom}_R(L, N)$
- With addition as above and multiplication as defined as function composition, $\text{Hom}_R(M, M)$ is a ring with $1$. When $R$ is commutative $\text{Hom}_R(M, M)$ is an $R$-algebra.

**Def:** The ring $\text{Hom}_R(M, M)$ is called the *endomorphism ring of $M$* and will often be denoted by $\text{End}_R(M)$, or just $\text{End}(M)$ when $R$ is clear from the context. The elements of $\text{End}_R(M)$ are called *endomorphisms*. 

**Prop:** 

**Prop:** Let $R$ be a ring, let $M$ be an $R$-module and let $N$ be a submodule of $M$. The (additive, abelian) quotient group $M/N$ can be made into an $R$-module by defining the action of elements of $R$ by $$ r(x+ N) = rx + N\qquad \text{ for all } r \in R, x+N \in M/N.$$ The natural projection map $\pi: M \to M/N$ defined by $\pi(x) = x+N$ is an $R$-module homomorphism with kernel $N$.

**Prop:** Let $A_1, \dots A_n$ be $R$-modules and let $B_i$ be a submodule of $A_i$ for each $i = 1, \dots ,n$. Then $$(A_1 \times \dots A_n) /(B_1\times \dots\times B_n) \cong (A_1/B_1) \times \dots \times (A_n/B_n).$$
**Def:** Let $A$ and $B$ be submodules of the $R$-module $M$. The *sum* of $A$ and $B$ is the set $$A + B := \{a+b \mid a \in A, b \in B\}.$$This is the smallest submodule which contains both $A$ and $B$.

**Imorphism Theorems:** 
- (The First Isomorphism Theorem for Modules). Let $M$, $N$ be $R$-modules and let $\varphi: M \to N$ be an $R$-module homomorphism. Then $\ker \varphi$ is a submodule of $M$ and $M/\ker \varphi \cong \varphi[M]$. 
- (The Second Isomorphism Theorem for Modules). Let $A, B$ be submodules of the $R$-modules $M$. Then $(A+ B)/B \cong A /(A\cap B)$.
- (The Third Isomorphism Theorem for Modules). Let $M$ be an $R$-module, and let $A$ and $B$ be submodules of $M$ with $A \subseteq B$. Then $(M/A)/(B/A) \cong M/B$.
- (The Fourth Isomorphism Theorem for Modules). Let $N$ be a submodule of the $R$-module $M$. There is a bijection between submodules of $M$ which contain $N$ and the submodules of $M/N$. The correspondence $A \leftrightarrow A/N$, for all $A \supseteq N$. 

This last theorem actually induces a lattice isomorphism between the lattice of submodules of $M/N$ and the lattice of submodules of $M$ which contain $N$. 