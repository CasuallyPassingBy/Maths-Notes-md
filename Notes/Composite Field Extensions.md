---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]]

**Def:** Let $K_1$ and $K_2$ be two subfields of $K$. Then the *composite field* of $K_1$ and $K_2$, denoted $K_1K_2$, is the smallest subfields of $K$ containing both $K_1$ and $K_2$. Similarly, the composite of any collection of subfields of $K$ is the smallest subfield containing all the subfields. 

**Prop:** If $K_1$ and $K_2$ be two finite extensions of a field $F$ contained in $K$, then $$[K_1K_2: F ] \le [K_1:F] [K_2: F].$$with equality iff an $F$-basis for one of the fields remains linearly independent over the other field. If $\alpha_1,\alpha_2,\dots, \alpha_n$ and $\beta_1,\dots, \beta_m$ are bases for $K_1$ and $K_2$ over $F$, respectively, then the elements $\alpha_i \beta_j$ for $i\in \{1,\dots, n\}$ and $j \in \{1,\dots, m\}$ span $K_1K_2$ over $F$. 

**Cor:** Suppose that $[K_1: F] = n$, $[K_2: F]= m$, where $K_1/F$ and $K_2/F$ are field extensions, $(n, m) = 1$, then $[K_1K_2: F] = [K_1: F] [K_2: F]$. 

**Prop:** The field $F(\alpha_1,\dots, \alpha_n)$ is the composite field of the fields $F(\alpha_1)$, $F(\alpha_2)$,..., $F(\alpha_n)$.

**Prop:** Let $K_1$ and $K_2$ be two finite field extensions of a field $F$ contained in the field $K$. The $F$-algebra $K_1\otimes K_2$ is a field iff $[K_1K_2: F] = [K_1: F] [K_2:F]$, where $K_1\otimes K_2$ is represents the [[Tensor Product of Modules|tensor product]] of vector spaces. 

**Obs:** Let $K_1$ and $K_2$ be finite extensions of $F$ contained in a field $K$, and assume both are splitting fields over $F$.
- $K_1K_2$ is a splitting field over $F$.
- $K_1\cap K_2$ is a splitting field over $F$.