---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Logarithms of curves]], [[Homotopy in C]], [[Homology in C]], [[Homotopy Cauchy's Theorem]]

The Riemann Mapping Theorem behaves as a huge connection to a lot of to numerous section of complex analysis, since it is a huge list of equivalences.

We need to just make $D = B_1(0)$

Let $U \subseteq \Bbb C$ be a region. Then all the following are equivalent
1. $U$ is [[Homology Cauchy's Theorem#^a4ab7b|simply connected]]
2. If $\Gamma \subseteq U$ a cycle, then $\Gamma \sim 0 \pmod U$
3. If $\Gamma \subseteq U$ a cycle, $f \in \mathcal H(U)$ and $a \in U\setminus \Gamma$, then $$ f(a) \cdot n(\Gamma;a) = \frac{1}{2\pi i }\oint_\Gamma \frac{f(z)}{z-a}\, dz $$
4. If $\Gamma \subseteq U$ a cycle and $f \in \mathcal H(U)$, then $$ \oint_\Gamma f(z)\, dz =0$$
5. If $f\in \mathcal H(U)$, then $f$ has a primitive on $U$
6. If $f \in \mathcal H(U)$ and $Z(f) = \varnothing$, then $f$ has a logarithm
7. If $f \in \mathcal H(U)$ and $Z(f) = \varnothing$, then $f$ has a square root, also known as the Riemann condition.
8. $U$ is [[Biholomorphism|biholomorphic]] to $\Bbb C$ or to $D$
9. $U$ is homeomorphic to $D$
10. If $\gamma\subseteq U$ is a closed curve, then $\gamma \simeq 0 \pmod U$
11. if $u \in \mathcal a(U)$, then $u$ has a has a [[2D Harmonic Functions|harmonic conjugate]] on $U$

We know that $1 \implies 2$ because of [[Homology Cauchy's Theorem#^e7f410|homology]]

We know that $2 \implies 3$ because of [[Cauchy's Integral Formula#Homology Cauchy Integral Formula|homology form of Cauchy's integral Formula]] 

We know that $3 \implies 4$ because, let $\Gamma \subseteq U$ be a cycle, $a \in U\setminus \Gamma$, and $f\in \mathcal H(U)$, then we define $g(z) = f(z)(z-a)$, and apply Cauchy's integral formula, then get the desired outcome

We know that $4 \implies 5$ because of [[Contour Integrals in C#Path-Independence Theorem|Path-independence Theorem]]

We know that $5 \implies 6$ because, if $f \in \mathcal H(U)$ and $Z(f) = \varnothing$, then $f'/f$ is analytic, and thus a primitive, which will be a logarithm of $f$.

We know that $6 \implies 7$ because given a logarithm we can construct the square root.

We know that $7 \implies 8$ because of [[Biholomorphism#Riemann Theorem|Riemann's Theorem]] 

We know that $8 \implies 9$ because $D \cong \Bbb C$, and every bilohomorphism is a homeomorphism. 

We know that $9 \implies 10$ because we can construct a homeomorphism to $D$, and then look that $\gamma \simeq 0\pmod U$

We know that $8 \implies 11$ because of we can make a harmonic function on $D$ that has a harmonic conjugate, and we can transport back the harmonic conjugate

We know $11 \implies 6$, we can construct a harmonic function from $f \in \mathcal H(U)$ that $Z(f) = \varnothing$, being $\ln|f| = u$ this $u$ is harmonic. We construct its harmonic conjugate, and an analytic function $g$ related to both. This $g+a$ for some $a\in \Bbb C$, is a logarithm 

We know that $10 \implies 2$ because of [[Logarithms of curves#Connection to Homoogy|the connection between homotopy and homology]]

We know that $6 \implies 2$ let $a \not\in U$, then $f\in \mathcal H(U)$, defined as $f(z) = z-a$, has $Z(f) = \varnothing$. We construct a logarithm $g$, and when we want to calculate the index we are integrating $g'$ over a closed cycle, getting $0$.

We know that $2 \implies 1$ because of [[Homology Cauchy's Theorem#^e7f410|homology]]