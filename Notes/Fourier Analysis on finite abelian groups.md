---
tags:
  - FourierAnalysis
  - GroupTheory
---
Subjects: [[Fourier Analysis]], [[Group Theory]]
Links: [[Fourier Analysis on Z(N)]], [[Group Homomorphisms and Isomorphisms]]

Let $G$ be a finite abelian group, and $\Bbb S^1$ the unit circle on the complex plane. A *character* on $G$ is a group homomorphism $e: G \to \Bbb S^1$. The *trivial* or *unit character* is defined by $e \equiv 1$.

If $G$ is a finite abelian group, we denote by $\hat G := \text{Hom}(G, \Bbb S^1)$, the set of all characters.

**Prop:** $\widehat{\Bbb Z(N)} \cong \Bbb Z(N)$

**Lemma:** The set $\hat G$ is an abelian group under multiplication defined by $$(e_1 \cdot e_2)(a) = e_1(a) e_2(a) \qquad \forall a \in G$$
**Lemma:** Let $G$ be a finite abelian group, and $e: G\to \Bbb C\setminus \{0\}$ a multiplicative function, namely $e(a\cdot b) = e(a) e(b)$ for all $a. b\in G$. Then $e$ is a character.

**Prop:** Let $G_1$ and $G_2$ be groups, then $\widehat{G_1\times G_2} \cong \hat G_1 \times \hat G_2$.

**Th:** If $G$ is a finite abelian group, then $G \cong \hat G$, this is using the fact that finite abelian groups can be decomposed as the product of cyclic groups. 

Let $V$ denote the vector space of all complex-valued function defined on the finite abelian group $G$, $\Bbb C^G$. Note that the dimension of $V$ is $|G|$. We define the inner product on $V$ by $$(f, g) = \frac1{|G|} \sum_{a \in G} f(a)\overline{g(a)} \qquad f, g\in V$$
**Lemma:** If $e$ is a non-trivial character of the group $G$, then $$\sum_{a\in G} e(a) = 0$$
**Th:** The characters of $G$ form an orthonormal family with respect to the inner product defined above.

We see that characters are linearly independent, and thus $|\hat G| \le |G|$

**Lemma:** Suppose $\{T_1, \dots, T_k\}$ is a commuting family of unitary transformations on the finite-dimensional inner product space $V$; that is $$T_i T_j = T_j T_i \qquad \forall i, j \in \{1, \dots k\}$$Then $T_1, \dots, T_k$ are simultaneously diagonalizable. In other words, there exists a basis for $V$ which consists of eigenvectors for every $T_i$, $i \in \{1, \dots, k\}$. This is a generalisation of the [[Orthogonal Projections and Spectral Theorem#The Spectral Theorem|the spectral theorem]].

**Th:** The characters of a finite abelian group $G$ form a basis for the vector space of functions on $G$. 

Meaning that $|G| = |\hat G|$. 

**Def:** Given a function $f$ on $G$, a finite abelian group, and a character $e$ of $G$, we define the *Fourier coefficient* of $f$ with respect to $e$, by $$\hat f (e) = (f, e) = \frac1{|G|} \sum_{a\in G} f(a)\overline{e(a)}$$and the *Fourier series* of $f$ as $$ f \sim \sum_{e \in \hat G} \hat f(e) e$$
**Th:** Let $G$ be a finite abelian group. The characters of $G$ form an orthonormal basis for the vector space $\Bbb C^G$  equipped with the inner product $$(f, g) = \frac1{|G|} \sum_{a \in G} f(a)\overline{g(a)} \qquad f, g\in V$$in particular, any function $f$ on $G$ is equal to its Fourier series $$ f = \sum_{e \in \hat G} \hat f(e) e$$
**Th:** If $f$ is a function on $G$, then $$\|f\|^2 = \sum_{e \in \hat G}|\hat f(e)|^2$$
We can define the convolution of two function $f$ and $g$ in $\Bbb C^G$ is defined for each $a \in G$ by $$(f*g)(a) := \frac1{|G|} \sum_{b \in G} f(b)g(b^{-1}\cdot a)$$
We have the nice property that for all $e \in \hat G$, we have that $$\widehat{(f*g)}(e) = \hat f (e) \hat g(e)$$
We can get the result that for a $c\in G$, such that $c$ is not the identity of $G$, we get $$\sum_{e \in \hat G}e(c) = 0$$
We define $D$, on $G$ as $$D(c) = \sum_{e \in \hat G} e(c) = \begin{cases}|G| & c = 1_G \\ 0 & c \ne 1_G\end{cases}$$
And we have $f*D = f$. Making $D$ have a similar role as the "Dirac delta function", since it has unit mass $$\frac1{|G|}\sum_{c \in G}D(c) = 1$$and it is concentrated at the unit element in $G$.