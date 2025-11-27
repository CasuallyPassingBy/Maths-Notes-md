---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]], [[Linear Algebra]]
Links: [[Field Extensions]], [[Algebraic Field Extensions]], [[Determinants]], [[Trace of Matrix]], [[Characteristic and Minimal Polynomial of a Linear Transformation]], [[Separable Field Extensions]]

**Prop:** Let $F(\alpha)/F$ be a simple finite extension. Consider the function $\tilde\alpha: F(\alpha) \to F(\alpha)$ defined as $\tilde \alpha(x) = \alpha \cdot x$. Then $\tilde\alpha$ is a $F$-linear transformation, and $\phi(x) := \det(xI -\tilde \alpha)$ satisfies the equality $\text{Irr}(\alpha, F) = \phi(x)$. 

This fact is related to [[Rational or Frobenius Normal Form]] of linear transformations, and $\phi(x)$ is not the characteristic polynomial but the minimal polynomial of the companion matrix. 

**Th:** If $K/F$ be a finite field extension. If $[K: F] \le n$ then $K$ is isomorphic to a subfield of $\mathcal M_n(F)$. This means, that $\mathcal M_n(F)$ contains all the field extensions of degree less than $n$. 

[[Matrix Representation of Complex Numbers]] is a special case of this theorem. 

**Th:** Let $K/F$ be a finite field extension, and $\alpha \in K$. The minimal polynomial of $\alpha$ equals the minimal polynomial of $\widetilde \alpha$. The characteristic polynomial of $\widetilde\alpha$ is $\text{Irr}(\alpha, F)^{[K: F(\alpha)]}$. 

Let $K/F$ be a finite field extension and $\alpha \in K$. We consider the $F$-linear transformation $\widetilde\alpha: K \to K$ defined as $\widetilde\alpha(x) = \alpha x$. We have seen that the minimal polynomial of this linear transformation corresponds to the minimal polynomial of $\alpha$. Now if we consider the determinant of this linear transformation we get something different. 

**Def:** Let $K/F$ be a finite field extension and $\alpha\in K$. We consider $\widetilde \alpha$ as above, then $\text N_{K/F}(\alpha) := \det \widetilde \alpha$. 

**Prop:** Let $\sigma_1,\dots, \sigma_n$ be the roots of the minimal polynomials of $\alpha$ over $F$; then $$\text N_{K/F}(\alpha) = \left(\prod_{j= 1}^n \sigma_j(\alpha)\right)^{[K: F(\alpha)]}.$$If $K/F$ is separable, then each root appears only once in the product, but $[K: F(\alpha)]$ might be greater than $1$. 

**Cor:** If $K/F$ is a finite Galois extension. If $\alpha \in K$, then $$\text N_{K/F}(\alpha) = \prod_{\sigma\in \text{Gal}(K/F)}\sigma(\alpha). $$
**Obs:** Let $K/F$ be a finite field extension. If $\alpha \in K$, then $\text N_{K/F}(\alpha) \in F$. 

**Prop:** Let $K/F$ be a finite field extension. If $\alpha, \beta \in K$, then $\text N_{K/F}(\alpha\beta) = \text N_{K/F}(\alpha) \text N_{K/F}(\beta)$, meaning that is multiplicative from $K$ to $F$. 

**Cor:** Let $K = F(\sqrt D)$ be a quadratic extension of $F$. Then $\text N_{K/F}(a + b\sqrt D) = a^2-Db^2$. 

**Prop:** Let $x^d +a_{d-1}x^{d-1} + \dots a_1 x + a_ 0  =\text{Irr}(\alpha, F)$ be the minimal polynomial for $\alpha\in K$ over $F$. Let $n = [K: F]$. We see that $d\mid n$, there are $d$ distinct Galois conjugates of $\alpha$ which are all repeated $n/d$ times in the product above, and $$\text N_{K/F}(\alpha) = (-1)^{n }a_0^{n/d}.$$
**Prop:** Let $K/F$ be a finite field extension with degree $n$. If $\alpha \in K$ and $a\in F$, then $\text{N}_{K/F}(a\alpha) = a^n\text{tr}_{K/F}(\alpha)$, and in particular, $\text{tr}_{K/F}(a) = a^n$. 

**Def:** Let $K/F$ be a finite field extension. If $\alpha \in K$, then we can define its *trace* as $$\text{tr}_{K/F}(\alpha) := \text{tr}(\widetilde \alpha). $$
**Prop:**  Let $\sigma_1,\dots, \sigma_n$ be the roots of the minimal polynomials of $\alpha$ over $F$; then $$\text{tr}_{K/F}(\alpha) = [K: F(\alpha)]\sum_{j= 1}^n \sigma_j(\alpha).$$If $K/F$ is separable, then each root appears only once in the product, but $[K: F(\alpha)]$ might be greater than $1$. 

**Cor:** If $K/F$ is a finite Galois extension. If $\alpha \in K$, then $$\text{tr}_{K/F}(\alpha) = \sum_{\sigma\in \text{Gal}(K/F)}\sigma(\alpha). $$
**Obs:** Let $K/F$ be a finite field extension. If $\alpha, \beta\in K$, then $\text{tr}_{K/F}(\alpha)\in F$, and $\text{tr}_{K/F}(\alpha + \beta) = \text{tr}_{K/F}(\alpha) + \text{tr}_{K/F}(\beta)$, meaning it is an additive map from $K$ to $F$. 

**Prop:** **Cor:** Let $K = F(\sqrt D)$ be a quadratic extension of $F$. Then $\text{tr}_{K/F}(a + b\sqrt D) = 2a$. 

**Prop:** Let $x^d +a_{d-1}x^{d-1} + \dots a_1 x + a_ 0  =\text{Irr}(\alpha, F)$ be the minimal polynomial for $\alpha\in K$ over $F$. Then $$\text{tr}_{K/F}(\alpha) = -\frac nd a_{d-1}.  $$
**Prop:** Let $K/F$ be a finite field extension with degree $n$. If $\alpha \in K$ and $a\in F$, then $\text{tr}_{K/F}(a\alpha) = a\text{tr}_{K/F}(\alpha)$, and in particular, $\text{tr}_{K/F}(a) = na$. 

**Prop:** If $K/F$ be a [[Galois Field Extensions|Galois extension]], then there is an element $\alpha\in K$ with $\text{tr}_{K/F}(\alpha) \ne 0$. 

**Obs:** If $K/F$ is a Galois extension, and $\sigma$ is a $F$-automorphism of $K$, then  $\text N_{K/F}(\beta/\sigma (\beta)) = 1$, and $\text{tr}_{K/F}(\beta - \sigma(\beta)) = 0$ for every $\beta\in K$. 

This observation tells us that Galois conjugates are really difficult to tell apart. 

**Hilbert's Theorem 90 or Satz 90:** Let $K/F$ be a Galois extension with cyclic Galois group order $n$ generated by $\sigma$. If $\alpha \in K$ has $\text N_{K/F}(\alpha) = 1$, then there exists $\beta\in K$ such that$$\alpha = \frac\beta{\sigma(\beta)}.$$
**Cor:** The rational solutions $a, b\in \Bbb Q$ for the Pythagoras's equation $a^2 + b^2 = 1$ are of the form $a = \dfrac{s^2-t^2}{s^2+t^2}$ and $b = \dfrac{2st}{s^2+t^2}$ for some $s, t\in \Bbb Q$ and hence, any right triangle with integer sides has sides of length $(m^2-n^2, 2mn, m^2+n^2)$ for some integers $m$ and $n$. This is because $a^2 + b^2 = \text N_{\Bbb Q(i)/\Bbb Q}(a+bi) = 1$. 

**Cor:** Let $D\in \Bbb Z$ such that is not a perfect square. The rational solution to the equation $a^2+Db^2 = 1$ has rational solutions of the form $a = \dfrac{s^2-Dt^2}{s^2+Dt^2}$ and $b = \dfrac{2st}{s^2+Dt^2}$ for some $s, t\in \Bbb Q$, 

**Additive Hilbert Theorem 90:** Let $K/F$ be a Galois extension with cyclic Galois group order $n$ generated by $\sigma$. If $\alpha \in K$ has $\text{tr}_{K/F}(\alpha) = 0$, then there exists $\beta\in K$ such that$$\alpha = \beta-{\sigma(\beta)}.$$