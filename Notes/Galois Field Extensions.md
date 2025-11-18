---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Automorphism Group of a Field Extension]], [[Splitting Fields and Normal Field Extensions]], [[Separable Field Extensions]]

**Def:** If $L/F$ is a finite, separable and normal extension, we call it a *Galois extension.* Additionally, the automorphism group $\text{Aut}(L/F)$ is known as the *Galois group of the extnesion* and it is denoted $\text{Gal}(L/F)$. 

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

The proof of the last point of the fundamental theorem of Galois theory actually relies on the [[Group Homomorphisms and Isomorphisms#^ff5e58|first isomorphism theorem for groups]], 

This theorem, actually gives us the *Galois correspondence* between subgroups of $\text{Gal}(L/F)$ and intermediate fields of the extension $L/F$. ^5c8efc