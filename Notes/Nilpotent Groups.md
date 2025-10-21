---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Solvable Groups]], [[Group Homomorphisms and Isomorphisms]], [[Cauchy and Sylow Theorems]]

**Def:** Let $G$ be a group. We define the subgroups $Z^k(G)$ of $G$ as follows: $Z^0(G) = \{e\}$ is the trivial subgroup, $Z^1(G)$ is the *centre* $Z(G)$ of the group $G$, $Z^2(G)$ is the subgroup of $G$ corresponding to the centre of quotient $G/Z^1(G)$, then $Z^1(G)\subseteq Z^2(G)$. We inductively, if $Z^k(G)$ is already defined, then $Z^{k+1}(G)$ is the normal subgroup of $G$ that correspond to the centre of the quotient $G/Z^k(G)$. We have the sequence of subgroups $$\{e\} = Z^0(G) \subseteq Z^1(G) \subseteq \dots \subseteq Z^k(G) \subseteq \dots \subseteq G,$$where $Z^{k+1}(G)$ is defined by $$Z^{k+1}(G)/Z^k(H) = Z(G/Z^k(G)).$$
The sequence of subgroups above is called the *central superios sequence* of $G$. A group $G$ is said to be *nilpotent* if there exists an integer $n \ge 0$ such that $Z^n(G) = G$. The least integer that satisfies $Z^n(G) =G$ is called the *class* of $G$. 

**Lemma:** Every nilpotent group is solvable.

**Lemma:** Every nontrivial nilpotent has a nontrivial centre. 

**Lemma:** Every finite $p$-group is nilpotent. 

We get the following strict inclusions of the different classes of subgroups: $$\mathsf{Abelian} \subseteq\mathsf{Nilpotent} \subseteq \mathsf{Solavable}.$$
**Lemma:**
- Let $H$ and $K$ subgroups of $G$. Then $[H, K] \subseteq H$ iff $K \le N_G(H)$. 
- If $K \trianglelefteq G$ and $K \le H \le G$, then $[H, G] \le K$ iff $H/K \le Z(G/K)$. 
- If $f: G \to G'$ is a surjective group homomorphism, and $A \subseteq Z(G)$, then $f[A] \subseteq Z(G')$. 

This last proposition tells that the sequence of groups of $G$: $$G = : L_1(G) \supseteq L_2(G) \supseteq \dots \supseteq L_k(G) \supseteq \dots \supseteq \{1\} = 1$$is called the *central inferior sequence of* $G$. 

**Th:** Let $G$ be a group. $Z^m(G) = G$ iff $L_{m+1}(G)$. It follows that $G$ is nilpotent of class $m$ iff $L_{m+1}(G) = 1$, and $m$ is the least integer that satisfies this. 

**Cor:** The following statements about groups.
- The subgroups of nilpotent groups are nilpontent. 
- If $G$ is nilpotent, and $H\trianglelefteq G$, then $G/H$ is nilpotent. 

**Lemma:** If $G$ is the direct product of a finite number of nilpotent groups, then $G$ is also nilpotent. 

**Burnside-Wielandt Theorem:** Let $G$ be a finite group. The following statements are equivalent.
- $G$ is nilpotent
- If $H$ is a proper subgroup of $G$, then $H < N_G(H)$
- For each prime $p$ there's only one Sylow $p$-subgroup of $G$.
- $G$ is the direct product of its Sylow subgroups. 