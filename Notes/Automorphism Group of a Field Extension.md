---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Automorphism Group]], [[Classification of Simple Field Extensions]]

An *isomorphism* between two extension $L/F$ and $K/F$ over the same field, is an field isomorphism $\phi: L \to K$ such that $\phi|_F = \text{id}_F$, i.e., the following diagram commutes
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
In particular, it means that $\phi$ fixes $F$. Thus, an automorphism of field extension $K/F$, is a field automorphism $\phi: K \to K$ such that $\phi|_F = \text{id}_F$, i.e., a field automorphism of $K$ that leave $F$ fixed. The automorphisms of the field extension $K/F$ are called *$F$-automorphisms of $K$.* 

**Obs:** If $K/F$ is a field extension, then the set of $F$-automorphisms of $K$, denoted $\text{Aut}(K/F)$ is a group, and it is a subgroup of $\text{Aut}(K)$. 

**Def:** Let $L/K$ and $K/F$ be a field extensions. I am gonna use the notation $$S(K) := \text{Aut}(L/K) \le \text{Aut}(L/F),$$to denote the subgroup $\text{Aut}(L/F)$ associated with the intermediate field $K$. We have the function $$S: \mathcal F_{L/F}:=\{\text{Intermediate fields of }L/F\}\to \mathcal G_{L/F}:=\{\text{Subgroups of }\text{Aut}(L/F)\}.$$
We have the following properties of this function $S$.

**Prop:** The function $S: \mathcal C_{L/F} \to \mathcal G_{L/F}$ satisfies the following:
- If $M_1\subseteq M_2$ are intermediate fields, then $S$ flips the inclusions, i.e., $S(M_2)\subseteq S(M_1).$
- For the intermediate field, $M = F$, we have that $S(M) = \text{Aut}(L/F)$ is the total group.
- For the intermediate field $M = L$, we have that $S(L) = \text{Aut}(L/L) = \{\text{id}_L\}$ is the trivial subgroup.

Given a subgroup $H$ of the group $G = \text{Aut}(L/F)$ we would like to associate it with an intermediate field of $L/F$. 

Let us observer that $\text{Aut}(L)$ [[Group Actions|acts naturally]] on $L$, since the action is just $(\sigma, \alpha) \in \text{Aut}(L) \times L \mapsto \sigma(\alpha)\in L$. This means that if $L/F$ is a field extension, then $\text{Aut}(L/F)$ also acts naturally on the extension $L/F$, by the same action. 

Given $H\le \text{Aut}(L/F)$ let $$L^H := \{a\in L \mid a\in \forall \sigma\in H(\sigma(a) = a) \},$$meaning, $L^H$ is the subset of $L$ that ate fixed by all the elements of $H \le\text{Aut}(L/F)$. This is just the $H$[[Group Actions#^7f0380|-fixed points]] of $L$. 

**Lemma:** If $H\le \text{Aut}(L/F)$, then $L^H$ is an intermediate field of $L/F$. 

**Def:** If $H\le \text{Aut}(L/F)$, then $L^H$ is called the *fixed field* of the subgroup $H\le \text{Aut}(L/F)$. We have the function $$ F: \mathcal G_{L/F}\to \mathcal C_{L/F}$$ which for every subgroup $H$ of $\text{Aut}(L/F)$ we associate its corresponding fixed field $F(H) := L^H$. 

**Lemma:** The function $F: \mathcal G_{L/F}\to \mathcal C_{L/F}$ satisfies the following:
- If $H_1 \le H_2$ be subgroups of $\text{Aut}(L/F)$, then $F$ flips inclusions, i.e., $F(H_1)\supseteq F(H_2)$. 
- If $H \le \text{Aut}(L/F)$, then $H \le S(F(H))$. 
- If $M$ is an intermediate field of $L/F$, then $M \subseteq F(S(M))$. 

**Dedekind theorem:** Let $F$ be a field. Then, any finite set of distinct automorphisms $\sigma_1,\dots,\sigma_n: F \to F$ are linearly independent. Meaning, if $a_1\sigma_1(x) + a_n\sigma_n(x) = 0$ for all $x\in F$, then $a_i = 0$ for all $i\in\{1,\dots, n\}$. 

**Cor:** If $L/F$ is a finite field extension, then $|\text{Aut}(L/F)|\le [L:F]$. 

# Normal and Separability

**Th:** Let $G = \{\sigma_1,\dots, \sigma_n\}$ is a finite group of automorphisms of a field $L$ and $L^G$ is the fixed field of $G$, then $$[L: L^G]= |G| = n.$$
**Artin Theorem:** Let $G$ be a subgroup of a finite automorphism group of a field $L$. If $L^G$ is the fixed field of $G$, then $\text{Aut}(L/L^G) = G$. 

**Cor:** Let $L$ be a field. The function $F$, that assigns each finite subgroup $G$ of $\text{Aut}(L)$ to $L^G,$ is injective.

The results above show that the importance for a finite extension $L/F$ is to have that $F = L^G$ is the fixed field of the group $\text{Aut}(L/F)$. 

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

**Def:** An irreducible polynomial $f(x)\in F[x]$ is called *separable* over $F$ if it has no multiple roots in its splitting field, An irreducible polynomial $f(x) \in F[x]$ is called *inseparable* over $F$ if it is not separable. 

**Lemma:** Let $F$ be a field. A nonzero polynomial $f(x)\in F[x]$, with a multiple root in the splitting field iff $f$ and $f'$ have a factor of degree $n \ge 1$ in $F[x]$. 

**Cor:** Let $F$ be a field and $f(x) \in F[x]$ irreducible.
- If $F$ has characteristic $0$, then $f(x)$ is separable over $F$.
- If $F$ has characteristic $p\ne 0$, then $f(x)$ is inseparable iff $f(x)$ is of the form $f(x) = g(x^p)$ with $g(x)\in F[x]$. This last condition means that the all the powers of $x$ that appear in $f(x)$ are only the one that correspond with a integer multiple of $p$. 

**Def:** If $L/F$ is a field extension, an algebraic element $\alpha\in L$ over $F$ is called *separable over $F$*, if $\text{Irr}(\alpha, F)\in F[x]$ is separable. The extension $L/F$ is called *separable* if every $\alpha\in L$ is separable over $F$. An arbitrary polynomial $f(x)\in F[x]$ is called *separable over $F$* is all of its irreducibles factors are separable over $F$. 

**Prop:** Let $L/F$ be an algebraic separable extension. If $F \subseteq K \subseteq L$ is an intermediate field, then the subextensions $L/K$ and $K/F$ are also separable. 

**Th:** Let $L/F$ be a finite field extensions with automorphism group $G := \text{Aut}(L/F)$. The following statements are equivalent.
1. $L/F$ is normal and separable.
2. $L$ is the splitting field of a separable polynomials $p(x) \in F[x]$.
3. $F$ is the fixed field of $G$, i.e., $F = L^ G$.

The proof is as follows:

To show normality, let $f(x) \in F[x]$ be irreducible with a root $\alpha \in L$. Then $f(x) = \mathrm{Irr}(\alpha,F)$, and its other roots are the conjugates $\sigma(\alpha)$ for $\sigma \in G$, all of which lie in $L$. Therefore $f(x)$ splits in $L$, and the extension is normal.

$1) \Rightarrow 2)$. If $L/F$ is a finite, separable, and normal extension then $L$ we know that $L$ is a finitely generated algebraic extension. Let $L = F(\alpha_1,\dots, \alpha_n)$. We know that each $\alpha_i$ is separable over $F$, and the polynomials $p_i(x) := \text{Irr}(\alpha_i, F)\in F[x]$ are also separable over $F$. If we let $p(x) = p_1(x) \cdots p_n(x)\in F[x]$. Since each $p_i(x) \in F[x]$ are separable and irreducible, then $p(x)$ is also separable, and it decomposes in $L$. We see that $L$ is actually the splitting field of the separable polynomial $p(x)$.

$2) \Rightarrow 3)$ Let $p(x)$ be a separable polynomial and $L$ be the splitting field of $p(x)$. The proof relies on induction over the number of roots in $L\setminus F$. The base case is fairly trivial. If there are no roots in $L\setminus F$, that means that $F = L = L^{\text{Aut}(L/F)}$. 

The induction hypothesis is a little convoluted. Let $p(x)$ have $n$ roots in $L\setminus F$, and for any intermediate field $K$
```tikz
\usepackage{tikz-cd} 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}  
L\arrow[dr, dash]\arrow[dd, dash] \\
& K\arrow[dl, dash] \\
F 
\end{tikzcd}
\end{document}
```
when we see $p(x)$ inside $K[x]$, has less than $n$ roots in $L \setminus K$, we have that $$K = L^{\text{Aut}(L/K)}.$$
When we decompose $p(x) = p_1(x) \cdots p_r(x)$ is its decomposition into irreducibles in $F[x].$We know that if every $p_i(x)$ are linear, then we would contradict the fact that there are roots outside of $F$. Without loss of generality, let $p_1(x)$ be of degree $s > 1$. Since $p(x)$ is separable, thus $p_1(x)$ must also be separable. Let $\alpha_1,\dots, \alpha_s\in L \setminus F$ be distinct roots of $p_1(x)$. We can now interpret $p(x) \in F[x] \subseteq F(\alpha_1)[x]$, and $L$ is still the splitting field of $p(x)$ with $p(x)$ has less than $n$ roots in $L\setminus F(\alpha_1)$. By the induction hypothesis, we have that $$F(\alpha_1) = L^{\text{Aut}(L/F(\alpha_1))}.$$
We now consider the extensions  
```tikz
\usepackage{tikz-cd} 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}  
L\arrow[d, dash]\arrow[rr, dashed, "\sigma_i"] && L\arrow[d, dash] \\
F(\alpha_1)\arrow[dr, dash]\arrow[rr, dashed, "\tilde\sigma_i"] && F(\alpha_i)\arrow[dl, dash]\\
& F&
\end{tikzcd}
\end{document}
```
We know that there's a field extension isomorphism $\tilde \sigma_i$ between $F(\alpha_1)/F$ and $F(\alpha_i)/F$ since $\text{Irr}(\alpha_i, F) = \text{Irr}(\alpha_1, F)$ for every $i\in \{1,\dots, s\}$. Notice hat by properties of the splitting field, we have that the $\tilde\sigma_i$ can be extended to a $F$-automorphism $\sigma_i:L \to L$ that fixes $F$. We only need to show that $F = L^{\text{Aut}(L/F)}.$ 

If $\theta\in L^{\text{Aut}(L/F)}$, then $\theta\in L^{\text{Aut}(L/F(\alpha_1))} = F(\alpha_1)$. Since $1,\alpha_1, \dots,\alpha^{s-1}_1$ are a base for $F(\alpha_1)$ as an $F$-vector space, then $\theta = \sum_{k < s} c_k \alpha^k_1$ with $c_k \in F$. If we apply $\sigma_i$, we know that $$\theta = \sigma_i(\theta) = \sum_{k < s} c_k \alpha^k_i$$for each $1  \le i \le s$. The polynomial $$q(x) = c_0 - \theta + c_1x+\dots c_{k-1}x^{k-1}\in F(\alpha)[x] $$has degree at most $s-1$, and $s$ distinct roots. This means that $q(x) = 0$, and in particular $c_0 - \theta = 0$, equivalently, that $c_0 = \theta \in F$.

$3) \Rightarrow 1)$ We will first show that $L/F$ is separable. Let $\alpha\in L$. If we consider the polynomial $$p(x) := \prod_{\sigma \in \text{Aut}(L/F)} (x-\sigma(\alpha))\in L[x], $$then we see that for any $\sigma\in \text{Aut}(L/F)$, $\sigma(p(x)) = p(x)$. By our hypothesis, this implies that $p(x) \in F[x]$, and it is monic. We have constructed a sepable polynomial $p(x)\in F[x]$ such that $\alpha$ is a root. This also implies that $\text{Irr}(\alpha. F)$ is separable, since it must divide $p(x).$
 We can show a little bit more, that in fact, $p(x) = \text{Irr}(\alpha, F)$. If $g(x)\in \text{Irr}(\alpha, F)$ is a polynomial with $\alpha$ as its root, then $$0 = \sigma(g(\alpha)) = g(\sigma(\alpha)).$$ for every $\sigma \in  \text{Aut}(L/F)$, hence $p(x)$ must divide $g(x)$. In particular, if $g(x) = \text{Irr}(\alpha, F)$, then $p(x) = \text{Irr}(\alpha, F)$ since they both are monic. 

To show that $L/F$ is a normal extension, let $f(x) \in F[x]$ be a irreducible polynomials that has $\alpha\in L$ as its root. We know that $\text{Irr}(\alpha, F)$ is splits in $L$. Lastly, this implies that $f(x) \mid \text{Irr}(\alpha, F)$ and $\text{Irr}(\alpha, F) \mid f(x)$ in $F[x]$, and that $f(x)$ is a constant multiple of $\text{Irr}(\alpha, F)$, and hence split on $L$. 

# The Fundamental Theorem of Galois Theory

**Def:** If $L/F$ is a finite, separable and normal extension, we call it a *Galois extension.* Additionally, the automorphism group $\text{Aut}(L/F)$ is known as the *Galois group of the extnesion* and it is denoted $\text{Gal}(L/F)$. 

**Lemma:** Let $M/F$ be finite extension. The following are statements are equivalent.
- $M/F$ is normal.
- For any field extension $L/M$ such that $L/F$ is a normal and finite extension we have that every monomorphism $\tau: M \to L$ that leaves $F$ fixed and is, an $F$-automorphism $\tau: M\to M$. 

**Lemma:** Let $L/F$ be a Galois extension, and $M$ be an intermediate field. If $\tau\in \text{Gal}(L/F)$, then $$\text{Gal}(L/\tau[M]) = \tau\text{Gal}(L/M)\tau^{-1}$$
**Fundamental Theorem of Galois Theory:** Let $L/F$ be a Galois extension, and $G = \text{Gal}(L/F)$. Then:
- $|\text{Gal}(L/F)| = [L: F]$
- The functions $F: \mathcal G_{L/F} \to \mathcal F_{L/F}$ and $S : \mathcal F_{L/F} \to \mathcal G_{L/F}$ are inverses of each other.
- If $M$ is an intermediate field, $F \subseteq M \subseteq L$, then
	- $|S(M)| = |\text{Gal}(L/M)| = [L:M]$
	- $[M:F] = |\text{Gal}(L/F)|/|S(M)| = [\text{Gal}(L/F): S(M)]$. 
- If $M$ is an intermediate field, $F \subseteq M \subseteq L$, then $M/F$ is normal iff $\text{Gal}(L/M) \trianglelefteq \text{Gal}(L/F)$, meaning that $\text{Gal}(L/M)$ is a normal subgroup of $\text{Gal}(L/F).$
- If $M$ is an intermediate field, and the extension $M/F$ is normal, then the Galois group $\text{Gal}(M/F)$ is isomorphic to the quotient group $\text{Gal}(L/F) /\text{Gal}(L/M)$.

The proof of the last point of the fundamental theorem of Galois theory actually relies on the [[Group Homomorphisms and Isomorphisms#^ff5e58|first isomorphism theorem for groups]], 

This theorem, actually gives us the *Galois correspondence* between subgroups of $\text{Gal}(L/F)$ and intermediate fields of the extension $L/F$.