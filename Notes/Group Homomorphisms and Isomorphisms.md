---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]], [[Functions]], [[Normal Subgroups and Quotient Groups]], [[Symmetric Groups]], [[Automorphism Group]], [[Endomorphism Ring]]

**Def:** If a function between two groups $\phi: G \to G'$ satisfying that $\phi(ab) = \phi(a) \phi(b)$ for all $a, b\in G$, then we say that $\phi$ is a *group homomorphism*, or a *group morphism*, of $G$ on $G'$. In the case that $G' = G$, then $\phi$ is called a *group endomorphism*. 

**Lemma:** Let $\phi: G\to G'$ is a group homomorphism. Entonces, 
- $\phi(e) = e'$, where $e\in G$ and $e'\in G'$ are the respective identities
- If $g \in G$, then $\phi(g^{-1}) = \phi(g)^{-1}$

A common example, is that $N \trianglelefteq G$ is a normal subgroup is a natural function from $G$ to $G/N$, and $\rho: G \to G/N$ given by $\rho(g) = gN$. This is the *canonical homomorphism* or *canonical morphism*, and it is surjective. 

**Prop:** Let $\phi: G \to G'$ is a group morphism:
- If $H \le G$, then $\phi[H] \le G'$
- If $H \trianglelefteq G$, then $\phi[H] \trianglelefteq G'$
- If $K \le G'$, then $\phi^{-1}[K] \le G$ 
- If $K \trianglelefteq G'$, then $\phi^{-1}[K] \trianglelefteq G$

**Def:** If $\phi:G \to G'$ is a group homomorphism, and we consider the trivial subgroup $\{e'\}\trianglelefteq G'$ , then $\phi^{-1}\{e'\} \trianglelefteq G$. This is a special subgroup and it is called the *kernel of the homomorphism* $\phi$, and denoted as $$\ker (\phi):= \phi^{-1}\{e'\} = \{g\in G \mid \phi(a) = e'\}.$$
**Prop:** Let $\phi: G\to G'$ is a group homomorphism. Then $\phi$ is injective iff $\ker(\phi) = \{e\}$ is the trivial subgroup of $G$.

**Def:** If $\phi:G \to G'$ is a group homomorphism, and we consider the trivial subgroup $G\trianglelefteq G$ , then $\phi^[G] \trianglelefteq G'$. This is a special subgroup and it is called the *image of the homomorphism* $\phi$, and denoted as $$\text{Im} (\phi):= \phi[G] = \{\phi(g)\in G' \mid g \in G\}.$$
A group homomorphism $\phi: G \to G'$ is surjective iff $\text{Im}(\phi) = G'$ 

**Def:** When a homomorphism $\phi: G \to G'$ is bijective, then we say that $\phi$ is a *group isomorphism*. We also say that $G$ and $G'$ are *isomorphic* if there's an isomorphism between them. It is denoted as $(G, \cdot, e) \cong (G', \cdot', e')$ or $G \cong G'$ when the operation an identity are clear. 
In the case that $G' = G$, then $\phi$ is called as an *automorphism*. 

**Lemma:** 
- If $\phi: G \to G'$ is a group isomorphism, then its inverse $\phi^{-1}: G'\to G$ is also an isomorphism.
- If $\phi: G \to G'$ and $\psi:G'\to G''$ are group isomorphisms, then the composition $\psi \circ \phi: G \to G''$ is also an isomorphism.

**Factorising Homomorphism:** Let $\phi$ and $\psi$ be group homomorphism such that 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}
G \arrow[d, two heads,"\psi"'] \arrow[r, "\phi"] & \mathrm{Im}(\phi) \\ G/\ker(\phi) \arrow[ur, dashed, "\overline{\phi}"']
\end{tikzcd}
\end{document}
```

where $\psi$ is surjective and $\ker(\psi) \le \ker(\phi)$. Then there exists a unique group homomorphism $\overline \varphi: T \to H$ such that $\phi = \overline \varphi \circ \psi$, and:
- $\text{Im}(\overline \varphi) = \text{Im}(\phi)$
- $\ker(\overline \varphi) = \psi[\ker(\phi)]$ 
In fact:
- $\overline \varphi$ is surjective iff $\phi$ is surjective
- $\overline \varphi$ is injective iff $\ker(\phi) = \ker(\psi)$

**Noether's First Isomorphism Theorem:** If $\phi: G \to G'$ is a group homomorphism, then $\phi$ induces a group isomorphism $\overline \phi: G/\ker (\phi)\to \text{Im}(\phi)$, such that the diagram commutes: 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}     
G \arrow[d,two heads, "\rho"'] \arrow[dr, "\phi"] \\ G/\ker(\phi) \arrow[r, "\cong"'] & \mathrm{Im}(\phi)
\end{tikzcd}
\end{document}
```

**Cor:** Let $G$ be a group:
- If $\phi$ is a group homomorphism with domain $G$, then $\ker(\phi) \trianglelefteq G$, then $G/\ker(\phi) \cong \text{Im}(\phi)$. 
- If $N \trianglelefteq G$ is a normal subgroup of $G$, then $N$ is the kernel of the canonical group homomorphism $\rho: G \to G/N$.

**Noether's Second Isomorphism Theorem**: Let $H, K \le G$, with $K \trianglelefteq G$. Then $H\cap K \trianglelefteq H$, $HK \le G$, and $K \trianglelefteq HK$ and we have the isomorphism: $$H /(H \cap K) \cong HK/K$$
**Noether's Third Isomorphism Theorem:** Let $H, K \trianglelefteq G$ such that $H \le K$. Then $H \trianglelefteq K$, and $K/H \trianglelefteq G/H$ and $$(G/H)/(K/H) \cong G/K$$
**Cayley's Theorem:** Every group is isomorphic to a subgroup of a permutation group