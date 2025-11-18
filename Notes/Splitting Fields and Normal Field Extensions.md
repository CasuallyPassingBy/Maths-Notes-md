---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Automorphism Group of a Field Extension]], [[Field Extensions]]

**Def:** Let $F$ be a field and $f(x) \in F[x]$. An extension $L$ of $F$ is called a *splitting field of $f(x)$* over $F$ if
- $f(x)$ is decomposed into linear factors in $L[x]$. 
- If $M$ is another extension of $F$, where $f(x)$ is a decomposed into linear factors in $M[x]$ and $M\subseteq L$, then $M = L$.
- $L = F(\alpha_1,\dots, \alpha_n)$, where $\alpha_1,\dots,\alpha_n$ are the roots of $f(x)$. 

**Prop:** If $F$ is a field and $f(x) \in  F[x]$ is a polynomial of degree $n \ge 1$, then there exists a splitting field $L/F$ of $f(x)$, and $[L: K] \le n!$. 

**Lemma:** Let $\phi: F \to F'$ be a field isomorphism and $f(x) \in F[x]$ be a polynomial. If $L$ is a splitting field of $f(x)$ over $F$, and $L'$ be a field extension of $F'$ such that $\phi(f(x)) \in F'[x]$ decomposes into linear factors in $L'[x]$, then there exists a monomorphism $\psi: L \to L'$ such that $\psi|_F = \phi$. 
```tikz
\usepackage{tikz-cd} 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
L\arrow[r,dashed, "\psi"]\arrow[d, dash] & L'\arrow[d, dash]\\
F\arrow[r, "\phi", "\simeq"'] & F'
\end{tikzcd}
\end{document}
```

By my definition of a field extension, this actually tells us that $L'/L$ is a field extension. In particular, every field that where $f(x)$ is decomposed into linear factors must extend the splitting field $L$ of $f(x)$ over $F$.

**Th:** Let $\phi: F \to F'$ be a field isomorphism and $f(x)\in F[x]$ a polynomial. If $L$ is a splitting field of $f$ over $F$ and let $L'$ be a splitting field of $\phi(f)$ over $F'$, then there's an isomorphism $\psi: L \to L'$ such that $\psi|_F = \phi$, meaning that $L/F$ and $L'/F'$ are isomorphic extensions 
```tikz
\usepackage{tikz-cd} 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
L\arrow[r,dashed, "\psi", "\simeq"']\arrow[d, dash] & L'\arrow[d, dash]\\
F\arrow[r, "\phi", "\simeq"'] & F'
\end{tikzcd}
\end{document}
```

**Uniqueness of the Splitting Field:** Let $F$ be a field and $f(x)\in F[x]$ a polynomial. If $L$ and $L'$ are splitting fields of $f(x)$ over $F$, then there exists an isomorphism $\psi: L \to L'$ such that $\psi|_F = \text{id}_F$. 

**Def:** A field extension $L/F$ is called *normal* if every irreducible polynomials $f(x)\in F[x]$ that has a root in $L$, then it has all roots in $L$. 

**Th:** Let $L/F$ be a field extension. $L/F$ is a normal and finite extension iff $L$ is the splitting field for some polynomial in $F[x]$. 

**Examples:**
- $\Bbb Q(\sqrt 2)$ is the splitting field of $x^2-2$. We also note that $\Bbb Q(\sqrt 2)/\Bbb Q$ is a normal field extension.
- $\Bbb Q(\sqrt[3]2)$ is not the splitting field of $x^3-2$, since it doesn't into linear factor inside $\Bbb Q(\sqrt[3] 2)[x]$, and $[\Bbb Q(\sqrt[3] 2): \Bbb Q] = 3$ while $\text{Aut}(\Bbb Q(\sqrt [3]2)/\Bbb Q) = \{\text{id}\}$. 