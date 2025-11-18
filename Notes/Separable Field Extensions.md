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

**Prop:** Every irreducible polynomial over a finite field $F$ is separable. A polynomial if $F[x]$ is separable iff it is the product of distinct irreducible polynomials in $F[x]$. 

**Def:** If $L/F$ is a field extension, an algebraic element $\alpha\in L$ over $F$ is called *separable over $F$*, if $\text{Irr}(\alpha, F)\in F[x]$ is separable. The extension $L/F$ is called *separable* if every $\alpha\in L$ is separable over $F$. An arbitrary polynomial $f(x)\in F[x]$ is called *separable over $F$* is all of its irreducibles factors are separable over $F$. A field extension which is not separable is *inseparable*. 

**Prop:** Let $L/F$ be an algebraic separable extension. If $F \subseteq K \subseteq L$ is an intermediate field, then the subextensions $L/K$ and $K/F$ are also separable. 

**Def:** A field $K$ of characteristic $p$ is called *perfect* if every element of $K$ is a $p$th power in $K$, i.e., $K = K^p$. Ant field of characteristic $0$ is also called perfect.

**Cor:** Every finite extension of a perfect field is separable. In particular, every finite extension of either $\Bbb Q$ or a finite field. 

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
