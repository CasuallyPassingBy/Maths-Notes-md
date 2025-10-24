---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Rings and Fields]], [[Groups]]

Let $G$ be a group, written multiplicative, and let $R$ be a ring. The group ring of $G$ over $R$, which we will denote by $R[G]$, or simply $RG$, is  $$R[G] :=\bigoplus_{g\in G} R,$$the set of functions $f: G \to R$ with finite support. Addition is done componentwise. to turn the additive group $R[G]$ into a ring, we define the product of $f$ and $g$ to be the mapping $$ x\mapsto \sum_{uv = x} f(u) g(v) = \sum_{u \in G} f(u) g(u^{-1} x).$$The sum is well defined because $f$ and $g$ are of finite support, and the ring axioms are easily verified. 

Some variations in the notations and terminology are in use. In particular, the mappings such as $f: G \to R$ are sometimes written as what are called *formal linear combination of elements of $G$ with coefficients in $R$*: $$\sum_{g\in G} f(g) g = \sum_{g\in G} f_g g. $$
Let us note that if $1_G$ represents the identity element of $G$, the we $a 1_G$ for any element $a\in R$, is also an element of $R[G]$. Thus we see that $R\hookrightarrow R[G]$. 

**Prop:** If $R$ and $G$ are both commutative, then $R[G]$ is commutative.

**Obs:** if $H \le G$, then $R[H]$ is a subring of $R[G]$. Similarly, if $S$ is a subring of $R$, then $S[G]$ is a subring of $R[G]$. 

**Prop:** If $G$ is a finite group of order greater than $1$, then $R[G]$ always hace zero divisors. 