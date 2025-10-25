---
tags:
  - RingTheory
  - NumberTheory/AlgebraicNumberTheory
---
Subjects: [[Ring Theory]], [[Algebraic Number Theory]]
Links: [[Rings and Fields]], [[Continued Fractions]]

**Def:** Let $D \in \Bbb Q$ that is not a perfect square in $\Bbb Q$, i.e. $\sqrt{D} \notin \Bbb Q$, and define $$\Bbb Q(\sqrt D) := \{a + b\sqrt D\mid a, b\in \Bbb Q\} \subseteq \Bbb C.$$

This set is closed under subtraction, and multiplication. Hence $\Bbb Q(\sqrt D)$ is a subring of $\Bbb C$. We can see that the assumption that $D$ is not a square implies that every element of $\Bbb Q(\sqrt D)$ may be written uniquely in the form $a + b\sqrt D$. This assumption implies that if $a \neq 0$ or $b \neq 0$, then $a^2- Db^2 \neq 0$, since $(a+ b\sqrt D)(a-b\sqrt D) = a^2-Db^2$. It follows that if $a+b \sqrt D\neq 0$, then $\dfrac{a - b\sqrt D}{a^2-Db^2}$ is the inverse of $a+b\sqrt D$. This shows that $\Bbb Q(\sqrt D)$ is field, called a *quadratic field*. 

The rational number $D$ may be written as $D = f^2 D'$ for some $f\in \Bbb Q$ and $D'$ is a unique square-free integer. Call $D'$ the *square-free part* of $D$. Then $\sqrt D = f\sqrt {D'}$, and so $\Bbb Q(\sqrt D) = \Bbb Q(\sqrt{D'})$. Thus, *there is no loss in assuming that $D$ is a square-free integer in the definition of the quadratic field $\Bbb Q(\sqrt D)$*. 

**Def:** Let $D$ be a square-free integer. It is immediate from the addition and multiplication that the subset $\Bbb Z[ \sqrt D] := \{a + b\sqrt D\mid a, b\in \Bbb Z\}$ forms a subring of the quadratic field $\Bbb Q(\sqrt D)$ defined earlier. If $D \equiv 1 \pmod 4$ then the slightly larger subset $$\Bbb Z \left[\frac{1+\sqrt D}{2}\right] := \left\{\left. a + b\frac{1+\sqrt D}{2}\;\right \rvert \; a, b \in \Bbb Z\right\}$$is also a subring: closure under addition is immediate and $$\left(a+ b \frac{1+\sqrt D}{2}\right)\left(c+ d\frac{1+\sqrt D}{2}\right) = \left(ac + bd \frac{D-1}{4}\right)+(ad + bc+ bd)\frac{1+\sqrt D}{2}$$together with the congruence on $D$ shows closure under multiplication.

Define $$\mathcal O = \mathcal O_{\Bbb Q(\sqrt D)} = \Bbb Z[\omega] = \{a+ b\omega\mid a, b\in \Bbb Z\},$$where $$\omega := \begin{cases} \sqrt D & D \equiv 2, 3 \pmod 4 \\
\dfrac{1+\sqrt D}{2} & D \equiv 1 \pmod 4,
\end{cases}$$called the *ring of integers* in the quadratic field $\Bbb Q(\sqrt D)$. The terminology comes from the fact that $\cal O$ has many properties analogous to those of the subring of integers $\Bbb Z$ in $\Bbb Q$ (and are called the *integral closure* of $\Bbb Z$ in $\Bbb Q(\sqrt D)$)

In the special case when $D = -1$ we obtain the ring $\Bbb Z[i]$ of *Gaussian integers*. These numbers were originally introduced by Gauss around $1800$ in order to state the biquadratic reciprocity law. 

We also define the *field norm* $N : \Bbb Q(\sqrt D) \to \Bbb Q$ by $$N(a+b\sqrt D) := (a+b\sqrt D)(a-b\sqrt D)=  a^2 - Db^2.$$This norm gives a measure of 'size' in the field $\Bbb Q(\sqrt D)$.

**Prop:** The field norm $N$ is multiplicative, i,e, that $N(\alpha\beta) = N(\alpha) N(\beta)$ for all $\alpha, \beta\in \Bbb Q(\sqrt D)$. 

On the subring $\cal O$ is also easy to see that the field norm is given by $$N(a+b\omega) := (a+ b\omega)(a+b\overline \omega)=\begin{cases}a^2- Db^2 & D \equiv 2, 3 \pmod 4 \\
a^2+ab+ \dfrac{1-D}{4} b^2 & D \equiv 1 \pmod 4,\end{cases}$$where $$\overline \omega := \begin{cases} - \sqrt D & D \equiv 2, 3 \pmod 4 \\ \dfrac{1-\sqrt D}{2} & D \equiv 1 \pmod 4.\end{cases}$$From this we can see that if $\alpha \in \cal O$, then $N(\alpha) \in \Bbb Z$. 

**Prop:** Let $\alpha \in \cal O$. $\alpha$ is a unit iff $N(\alpha) = \pm 1$. 

**Obs:** The determination of the integer solutions to the equation $x^2- Dy^2 = \pm 1$, *Pell's equation* in number theory, is essentially equivalent to the determination of the units in the ring $\cal O$.

**Prop:** $(\Bbb Z[i])^\times = \{\pm 1, \pm i\}$.

**Prop:** $\left(\Bbb Z\left[\frac{1+\sqrt{-3}}{2}\right]\right)^\times = \{\pm 1, \pm \rho, \pm \rho^2\},$ where $\rho = (-1+\sqrt{3})/2$. 

**Th:** If $D <0$, then $(\Bbb Z[\omega])^\times = \{\pm 1\}$, when $D\neq -1, -3$. 

**Th:** If $D> 0$, then $(\Bbb Z[\omega])^\times$ is infinite. 



**Prop:** There are special values of the quadratic integers where it is an [[Euclidean Domains|Euclidean domain]]. 
- $\Bbb Z[\sqrt{2}]$. 
- The Gaussian Integers $\Bbb Z[i]$.
- $\Bbb Z[\sqrt{-2}]$.
- The Eisenstein Integers $\Bbb Z[(1+\sqrt{-3})/2]$.
- $\Bbb Z[(1+\sqrt{-7})/2]$.
- $\Bbb Z[(1+\sqrt{-11})/2]$.

**Prop:** The following rings are [[Principal Ideal Domains|principal ideal domains]] but not Euclidean Domains:
- $\Bbb Z[(1+\sqrt{-19})/2]$
- $\Bbb Z[(1+\sqrt{-43})/2]$
- $\Bbb Z[(1+\sqrt{-67})/2]$
- $\Bbb Z[(1+\sqrt{-163})/2]$