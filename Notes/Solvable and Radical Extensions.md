---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Galois Groups of Polynomials]], [[Galois Field Extensions]], [[Cyclic Groups]], [[Cyclotomic Polynomials and Extensions]]

**Def:** *Simple radical extensions* are extensions obtained by adjoining to a field $F$ the $n$th root of an element $a$ in $F$. 

**Obs:** Since all the roots of the polynomial $x^n -a$ for $a\in F$ differ by factors fo the $n$th roots of unity, adjoining one such root will give a Galois extension iff this field contains the $n$th roots of unity. Simple radical extensions are best behaved when the base field $F$ already contains the appropriate roots of unity. The symbol $\sqrt[n] a$ for $a\in F$ is used to denote any root of the polynomial $x^n -a$. 

**Def:** The extension $K/F$ is said to be *cyclic* if it is Galois with a cyclic Galois group. 

**Prop:** Let $F$ be a field of characteristic not diving $n$ which contains the $n$th roots of unity. The extension $F(\sqrt[n] a)$ for $a\in F$ is cyclic over $F$ of degree dividing $n$. 

Let $K$ be any cyclic extension of degree $n$ over a field $F$ of characteristic not dividing $n$ which contains the $n$th roots of unity. Let $\sigma$ of the generator for the cyclic group $\text{Gal}(K/F)$. 

**Def:** For $\alpha\in K$ and any $n$th root of unity $\zeta$, we define the *Lagrange resolvent* $(\alpha, \zeta) \in K$ by $$(\alpha, \zeta) := \alpha + \zeta\sigma(\alpha) + \zeta^2\sigma^2(\alpha) +\dots + \zeta ^{n-1}\sigma^{n-1}(\alpha) = \sum_{k <n} \zeta^k\sigma^k(\alpha).$$
If we apply the automorphism $\sigma$ to $(\alpha, \zeta)$ we get that $$\sigma(\alpha, \zeta) = \zeta^{-1}(\alpha, \zeta).$$It follows that $$\sigma((\alpha, \zeta)^n) = (\alpha, \zeta)^n $$
We see that $(\alpha, \zeta)^n$ is fixed by $\text{Gal}(K/F)$, hence is an element of $F$ for any $\alpha\in K$. 

**Prop:** Any cyclic extension of degree $n$ over a field $F$ of characteristic not dividing $n$ which contains the $n$th roots of unity is of the form $F(\sqrt[n] a)$ for some $a\in F$. 

**Def:** An element $\alpha$ which is algebraic over $F$ can be *expressed by radicals* or *solved for in terms of radicals* if $\alpha$ is an element of a field $K$ which can be obtained by a succession of simple radical extensions $$F = K_0 \hookrightarrow K_1 \hookrightarrow \cdots \hookrightarrow K_i \hookrightarrow K_{i+1} \hookrightarrow \cdots \hookrightarrow K_n = K$$where $K_{i+1} = K_i (\sqrt[n_i]{ a_i})$ for some $a_i \in K_i$, $i = 0, 1,\dots, n-1$. Here $\sqrt[n_i]{a_i}$ denotes some root of the polynomial $x^{n_i}-a_i$. such a field $K$ will be called a *root extension* of $F$.

A polynomial $f(x)\in F[x]$ can be *solved by radicals* if all its roots can be solved for in terms of radicals.

This gives us a precise meaning to the intuitive notion that $\alpha$ is obtained by successive algebraic operations and successive root extractions. 

In considering radical extensions one may always adjoin roots of unity, since by definition roots of unity are radicals. 

**Obs:** The composite of two root extensions is again a root extension. 

**Lemma:** If $\alpha$ is solved for in terms of radicals, then $\alpha$ is contained in a root extension which is Galois over $F$ and where each extension $K_{i+1}/K$ is cyclic. 

**Th:** The polynomial $f(x)$ can be solved by radicals iff its Galois group is [[Solvable Groups|solvable]].

This theorem gives us Galois' fundamental connection between solving roots of polynomials in terms of radical and the Galois group of the polynomial. 

**Cor:** The general equation of degree $n$ cannot be solved by radicals for $n \ge 5$. This is immediate since $S_n$, and $A_n$ are not solvable for $n \ge 5$. 

## Cardano's Formula
