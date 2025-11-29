---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Polynomials in Several Variables over a Field]]

**Def:** Two field extensions $L/F$ and $K/k$ are *isomorphic* is there exists a pair of field isomorphisms $\phi: L \to K$ and $\psi: F \to k$ such that the following diagram commutes 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
L\arrow[r, "\phi"]\arrow[d, dash] & K\arrow[d, dash]\\
F\arrow[r, "\psi"] & k
\end{tikzcd}
\end{document}
```
meaning, $\phi|_F = \psi$. 

**Def:** An *isomorphism* between two extension $L/F$ and $K/F$ over the same field, is an field isomorphism $\phi: L \to K$ such that $\phi|_F = \text{id}_F$, i.e., the following diagram commutes
```tikz
\usepackage{tikz-cd} 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
L\arrow[r, "\phi"]\arrow[d, dash] & K\arrow[d, dash]\\
F\arrow[r, "\text{id}_F"] & F
\end{tikzcd}
\end{document}
```
In particular, it means that $\phi$ fixes $F$. 

**Th:** If $F(\alpha)/F$ and $F(\beta)/F$ are two algebraic simple extensions of $F$ and $\text{Irr}(\alpha, F) = \text{Irr}(\beta, F)$, then there exists a isomorphism between the two extensions, furthermore, the isomorphism can be chosen such that it maps $\alpha$ to $\beta$. 

**Th:** Let $\psi: K \to L$ a field isomorphism and let $K(\alpha)/K$ and $L(\beta)/L$ simple algebraic extensions. Let $m_\alpha(x) := \text{Irr}(\alpha, K)$ and $m_\beta(x) :=\text{Irr}(\beta, L)$ be the corresponding irreducible monic polynomials. If we consider the ring isomorphism $\widehat\psi: K[x] \to L[x]$ induced by $\psi$, and if $\widehat\psi(m_\alpha(x)) = m_\beta(x)$, then there exists a field isomorphism $\phi: K(\alpha) \to L(\beta)$ such that $\phi|_K =\psi$, and $\phi(\alpha) = \beta$. 
```tikz
\usepackage{tikz-cd} 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
K(\alpha)\arrow[r, dashed, "\phi"]\arrow[d, dash] & L(\beta)\arrow[d, dash]\\
K\arrow[r, "\text{id}_F"] & L
\end{tikzcd}
\end{document}
```


**Prop:** If $F$ is a field, then $F(x)/F$ is a simple transcendental extension, where $F(x)$ represents the field of rational functions on $x$ with coefficients in $F$.

**Th:** Every simple transcendental extension $F(\alpha)/F$ is isomorphic to the extension $F(x)/F$ of rational functions over $x$. Furthermore, the isomorphism can be taken such that it maps $x$ to $\alpha$. 

**Obs:** This gives the equivalence that a field extension is finite iff it is algebraic and finitely generated.

**Def:** Let $K/F$ be an extension $\alpha_1, \dots, \alpha_n\in K$ transcendental over $F$. We say that $\alpha_1,\dots,\alpha_n$ are *algebraically independent over $F$* if there is no nonzero polynomial $p\in F[x_1,\dots, x_n]$ such that $$p(\alpha_1,\dots, \alpha_n) = 0.$$Otherwise, we say that are *algebraically dependent.*

**Prop:** If $L/F$ is a finitely generated field extension, then there's an intermediate field $F\subseteq K \subseteq L$ such that:
- $K = F(\alpha_1,\dots, \alpha_r)$ where $\alpha_j$ are transcendental elements that are algebraically independent over $F$
- $L/K$ is a finite extension.

**Steinitz Theorem:** Let $L/F$ is a finitely generated field extension. We know that there's an intermediate field $F \subseteq K \subseteq L$ such that $K = F(\alpha_1,\dots, \alpha_r)$ where each $\alpha_j$ is transcendental element and $\alpha_1,\dots, \alpha_r$ are algebraically independent over $F$, and $L/K$ is a finite extension. If there is another intermediate field $K' = F(\beta_1,\dots,\beta_s)$ such that the elements $\beta_i$ are transcendental and algebraically independent over $F$ and $L/K'$ is a finite extension, then $r =s$. 

**Def:** Let $L/F$ be a finitely generated field extension. Let $K = F(\alpha_1,\dots,\alpha_r)$ such that $L/K$ is a finite extension and $\alpha_1,\dots, \alpha_r$ are algebraically independent over $F$. The integer $r\ge 0$ is called the *degree of transcendence* of the extension $L/K$, and is denoted as $$\text{tr. deg.}(L/F):= r.$$
**Def:** Let $E/F$ be any finite separable extension. The Galois extension $K$ of $F$ containing $E$ is called the *Galois closure* of $E$ over $F$. 

**Prop:** Let $K/F$ be a finite extension. Then $K = F(\theta)$ iff there exists only finitely many subfields of $K$ containing $F$.

**The Primitive Element Theorem:** If $K/F$ is finite and separable, then $K/F$ is simple. In particular, any finite extension of fields of characteristic $0$ is simple.

