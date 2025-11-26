---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Automorphism Group]], [[Classification of Simple Field Extensions]]

An *isomorphism* between two extension $L/F$ and $K/F$ over the same field, is an field isomorphism $\phi: L \to K$ such that $\phi|_F = \text{id}_F$, i.e., the following diagram commutes
```tikz
\usepackage{tikz-cd} 
\usepackage{amsfonts, amsmath, amssymb}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
L\arrow[r, "\phi"]\arrow[d, dash] & K\arrow[d, dash]\\
F\arrow[r, "\text{id}_F"] & F
\end{tikzcd}
\end{document}
```
In particular, it means that $\phi$ fixes $F$. Thus, an automorphism of field extension $K/F$, is a field automorphism $\phi: K \to K$ such that $\phi|_F = \text{id}_F$, i.e., a field automorphism of $K$ that leave $F$ fixed. The automorphisms of the field extension $K/F$ are called *$F$-automorphisms of $K$.* 

**Obs:** If $K/F$ is a field extension, then the set of $F$-automorphisms of $K$, denoted $\text{Aut}(K/F)$ is a group, and it is a subgroup of $\text{Aut}(K)$. 

**Def:** Let $L/K$ and $K/F$ be a field extensions. I am gonna use the notation $$S(K) := \text{Aut}(L/K) \le \text{Aut}(L/F),$$to denote the subgroup $\text{Aut}(L/F)$ associated with the intermediate field $K$. We have the function $$S: \mathcal F_{L/F}:=\{\text{Intermediate fields of }L/F\}\to \mathcal G_{L/F}:=\{\text{Subgroups of }\text{Aut}(L/F)\}.$$
We have the following properties of this function $S$.

**Prop:** The function $S: \mathcal C_{L/F} \to \mathcal G_{L/F}$ satisfies the following:
- If $M_1\subseteq M_2$ are intermediate fields, then $S$ flips the inclusions, i.e., $S(M_2)\subseteq S(M_1).$
- For the intermediate field, $M = F$, we have that $S(M) = \text{Aut}(L/F)$ is the total group.
- For the intermediate field $M = L$, we have that $S(L) = \text{Aut}(L/L) = \{\text{id}_L\}$ is the trivial subgroup.

Given a subgroup $H$ of the group $G = \text{Aut}(L/F)$ we would like to associate it with an intermediate field of $L/F$. 

Let us observer that $\text{Aut}(L)$ [[Group Actions|acts naturally]] on $L$, since the action is just $(\sigma, \alpha) \in \text{Aut}(L) \times L \mapsto \sigma(\alpha)\in L$. This means that if $L/F$ is a field extension, then $\text{Aut}(L/F)$ also acts naturally on the extension $L/F$, by the same action. 

Given $H\le \text{Aut}(L/F)$ let $$L^H := \{a\in L \mid a\in \forall \sigma\in H(\sigma(a) = a) \},$$meaning, $L^H$ is the subset of $L$ that ate fixed by all the elements of $H \le\text{Aut}(L/F)$. This is just the $H$[[Group Actions#^7f0380|-fixed points]] of $L$. 

**Lemma:** If $H\le \text{Aut}(L/F)$, then $L^H$ is an intermediate field of $L/F$. 

**Def:** If $H\le \text{Aut}(L/F)$, then $L^H$ is called the *fixed field* of the subgroup $H\le \text{Aut}(L/F)$. We have the function $$ F: \mathcal G_{L/F}\to \mathcal C_{L/F}$$ which for every subgroup $H$ of $\text{Aut}(L/F)$ we associate its corresponding fixed field $F(H) := L^H$. 

**Lemma:** The function $F: \mathcal G_{L/F}\to \mathcal C_{L/F}$ satisfies the following:
- If $H_1 \le H_2$ be subgroups of $\text{Aut}(L/F)$, then $F$ flips inclusions, i.e., $F(H_1)\supseteq F(H_2)$. 
- If $H \le \text{Aut}(L/F)$, then $H \le S(F(H))$. 
- If $M$ is an intermediate field of $L/F$, then $M \subseteq F(S(M))$. 

**Def:** A *character* $\chi$ of a group $G$ with values in the field $L$ is a homomorphism from $G$ to the multiplicative group of $L$: $\chi: G \to L^\times$, i.e., $\chi(g_1g_2) = \chi(g_1) \chi(g_2)$ for all $g_1, g_2\in G$. 

**Def:** The characters $\chi_1,\dots, \chi_n$ of $G$ are said to be *linearly independent* over $L$ if they are linearly independent as function on $G$,i.e., there is no nontrivial relation $$a_1 \chi_1 + \dots + a_n \chi_n = 0$$with $a_1,\dots, a_n \in L$ not all zero. 

**Linear Independence of Characters:** If $\chi_1,\dots, \chi_n$ are distinct characters of $G$ with values in $L$ then they are linearly independent over $L$ .

**Dedekind theorem:** Let $F$ be a field. Then, any finite set of distinct automorphisms $\sigma_1,\dots,\sigma_n: F \to F$ are linearly independent. Meaning, if $a_1\sigma_1(x) + a_n\sigma_n(x) = 0$ for all $x\in F$, then $a_i = 0$ for all $i\in\{1,\dots, n\}$. 

**Cor:** If $L/F$ is a finite field extension, then $|\text{Aut}(L/F)|\le [L:F]$. 

**Th:** Let $G = \{\sigma_1,\dots, \sigma_n\}$ is a finite group of automorphisms of a field $L$ and $L^G$ is the fixed field of $G$, then $$[L: L^G]= |G| = n.$$
**Artin Theorem:** Let $G$ be a subgroup of a finite automorphism group of a field $L$. If $L^G$ is the fixed field of $G$, then $\text{Aut}(L/L^G) = G$. 

**Cor:** Let $L$ be a field. The function $F$, that assigns each finite subgroup $G$ of $\text{Aut}(L)$ to $L^G,$ is injective.

The results above show that the importance for a finite extension $L/F$ is to have that $F = L^G$ is the fixed field of the group $\text{Aut}(L/F)$. 