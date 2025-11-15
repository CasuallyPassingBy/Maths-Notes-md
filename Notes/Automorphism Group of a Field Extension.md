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

Given $H\le \text{Aut}(L/F)$ let $$L^H := \{a\in L \mid a\in \forall \sigma\in H(\sigma(a) = a) \},$$meaning, $L^H$ is the subset of $L$ that ate fixed by all the elements of $H \le\text{Aut}(L/F)$. 

**Lemma:** If $H\le \text{Aut}(L/F)$, then $L^H$ is an intermediate field of $L/F$. 

**Def:** If $H\le \text{Aut}(L/F)$, then $L^H$ is called the *fixed field* of the subgroup $H\le \text{Aut}(L/F)$. We have the function $$ F: \mathcal G_{L/F}\to \mathcal C_{L/F}$$ which for every subgroup $H$ of $\text{Aut}(L/F)$ we associate its corresponding fixed field $F(H) := L^H$. 

**Lemma:** The function $F: \mathcal G_{L/F}\to \mathcal C_{L/F}$ satisfies the following:
- If $H_1 \le H_2$ be subgroups of $\text{Aut}(L/F)$, then $F$ flips inclusions, i.e., $F(H_1)\supseteq F(H_2)$. 
- If $H \le \text{Aut}(L/F)$, then $H \le S(F(H))$. 
- If $M$ is an intermediate field of $L/F$, then $M \subseteq F(S(M))$. 

**Dedekind theorem:** Let $F$ be a field. Then, any finite set of distinct automorphisms $\sigma_1,\dots,\sigma_n: F \to F$ are linearly independent. Meaning, if $a_1\sigma_1(x) + a_n\sigma_n(x) = 0$ for all $x\in F$, then $a_i = 0$ for all $i\in\{1,\dots, n\}$. 

**Cor:** If $L/F$ is a finite field extension, then $|\text{Aut}(L/F)|\le [L:F]$. 

# Normal and Separability

**Th:** Let $G = \{\sigma_1,\dots, \sigma_n\}$ is a finite group of automorphisms of a field $L$ and $L^G$ is the fixed field of $G$, then $$[L: L^G]= |G| = n.$$
