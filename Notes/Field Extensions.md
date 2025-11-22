---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Rings and Fields]], [[Characteristic of a Ring]], [[Ring Homomorphisms]]

**Prop:** Let $\varphi: F \to K$ be a homomorphism of fields. Then $\varphi$ is either identically $0$ or is injective, so that image is either $0$ or isomorphic to $F$. 

**Def:** A *field extension* is a field monomorphism $\phi: F \to K$. 

We see that if there's a monomorphism $\phi: F \to K$, then $F$ is embedded in $K$, so we can treat it as if it was a subset of $K$. Additionally, if $F\subseteq K$, then the monomorphism is the injection, thus it is also a field extension. 

**Def:** If $F$ and $K$ are fields such that $F \subseteq K$ and the operations $(+, \cdot)$ of $F$ are the sames as the ones in $K$, then we say that $F$ is a *subfield* of $K$ or, equivalently, $K$ is an *extension* of $F$. 

If $F\subseteq K$ is a field extension, we also use the notation $K/ F$, $K: F$, and 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}    
 & K \arrow[dash]{d} \\
 & F
\end{tikzcd}
\end{document}
```

**Def:** The *degree*, or *relative degree*, or *index* of a field extension $K/F$, denoted $[K: F]$, is the dimension of $K$ as a vector space over $F$, i.e., $[K: F] := \text{dim}_F K$. The extension is said to be *finite* if $[K:F]$ is finite and is said to be *infinite* otherwise. 

**Th:** If $L/K$ and $K/F$ are finite field extensions, then $L/F$ is a finite field extension, and $[L: F] = [L: K] [K:F]$. 

**Cor:** If $L/F$ is a finite extension, and $K$ is an intermediate field, i.e., $F\subseteq K \subseteq L$, then $[K: F]$ divides $[L:F]$. 

**Obs:** We see that a field is in particular an integral domain, thus their characteristic is either prime or $0$. 

**Def:** Let $F$ be a field, and $\{L_\alpha \mid \alpha < \kappa\}$ be the set of all subfields of $F$. We define the *prime subfield of $F$* to be $$\bigcap_{\alpha < \kappa} L_\alpha.$$
**Prop:** Let $F$ be field with prime subfield $K$. The following statements are true.
- If $F$ has characteristic $0$, then $K \cong \Bbb Q$. 
- If $F$ has nonzero characteristic, then $K \cong \Bbb Z/p\Bbb Z$. 

**Def:** Let $K/F$ be a field extension and a subset $X\subseteq K$. Let $\mathcal F :=\{ L \subseteq K \mid L/F \text{ is a field extension and } X\subseteq L\}$. Note that $\mathcal F \neq \varnothing$, since $X\in \cal F$. The subfield $F(X) := \bigcap \cal F$, and is called the field obtained by *adjoining $X$* to $F$. 

We see that $F \subseteq F(X)\subseteq K$, and $F(X)$ is the *smallest field* of $K$ that contain $F$ and $X$. If $X = \{a_1,\dots, a_n\}\subseteq K$ is finite set, then we use the notation $$F(X) = F(a_1,\dots, a_n). $$In particular, if $X = \{a\}\subseteq K$, we say that is a *simple extension* $F(a)/F$. 

**Prop:** Let $K/F$ a field extension and $\alpha \in K$. If $F(\alpha)/F$ the simple extension obtained by adjoining $\alpha$ to $F$. Then $$F(\alpha) = \left\{\left.\frac{f(\alpha)}{g(\alpha)}\; \right\rvert\; f(x), g(x)\in F[x], g(\alpha) \neq 0\right\} $$
