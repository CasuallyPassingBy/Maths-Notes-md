---
tags:
  - "#ModuleTheory"
---
Subjects: [[Module Theory]]
Links: [[Vector Spaces]], [[Rings and Fields]], [[Groups]], [[Ring Ideals and Quotient Rings]], [[Polynomial Ring of a Single Variable]]

# Module

**Def:** Let $R$ be a ring, A *left $R$-module* or a *left module over $R$* is a set $M$ together with
- a binary operation $+$ on $M$ under which $M$ is an abelian group, and
- an action of $R$ on $M$ denoted $rm$, for all $r \in R$ and $m \in M$ which satisfies
	- $(r+s) m = rm + sm$, for all $r, s \in R$ and $m \in M$
	- $(rs)m = r(sm)$, for all $r, s \in R$ and $m \in M$
	- $r(m+n) = rm + rn$, for all $r\in R$ and $m,n \in M$
If the ring $R$ has $1$ we impose the additional axiom:
- $1m = m$

The descriptor "left" in the module above indicates that the ring appear on the left; "right" $R$-modules can be defined analogously. If the the ring $R$ is *commutative* and $M$ is left $R$-module we can make $M$ into a right $R$ module by defining $mr = rm$ for all $m \in M$ and $r \in R$. 

In general, when we say module it is a left module. 

Modules that satisfy the last axiom with $R$ a unital ring, is called a *unital module*. 

**Def:** Let $R$ be a ring with $1$ and let $n \in \Bbb N^+$. Then a natural choice for a module is $$R^n = \{(a_1, \dots, a_n) \mid a_i \in R, i < n\}.$$Make $R^n$ into an $R$-modules by componentwise addition and multiplication by elements of $R$ in the same manner as when $R$ is a field. The module $R^n$ is called *the free module of rank $n$ over $R$*. 

**Obs:** When $R$ is a field $F$ the axioms for an $R$-module are precisely the same as those for a vector space over $F$, so that: *modules over a field $F$ and vector spaces over $F$ are the same*.

**Def:** Let $R$ be a ring and $M$ be an $R$-module. An $R$-*submodule* of $M$ is a subgroup $N$ of $M$ which is closed under the action of ring elements, i.e., $rn \in N$ for all $r \in R$ and $n \in N$.

**Def:** If $M$ is an $R$-module and for some ($2$-sided ideal) $I$ of $R$, $am = 0$ for all $a \in  I$ and all $m \in M$, we say that $M$ is *annihilated* by $I$. In this situation we can make $M$ into an $(R/I)$-module by defining an action of the quotient ring $R/I$ on $M$ as follows: for each $m \in M$ and coset $r+I$ in $R/I$ let $$(r+I) m = rm.$$
Since $am = 0$ for all $a \in I$ and all $m \in M$ this is well defined and this makes $M$ into an $(R/I)$-module. If $I$ is a maximal ideal in the commutative ring $R$ and $IM = 0$, then $M$ is a vector space over the field $R/I$. 

**Obs:** Submodules of $M$ are just subsets of $M$ that are themselves modules under the restricted operations. In particular, if $R = F$ is a field, submodules are the same as subspaces. Every $R$-module has two submodules $M$ and $\{0\}$ (the latter is called the *trivial submodule*)

**Prop:** Let $R$ be a ring and let $M$ be an $R$-module. A subset $N$ of $M$ is a submodule of $M$ iff
- $N \neq \varnothing$, and 
- for all $x, y \in N$ and $r \in R$ then $x+ry \in N$. 

**Cor:** The intersection of any collection of submodules or an $R$-module is a submodule. 

**Cor:** Let $N_1 \subseteq N_2 \subseteq \cdots$ be an ascending chain of submodules of $M$, then $\bigcup_{i = 1}^\infty N_i$ is a submodule of $M$.

**Prop:** If $rm = 0$ for some $r\in R$ and $m \in M\setminus \{0\}$, then $r \notin R^\times$. 

**Def:** An element $m$ of the $R$-module $M$ is called a *torsion element* if $rm = 0$ for some nonzero element $r \in R$. The set of torsion elements is denoted $$\text{Tor}(M) := \{m \in M \mid rm = 0, \text{for some }r \in R\setminus\{0\}\}. $$
### $\Bbb Z$-modules

An important example are $\Bbb Z$-modules. Let $G$ be *any abelian group* and write the operation of $A$ as $+$. We consider the action $$na = \begin{cases} g+g+\dots+g\; (n \text{ times}) & n >0 \\ 0 & n = 0 \\ -g -g -\dots -g \;(-n \text{ times}) & n <0 \end{cases}$$This definition of an action on the integers on $G$ makes $G$ into a $\Bbb Z$-module, and the module axioms show that this is the only possible action of $\Bbb Z$ on $A$ making it a $\Bbb Z$-module. Thus every abelian group is a $\Bbb Z$-module. Conversely, if $M$ is a $\Bbb Z$-module, by definition is an abelian group, so 

> $\Bbb Z$-modules are the same as abelian groups.

Furthermore, it is immediate from the definition that 

> $\Bbb Z$-submodules are the as subgroups. 

# Algebra

**Def:** Let $R$ be a commutative ring with identity. An $R$-algebra is a ring $A$ with together a ring homomorphism $f: R \to A$ mapping $1_R$ to $1_A$ such that the subring $f[R]$ of $A$ is in the centre of $A$. 

**Def:** If $A$ and $B$ are two $R$-algebras, an $R$-algebra homomorphism is a ring homomorphism $\varphi: A \to B$  mapping $1_A$ to $1_B$ such that $\varphi (r \cdot a) = r\cdot \varphi(a)$ for all $r \in R$ and $a \in A$. 
