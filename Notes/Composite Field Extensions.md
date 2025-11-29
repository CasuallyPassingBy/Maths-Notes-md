---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Galois Field Extensions]], [[Classification of Simple Field Extensions]], [[Separable Field Extensions]]

**Def:** Let $K_1$ and $K_2$ be two subfields of $K$. Then the *composite field* of $K_1$ and $K_2$, denoted $K_1K_2$, is the smallest subfields of $K$ containing both $K_1$ and $K_2$. Similarly, the composite of any collection of subfields of $K$ is the smallest subfield containing all the subfields. 

**Prop:** If $K_1$ and $K_2$ be two finite extensions of a field $F$ contained in $K$, then $$[K_1K_2: F ] \le [K_1:F] [K_2: F].$$with equality iff an $F$-basis for one of the fields remains linearly independent over the other field. If $\alpha_1,\alpha_2,\dots, \alpha_n$ and $\beta_1,\dots, \beta_m$ are bases for $K_1$ and $K_2$ over $F$, respectively, then the elements $\alpha_i \beta_j$ for $i\in \{1,\dots, n\}$ and $j \in \{1,\dots, m\}$ span $K_1K_2$ over $F$. 

**Cor:** Suppose that $[K_1: F] = n$, $[K_2: F]= m$, where $K_1/F$ and $K_2/F$ are field extensions, $(n, m) = 1$, then $[K_1K_2: F] = [K_1: F] [K_2: F]$. 

**Prop:** The field $F(\alpha_1,\dots, \alpha_n)$ is the composite field of the fields $F(\alpha_1)$, $F(\alpha_2)$,..., $F(\alpha_n)$.

**Prop:** Let $K_1$ and $K_2$ be two finite field extensions of a field $F$ contained in the field $K$. The $F$-algebra $K_1\otimes K_2$ is a field iff $[K_1K_2: F] = [K_1: F] [K_2:F]$, where $K_1\otimes K_2$ is represents the [[Tensor Product of Modules|tensor product]] of vector spaces. 

**Obs:** Let $K_1$ and $K_2$ be finite extensions of $F$ contained in a field $K$, and assume both are splitting fields over $F$.
- $K_1K_2$ is a splitting field over $F$.
- $K_1\cap K_2$ is a splitting field over $F$.

**Prop:** Suppose $K/F$ is a finite Galois extension, and $F'/F$ is any extension. Then $KF'/F'$ is a finite Galois extension, with Galois group $$\text{Gal}(KF'/F') \cong \text{Gal}(K/K \cap F')$$isomorphic to a subgroup of $\text{Gal}(K/F)$. Pictorially,
```tikz
\usepackage{tikz-cd}
\usetikzlibrary{decorations.markings}
 
\tikzset{
  tick/.style={
    postaction={decorate},
    decoration={markings, mark=at position 0.5 with {
      % size parameter
      \def\s{3pt} 
      \def\gap{2pt}
      % first tick
      \draw (-\s,-\s) -- (\s,\s);
      % second tick (slightly shifted)
      \draw (-\s+\gap,-\s-\gap) -- (\s+\gap,\s-\gap);
    }}
  }
}
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}  
& KF'\arrow[dl, dash] \arrow[dr, dash, tick]& \\
K\arrow[dr, dash, tick]&& F'\arrow[dl, dash]\\
&K \cap F'\arrow[d, dash] \\
&F&
\end{tikzcd}
\end{document}
```
We also see that $[KF': F'] = [K: K \cap F']$. 

**Cor:** Suppose $K/F$ is a finite Galois extension and $F'/F$ is any finite extension. Then $$ [KF': F] = \frac{[K:F][F':F]}{[K \cap F': F]}.$$
**Lemma:** Let $K/F$ and $L/F$ be field extensions and $F \subseteq K \cap L$.
- If $K$ and $L$ are normal extension of $F$, then $KL/F$ and $K\cap L /F$ are normal extensions. 
-  If $K$ and $L$ are separable extension of $F$, then $KL/F$ and $K\cap L /F$ are separable extensions. 

**Prop:** Let $K_1$ and $K_2$ be finite Galois extensions of a field $F$. Then
- The intersection $K_1\cap K_2$ is Galois over $F$
- The composite $K_1K_2$ is Galois over $F$. The Galois group is isomorphic to the subgroup $$H = \{(\sigma, \tau) \mid \sigma_{K_1 \cap K_2} = \tau_{K_1\cap K_2}\}\le \text{Gal}(K_1/F)\times \text{Gal}(K_2/F) $$consisting of elements whose restrictions to the intersection $K_1 \cap K_2$ are equal. 
```tikz
\usepackage{tikz-cd}
\usetikzlibrary{decorations.markings}
 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}  
& K_1K_2\arrow[dl, dash] \arrow[dr, dash]& \\
K_1\arrow[dr, dash]&& K_2\arrow[dl, dash]\\
&K_1 \cap K_2\arrow[d, dash] \\
&F&
\end{tikzcd}
\end{document}
```
**Cor:** Let $K_1$ and $K_2$ be Galois extensions of a field $F$ with $K_1 \cap K_2 = F$, then $$\text{Gal}(K_1K_2/F)\cong \text{Gal}(K_1/F)\times \text{Gal}(K_2/F).$$Conversely, if $K$ is Galois over $F$ and $\text{Gal}(K/F) = G_1\times G_2$ is the direct product of two subgroups $G_1$ and $G_2$, then $K$ is the composite of two Galois extensions $K_1$ and $K_2$ of $F$ with $K_1\cap K_2 = F$. 

**Cor:** Let $E/F$ be any finite separable extension. Then $E$ is contained in an extension $K$ which is Galois over $F$ and is minimal in the sense that in a fixed algebraic closure of $K$ any other Galois extension of $F$ containing $E$ contains $K$. 

**Def:** Let $E/F$ be any finite separable extension. Fix an [[Algebraic Closure of a Field|algebraic closure]] $\overline F$ fo $F$. The *Galois closure* of $E/F$ is the smallest subfield $K\subseteq \overline F$ such that 
- $E\subseteq K$
- $K/F$ is a Galois extension.
- If $L/F$ is any Galois extension $\overline F$ with $E\subseteq L$, then $K \subseteq L$. 

**Prop:** Let $K/F$ be a finite extension. Then $K = F(\theta)$ iff there exists only finitely many subfields of $K$ containing $F$.

**The Primitive Element Theorem:** If $K/F$ is finite and separable, then $K/F$ is simple. In particular, any finite extension of fields of characteristic $0$ is simple.

**Prop:** Let $f(x)\in F[x]$ be an irreducible polynomials of degree $b$ over the field $F$, let $L$ be the splitting field of $f(x)$ over $F$ and let $\alpha$ be a root of $f(x)$ in $L$. If $K$ is any Galois extension of $F$, then the polynomial $f(x)$ splits into a product of $m$ irreducible polynomials each of degree $d$ over $K$, where $d = [K(\alpha): K] = [(L \cap K)(\alpha): L \cap K]$ and $m = n/d = [F(\alpha)\cap K : F]$. 

**Prop:** Let $L/K$ and $K/F$ are $p$-extensions, then the Galois closure of $L/F$ is also a $p$-extension. 