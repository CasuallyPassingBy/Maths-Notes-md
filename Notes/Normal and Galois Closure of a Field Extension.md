---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Splitting Fields and Normal Field Extensions]], [[Algebraic Closure of a Field]]

**Def:** Let $L/F$ be an algebraic field extension. A *normal closure* of $L/F$ is a field extension $N$ of $L$, $F \subseteq L \subseteq N$, such that
- $N/F$ is normal.
- If $F \subseteq L \subseteq M \subseteq N$, and $M/F$ is normal, then $M = N$. 
In other words, $N$ is the smallest extension of $L$ such that $N/F$ is normal.

**Lemma:** If $L / F$ is finite field extension, then:
- There is a normal closure $N$ of $L/F$, and even more, $N/F$ is finite.
- If $N'$ is a another normal closure $L/F$, the the extensions $N/F$ and $N'/F$ are isomorphic as field extensions. 

**Lemma:** Let $K/F$ be a finite field extension, and fix an algebraic closure $\overline F$ of $F$. Let $\text{Hom}_F(K, \overline F)$ be the set of all $F$-embeddings of $K$ into $\overline F$. The composite field of $\{\sigma(K) \mid \sigma\in \text{Hom}_F(K, \overline F)\}$ is the normal closure of $K/F$. 

**Def:** If $L/F$ is an algebraic and separable field extension, then the normal closure $N$ of $L/F$, then $N/F$ is a Galois field extension, and $N$ is called the *Galois closure* of $L/F$. 

We can prove that this Galois extension exists using [[composite field extensions]]. 

**Prop:** Let $K/F$ be a finite extension. Then $K = F(\theta)$ iff there exists only finitely many subfields of $K$ containing $F$.

**The Primitive Element Theorem:** If $K/F$ is finite and separable, then $K/F$ is simple. In particular, any finite extension of fields of characteristic $0$ is simple.

**Prop:** Let $f(x)\in F[x]$ be an irreducible polynomials of degree $b$ over the field $F$, let $L$ be the splitting field of $f(x)$ over $F$ and let $\alpha$ be a root of $f(x)$ in $L$. If $K$ is any Galois extension of $F$, then the polynomial $f(x)$ splits into a product of $m$ irreducible polynomials each of degree $d$ over $K$, where $d = [K(\alpha): K] = [(L \cap K)(\alpha): L \cap K]$ and $m = n/d = [F(\alpha)\cap K : F]$. 

**Prop:** Let $L/K$ and $K/F$ are $p$-extensions, then the Galois closure of $L/F$ is also a $p$-extension. 