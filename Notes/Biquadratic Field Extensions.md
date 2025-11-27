---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Characteristic of a Ring]]

For this note $F$ is a field with characteristic different from $2$. 

**Obs:** Let $F$ be a field. If $D$ is not a square in $F$, then $F(\sqrt D)/F$ is a field extension. Note that this is a Galois extension, with $\text{Gal}(F(\sqrt D)/ F) \cong C_2$, the cyclic group of order $2$. 

**Lemma:** Let $\alpha$ and $\beta$ be elements of $F$, neither of which is a square in $F$. Then $F(\sqrt\alpha, \sqrt\beta)$ is of degree $4$ if $\alpha\beta$ is not a square in $F$ and is of degree $2$ otherwise.

**Def:**  Let $\alpha$ and $\beta$ be elements of $F$, neither of which is a square in $F$. When $F(\sqrt\alpha, \sqrt\beta)$ is of degree $4$ over $F$ the field extensions is called a *biquadratic extension* of $F$. 

**Prop:** Let $a, b$ be elements of the field $F$ with $b$ not a square in $F$. $\sqrt{a+\sqrt b} = \sqrt m+\sqrt n$ for some $m$ and $n$ in $F$ iff $a^2 -b$ is a square in $F$. 

We can find $m, n$, if we solve the system of equations $$
\begin{align*}a &= m+n \\ a^2-b &= (m-n)^2\end{align*}$$
**Cor:** Let $a, b\in \Bbb Q$. If $a^2-b$ is a square in $\Bbb Q$, then $\Bbb Q(\sqrt{a+\sqrt b})$ is a biquadratic field.

**Th:** If $K = F(\sqrt{D_1}, \sqrt {D_2})$  is a biquadratic extension, then $K/F$ is a Galois extension with $\text{Gal}(K/F)$ is isomorphic to the Klein $4$-group. Conversely, if $K/F$ is a Galois extension and $\text{Gal}(K/F)$ isomorphic to the Klein $4$-group, then $K/F$ is a biquadratic field extension. 

