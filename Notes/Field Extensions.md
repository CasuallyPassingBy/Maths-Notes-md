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
**Def:** Let $K/F$ be a field extension. An element $\alpha\in K$ is called an *algebraic extension* over $F$, if there exists a polynomial $p(x)\in F[x]\setminus\{0\}$, such that $p(\alpha) = 0$. Otherwise, we say that $\alpha$ is *transcendental over $F$*.  

**Obs:** Let $K/F$ be a field extension and $\alpha\in K$ be transcendental over F, then $f(\alpha)\in K$ is also transcendental over $F$ for every $f(x)\in F[x]$. 

**Lemma:** The monic polynomial with minimal degree $m(x)\in F[x]$ such that $\alpha\in K$ is a root is unique. Furthermore, $m(x)$ is irreducible in $F[x]$, and $m(x)$ divides any other polynomial $p(x)\in F[x]$ with $\alpha$ as one of its roots.

**Def:** The *irreducible monic polynomial* $m(x)\in F[x]$ with minimal degree such that $\alpha\in K$ is a roof, is called the *minimal polynomial* of $\alpha$, and can be denoted as $\text{Irr}(\alpha, F)\in F[x]$. 

**Obs:** If $L/F$ is  field extension and $\alpha$ is algebraic over both $F$ and $L$, then $\text{Irr}(\alpha, L) \mid \text{Irr}(\alpha, F)$ in $L[x]$. 

**Prop:** Let $\alpha\in K$ algebraic over $F$ and $m(x) := \text{Irr}(\alpha, F)\in F[x]$. Then $$F(\alpha) = \{p(\alpha) \mid p(x) \in F[x], \text{deg}(p(x)) < \text{deg}(m(x))\}\cong F[x]/(\text{Irr}(\alpha, F)(x))$$
**Th:** Let $K/F$ a field extension, and $\alpha\in K$. Then, $\alpha$ is algebraic over $F$ iff the extension $F(\alpha)/F$ is finite. 

**Cor:** Suppose $F = \Bbb Q(\alpha_1,\dots, \alpha_n)$ where $\alpha_i^2 \in \Bbb Q$ for $i \in\{1,\dots, n\}$, then $\sqrt[3]{2}\notin F$. 

**Prop:** Let $F$ be a field and $F(\alpha) /F$ be a field extension. If $[F(\alpha): F]$ is odd, then $F(\alpha) = F(\alpha^2)$. 

**Cor:** If $\alpha\in K$ is algebraic over $F$, then $$[F(\alpha): F] = \text{deg}(\text{Irr}(\alpha, F)).$$
**Cor:** If $\alpha$ is algebraic over $F$, then every element of $F(\alpha)$ is algebraic over $F$. 

**Prop:** Let $F(\alpha)/F$ be a simple finite extension. Consider the function $\tilde\alpha: K(\alpha) \to K(\alpha)$ defined as $\tilde \alpha(x) = \alpha \cdot x$. Then $\tilde\alpha$ is a $K$-linear transformation, and $\phi(x) := \det(xI -\tilde \alpha)$ satisfies the equality $\text{Irr}(\alpha, F) = \phi(x)$. 

This fact is related to [[Rational or Frobenius Normal Form]] of linear transformations, and $\phi(x)$ is not the characteristic polynomial but the minimal polynomial of the companion matrix. 

**Th:** If $K/F$ be a finite field extension. If $[K: F] \le n$ then $K$ is isomorphic to a subfield of $\mathcal M_n(F)$. This means, that $\mathcal M_n(F)$ contains all the field extensions of degree less than $n$. 

**Def:** An field extension $K/F$ is called *algebraic* if all of the elements of $K$ are algebraic over $F$. 

**Cor:** Every finite field extension $K/F$ is algebraic, 

**Prop:** A field extension $K/F$ is finite iff it is algebraic and there is a finite number of elements $\alpha_1, \dots,\alpha_n \in K$ such that $K = F(\alpha_1,\dots, \alpha_n)$. 

**Obs:** This gives the equivalence that a field extension is finite iff it is algebraic and [[Classification of Simple Field Extensions#^e1f018|finitely generated]] by algebraic elements. 

**Cor:** Let $L/K$ be a finite extension. If $[L:K]$ is a prime number, then $L/K$ is a simple extension. 

**Th:** If $L/K$ and $K/F$ are algebraic extension, the $L/F$ is also an algebraic extension. 

**Cor:** Let $L/K$ be a field extension. If $\alpha_1,\dots,\alpha_n\in L$ are algebraic over $K$, then the extension $K(\alpha_1,\dots, \alpha_n) /K$ is algebraic. 

**Cor:** Let $L/F$ be a field extension, and $\Gamma\subseteq L$ be a set such that every $\alpha\in \Gamma$ is algebraic over $F$. Then $F(\Gamma)/F$ is an algebraic extension. 

**Prop:** Let $K/F$ be an algebraic extension. If $R$ is subring of $K$ that contains $F$, then $R$ is a field. This tells us that the intermediate rings of an algebraic extension are actually intermediate fields. 

**Prop:** $L/K$ be an algebraic field extension. If $K$ is countable, then so is $L$. 

**Lemma:** Let $K/F$ be a field extension. If $\alpha, \beta\in K\setminus \{0\}$ are algebraic over $F$, then $\alpha\pm\beta, \alpha \beta$ and $\alpha/\beta$ are algebraic over $F$. This means that the set $L\subseteq K$ of all the algebraic elements over $F$ is a field and $F\subseteq L$. 

**Kronecker:** Let $F$ be a field and $p(x) \in F[x]$ an irreducible monic polynomial over $F$. Then there's a field extension $K/F$, of degree $[K:F] = \text{deg}(f(x)) = n$, and $p(x)$ has a root $\alpha\in K$, and in fact, $p(x) = \text{Irr}(\alpha, F)$ and $K = F(\alpha)$. 

**Cor:** Let $F$ be a field and $f(x) \in F[x]$ a polynomial of degree $n \ge 1$. Them, there's a finite extension $K/F$ of degree at most $n!$ such that $f(x)$ has all of its roots in $K$. 

**Def:** Let $L/K$ be a field extension. An element $\alpha\in L$ is called an *algebraic of degree $n$* over $K$, if $\alpha$ is the root of a polynomial $f(x)\in K[x]$ of degree $n$, but it is not a root of a polynomial in $K[x]$ with degree less than $n$.

**Obs:** If $\alpha\in L$ is a algebraic element of degree $n$ over $K$, then $[K(\alpha), K] = n$. 

**Prop:** If $\alpha, \beta\in L$ are algebraic elements over $K$ with degrees $m$ and $n$, respectively, and $(m. n) = 1$, then $[K(\alpha, \beta): K] = mn$. 