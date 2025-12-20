---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Galois Groups of Polynomials]], [[Galois Field Extensions]], [[Cyclic Groups]]

**Def:** *Simple radical extensions*  are extensions obtained by adjoining to a field $F$ the $n$th root of an element $a$ in $F$. 

**Obs:** Since all the roots of the polynomial $x^n -a$ for $a\in F$ differ by factors fo the $n$th roots of unity, adjoining one such root with give a Galois extension iff this field contains the $n$th roots of unity. Simple radical extensions are best behaved when the base field $F$ already contains the appropriate roots of unity. The symbol $\sqrt[n] a$ for $a\in F$ is used to denote any root of the polynomial $x^n -a$. 

**Def:** The extension $K/F$ is said to be *cyclic* if it is Galois with a cyclic Galois group. 

**Prop:** Let $F$ be a field of characteristic not diving $n$ which contains the $n$th roots of unity. The extension $F(\sqrt[n] a)$ for $a\in F$ is cyclic over $F$ of degree dividing $n$. 

Let $K$ be any cyclic extension of degree $n$ over a field $F$ of characteristic not dividing $n$ which contains the $n$th roots of unity. Let $\sigma$ of the generator for the cyclic group $\text{Gal}(K/F)$. 

**Def:** For $\alpha\in K$ and any $n$th root of unity $\zeta$, we define the *Lagrange resolvent* $(\alpha, \zeta) \in K$ by $$(\alpha, \zeta) := \alpha + \zeta\sigma(\alpha) + \zeta^2\sigma^2(\alpha) +\dots + \zeta ^{n-1}\sigma^{n-1}(\alpha) = \sum_{k <n} \zeta^k\sigma^k(\alpha).$$
If we apply the automorphism $\sigma$ to $(\alpha, \zeta)$ we get that $$\sigma(\alpha, \zeta) = \zeta^{-1}(\alpha, \zeta).$$It follows that $$\sigma((\alpha, \zeta)^n) = (\alpha, \zeta)^n $$