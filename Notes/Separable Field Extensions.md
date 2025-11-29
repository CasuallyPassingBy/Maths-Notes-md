---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Automorphism Group of a Field Extension]], [[Splitting Fields and Normal Field Extensions]]

**Def:** An irreducible polynomial $f(x)\in F[x]$ is called *separable* over $F$ if it has no multiple roots in its splitting field, An irreducible polynomial $f(x) \in F[x]$ is called *inseparable* over $F$ if it is not separable. 

**Lemma:** Let $F$ be a field. A nonzero polynomial $f(x)\in F[x]$, with a multiple root in the splitting field iff $f$ and $f'$ have a factor of degree $n \ge 1$ in $F[x]$. 

**Cor:** Let $F$ be a field and $f(x) \in F[x]$ irreducible.
- If $F$ has characteristic $0$, then $f(x)$ is separable over $F$.
- If $F$ has characteristic $p\ne 0$, then $f(x)$ is inseparable iff $f(x)$ is of the form $f(x) = g(x^p)$ with $g(x)\in F[x]$. This last condition means that the all the powers of $x$ that appear in $f(x)$ are only the one that correspond with a integer multiple of $p$. 

**Def:** Let $F$ be a field of characteristic $p$. The map $\phi: F \to F$ such that $\phi(a) = a^p$ is a monomorphism called the *Frobenious endomorphism* of $F$. 

**Cor:** If $F$ is a finite field of characteristic $p$, then every element of $F$ is a $p$th power in $F$, notationally, $F = F^p$, or that the Frobenious endomorphism is actually an isomorphism. 

**Obs:** Let $f(x)\in F[x]$. If $F$ is a finite field of characteristic $p$, then $f(x)^p = f(x^p)$. 

**Prop:** Every irreducible polynomial over a finite field $F$ is separable. A polynomial if $F[x]$ is separable iff it is the product of distinct irreducible polynomials in $F[x]$. 

**Def:** If $L/F$ is a field extension, an algebraic element $\alpha\in L$ over $F$ is called *separable over $F$*, if $\text{Irr}(\alpha, F)\in F[x]$ is separable. The extension $L/F$ is called *separable* if every $\alpha\in L$ is separable over $F$. An arbitrary polynomial $f(x)\in F[x]$ is called *separable over $F$* is all of its irreducibles factors are separable over $F$. A field extension which is not separable is *inseparable*. 

**Prop:** Let $L/F$ be an algebraic separable extension. If $F \subseteq K \subseteq L$ is an intermediate field, then the subextensions $L/K$ and $K/F$ are also separable. 

**Def:** A field $K$ of characteristic $p$ is called *perfect* if every element of $K$ is a $p$th power in $K$, i.e., $K = K^p$. Ant field of characteristic $0$ is also called perfect.

**Th:** Let $F$ be a field with characteristic $p> 0$. $F$ is a perfect field iff every finite extension is separable. 

**Prop:** Let $p(x)$ be an irreducible polynomial over a field $F$ of characteristic $p$. Then there is a unique integer $k \ge 0$ and a unique irreducible separable polynomial $p_\text{sep}\in F[x]$ such that $$p(x) = p_\text{sep} (x^{p^k}).$$
**Def:** Let $p(x)$ be an irreducible polynomial of characteristic $p$. The degree of $p_\text{sep}(x)$ in the last proposition is called the *separable degree* of $p(x)$, denoted $\deg_s p(x)$. The integer $p^k$ in the proposition is called the *inseparable degree* of $p(x)$, dented $\deg_i p(x)$. 

**Obs:** Let $p(x)\in F[x]$. $p(x)$ is separable iff it inseparability degree is $1$ iff its degree is equal to its separable degree. Also, computing degree in the relation $p(x) = p_\text{sep}(x^{p^k})$ we see that $$\deg p(x) = \deg_s p(x) \deg_i p(x).$$
**Def:** Let $E/F$ be any finite separable extension. The Galois extension $K$ of $F$ containing $E$ is called the *Galois closure* of $E$ over $F$. 

**Prop:** Let $K/F$ be a finite extension. Then $K = F(\theta)$ iff there exists only finitely many subfields of $K$ containing $F$.

**The Primitive Element Theorem:** If $K/F$ is finite and separable, then $K/F$ is simple. In particular, any finite extension of fields of characteristic $0$ is simple.