---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Galois Field Extensions]], [[Polynomial Ring of a Single Variable]], [[Symmetric Groups]], [[Splitting Fields and Normal Field Extensions]]

**Def:** If $f(x) \in F[x]$ is a separable polynomial, then we define the Galois group of $f(x)$ to be the Galois group of the splitting field of $f(x)$ over $F$. 

If $K/F$ is a Galois extension, the $K$ is the splitting filed for some separable polynomial $f(x)\in F[x]$. Any $F$-automorphism $\sigma\in \text{Gal}(K/F)$ maps a root of an irreducible factor of $f(x)$ to another root of the irreducible factor and $\sigma$ is uniquely determined by its action on these roots. If we fix a labelling of the roots $\alpha_1,\dots, \alpha_n$ , hence defines a unique permutation of the subscripts $\{1,2,\dots, n\}$. This gives us an injection $$\text{Gal}(K/F) \hookrightarrow S_n $$of the Galois group into the symmetric group of $n$ letters. This means that we can think of Galois groups as subgroups of $S_n$, and gives a group theoretic explanation on why the splitting fields for a polynomial of degree $n$ over $F$ is of degree at most $n!$ over $F$.

If $f(x)$ is irreducible, then given two roots of $f(x)$ there is an $F$-automorphism in the Galois group of $f(x)$ which maps the first root to the second. Such a group is said to be *transitive* on the roots, i.e., the Galois group of $f(x)$ [[Group Actions#Types of Actions|acts transitively]] on the roots. 

**Def:** Let $x_1,x_2, \dots, x_n$ be indeterminates. The *elementary symmetric functions* $s_0, s_1, \dots, s_n$ are defined $$\begin{align*}
s_0&:= 1\\
s_1 &:= x_1 + x_2+ \dots +x_n \\
s_2 &:= x_1x_2 + x_1x_3+ \dots + x_2x_3 +x_2x_4 + \dots +x_{n-1}x_n\\
&\vdots \\
s_n &:= x_1x_2\cdots x_n.
\end{align*}$$