---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Galois Groups of Polynomials]], [[Galois Field Extensions]], [[Cyclic Groups]], [[Cyclotomic Polynomials and Extensions]]

**Def:** *Simple radical extensions* are extensions obtained by adjoining to a field $F$ the $n$th root of an element $a$ in $F$. 

**Obs:** Since all the roots of the polynomial $x^n -a$ for $a\in F$ differ by factors fo the $n$th roots of unity, adjoining one such root will give a Galois extension iff this field contains the $n$th roots of unity. Simple radical extensions are best behaved when the base field $F$ already contains the appropriate roots of unity. The symbol $\sqrt[n] a$ for $a\in F$ is used to denote any root of the polynomial $x^n -a$. 

**Def:** The extension $K/F$ is said to be *cyclic* if it is Galois with a cyclic Galois group. 

**Prop:** Let $F$ be a field of characteristic not diving $n$ which contains the $n$th roots of unity. The extension $F(\sqrt[n] a)$ for $a\in F$ is cyclic over $F$ of degree dividing $n$. 

Let $K$ be any cyclic extension of degree $n$ over a field $F$ of characteristic not dividing $n$ which contains the $n$th roots of unity. Let $\sigma$ of the generator for the cyclic group $\text{Gal}(K/F)$. 

**Def:** For $\alpha\in K$ and any $n$th root of unity $\zeta$, we define the *Lagrange resolvent* $(\alpha, \zeta) \in K$ by $$(\alpha, \zeta) := \alpha + \zeta\sigma(\alpha) + \zeta^2\sigma^2(\alpha) +\dots + \zeta ^{n-1}\sigma^{n-1}(\alpha) = \sum_{k <n} \zeta^k\sigma^k(\alpha).$$
If we apply the automorphism $\sigma$ to $(\alpha, \zeta)$ we get that $$\sigma(\alpha, \zeta) = \zeta^{-1}(\alpha, \zeta).$$It follows that $$\sigma((\alpha, \zeta)^n) = (\alpha, \zeta)^n $$
We see that $(\alpha, \zeta)^n$ is fixed by $\text{Gal}(K/F)$, hence is an element of $F$ for any $\alpha\in K$. 

**Prop:** Any cyclic extension of degree $n$ over a field $F$ of characteristic not dividing $n$ which contains the $n$th roots of unity is of the form $F(\sqrt[n] a)$ for some $a\in F$. 

**Remark:** The two propositions above form a part of what is known as *Kummer theory.* A group $G$ is said to have *exponent* $n$ if $g^n = 1$ for every $g\in G$. Let $F$ be a field with characteristic not dividing $n$ which contains the $n$th roots of unity. If we take elements $a_1,\dots, a_k\in F^\times$ then we see that the extension $$ F(\sqrt[n]{ a_1},\dots, \sqrt[n]{a_k}) $$is an abelian extension of $F$ whose Galois group is of exponent $n$. Conversely, any abelian extension of exponent $n$ is of this form. 

**Def:** Such extensions as above are called *[[Kummer extensions]]*. 

If we want to examine what happens when $\text{char K} \mid n$, we need to consider the [[Artin-Schreier Extensions]]. 

**Def:** An element $\alpha$ which is algebraic over $F$ can be *expressed by radicals* or *solved for in terms of radicals* if $\alpha$ is an element of a field $K$ which can be obtained by a succession of simple radical extensions $$F = K_0 \hookrightarrow K_1 \hookrightarrow \cdots \hookrightarrow K_i \hookrightarrow K_{i+1} \hookrightarrow \cdots \hookrightarrow K_n = K$$where $K_{i+1} = K_i (\sqrt[n_i]{ a_i})$ for some $a_i \in K_i$, $i = 0, 1,\dots, n-1$. Here $\sqrt[n_i]{a_i}$ denotes some root of the polynomial $x^{n_i}-a_i$. such a field $K$ will be called a *root extension* of $F$.

A polynomial $f(x)\in F[x]$ can be *solved by radicals* if all its roots can be solved for in terms of radicals.

This gives us a precise meaning to the intuitive notion that $\alpha$ is obtained by successive algebraic operations and successive root extractions. 

In considering radical extensions one may always adjoin roots of unity, since by definition roots of unity are radicals. 

**Obs:** The composite of two root extensions is again a root extension. 

**Lemma:** If $\alpha$ is solved for in terms of radicals, then $\alpha$ is contained in a root extension which is Galois over $F$ and where each extension $K_{i+1}/K$ is cyclic. 

**Th:** The polynomial $f(x)$ can be solved by radicals iff its Galois group is [[Solvable Groups|solvable]].

This theorem gives us Galois' fundamental connection between solving roots of polynomials in terms of radical and the Galois group of the polynomial. 

**Cor:** The general equation of degree $n$ cannot be solved by radicals for $n \ge 5$. This is immediate since $S_n$, and $A_n$ are not solvable for $n \ge 5$. 

This corollary shows that there is nor formula involving radicals analogues to the quadratic formulas for polynomials of degree $2$ for the roots of a polynomial of degree $5$. 

## Cardano's Formula
Let us consider the cubic $$f(x) = x^3+ax^2+bx+c,$$ the substituion where $x = y-a/3$, $$g(y) = y^3+py+q$$where $$p = \frac13 (3b-a^2) \qquad q = \frac 1{27} (2a^-9ab+27c).$$We would like to adjoin the the $3$rd roots of unity. Let $\rho$ denote a primitive $3$rd root of unity, so that $\rho^2+\rho +1 = 0$. If $\alpha, \beta,\gamma$ are the roots of $g(y)$, we know that $$\alpha+\beta+\gamma = 0.$$This is actually one of the reasons why we consider $g(y)$ instead of $f(x)$. When working over the field $\Bbb Q(\sqrt D)$, with $D$ as the discriminant, then Galois group of $g(y)$ is $A_3 \cong C_3$. If we adjoin $\rho$ then this extension is a radical extension of degree $3$. and has a generator as a Lagrange resolvent. We consider the elements $$\begin{align*}
(\alpha, 1) &=  \alpha+\beta+\gamma = 0 \\
\theta_1 &:= (\alpha, \rho) =\alpha + \rho\beta+\rho^2\gamma \\ 
\theta_2 &:= (\alpha, \rho^2)= \alpha + \rho^2\beta+\rho\gamma \end{align*}
 $$
 We see the following relationships $$\begin{align*} 
 \theta_1+\theta_2  &= 3\alpha \\
 \rho^2\theta_1 +\rho \theta_2 &= 3\beta \\
 \rho \theta_1 +\rho^2\theta_2 &=3\gamma
 \end{align*}
 $$
 We want to expand $\theta_1^3$ we get that $$\alpha^3+\beta^3+\gamma^3+3\rho(\alpha^2\beta+\beta^2\gamma + \alpha\gamma^2)+ 3\rho^2(\alpha\beta^2+\beta\gamma^2+\alpha^2\gamma)+6\alpha\beta\gamma $$We have that $$ \sqrt{D} = (\alpha²\beta+\beta^2\gamma+\alpha\gamma^2)-(\alpha\beta^2+\beta\gamma^2+\alpha^2\gamma),$$and we are going to define $$S:= (\alpha²\beta+\beta^2\gamma+\alpha\gamma^2)+(\alpha\beta^2+\beta\gamma^2+\alpha^2\gamma).$$The value $\theta_1^3$ can be expressed as $$\alpha^3+\beta^3+\gamma^3 +\frac{3}{2}\rho(S+\sqrt D) + \frac{3}{2}\rho^2(S-\sqrt D)+6\alpha\beta\gamma .$$
  We can use [[Symmetric Polynomials|Newton's identities]] to get that $$\alpha^3+\beta^3+ \gamma^3 =-3q \quad \text{and}\quad S = 3q,$$where $s_1 = 0$, $s_2 = p$ and $s_3 = -q$. We now can substitute this equalities and get $$\begin{align*}
\theta_1^3 &= -3q + \frac32 \rho(3q+\sqrt D) + \frac32 \rho^2(3q-\sqrt D) -6q \\&= \frac{-27}{2}q + \frac 32 \sqrt{-3D}\end{align*}$$Again, we can do some calculations to get that $$\theta_1 \theta_2 = -3p.$$Using $D = -4p^3-27q^2$, we obtain Cardano's explicit formulas. Let $$\begin{align*} A &= \sqrt[3]{\frac{-27}{2}q + \frac 32 \sqrt{-3D}} \\ B &=\sqrt[3]{\frac{-27}{2}q - \frac 32 \sqrt{-3D}} \end{align*}$$Lastly, the roots of the equation $y^3+py+q = 0$ are $$\alpha= \frac{A+B}{3},\quad  \beta = \frac{\rho^2 A+ \rho B}{3}, \quad \gamma = \frac{\rho A+ \rho^2 B}{3},$$where $\rho = -\dfrac12 + \dfrac12 \sqrt{-3}$. 

There are two notable cases that can be distinguished by the sign of the discriminant. 