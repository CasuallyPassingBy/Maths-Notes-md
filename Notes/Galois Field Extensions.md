---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Automorphism Group of a Field Extension]], [[Splitting Fields and Normal Field Extensions]], [[Separable Field Extensions]]

**Def:** If $L/F$ is a separable and normal extension, we call it a *Galois extension.* Additionally, the automorphism group $\text{Aut}(L/F)$ is known as the *Galois group of the extension* and it is denoted $\text{Gal}(L/F)$. 

**Def:** Let $L/F$ be a Galois extension. If $\alpha\in K$ the elements $\sigma(\alpha)$ for $\sigma\in \text{Gal}(L/F)$ are called *Galois conjugates* of $\alpha$ over $F$. If $E$ is subfield of $L$ containing $F$, the field $\sigma[E]$ is called the *conjugate field* of $E$ over $F$. 

**Th:** Let $L/F$ be a finite field extensions with automorphism group $G := \text{Aut}(L/F)$. The following statements are equivalent.
1. $L/F$ is a Galois extension. 
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

**Def:** If $f(x)$ is s separable polynomial over $F$, then the *Galois group of $f(x)$ over $F$* is the Galois group of the splitting field of $f(x)$ over $F$. 

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
- If $M_1$ and $M_2$ correspond to $H_1$ and $H_2$, respectively, then the intersection $M_1 \cap M_2$ correspond to the group $\langle H_1, H_2\rangle$ generated by $H_1$ and $H_2$ and the [[Composite Field Extensions|composite field]] $M_1 M_2$ correspond to the intersection $H_1\cap H_2$. Hence, the lattice of intermediate fields of $L/F$ and the lattice of subgroups of $G$ are 'dual' (the lattice diagram for one is the lattice diagram for the other turned upside down). 

The proof of the last point of the fundamental theorem of Galois theory actually relies on the [[Group Homomorphisms and Isomorphisms#^ff5e58|first isomorphism theorem for groups]], 

This theorem, actually gives us the *Galois correspondence* between subgroups of $\text{Gal}(L/F)$ and intermediate fields of the extension $L/F$. ^5c8efc

**Prop:** Let $f(x) \in F[x]$ be a an irreducible polynomial of degree $n$ over the field $F$, $L$ be the splitting field of $f(x)$ over $F$ and $\alpha$ be a root of $f(x)$ in $L$. If $K/F$ is a finite Galois extension contained in $L/F$, then the polynomial $f(x)$ splits into a product of $m$ irreducible polynomials each of degree $d$ over $K$, where $m = [F(\alpha) \cap K : F]$, and $d = [K(\alpha): K]$. 