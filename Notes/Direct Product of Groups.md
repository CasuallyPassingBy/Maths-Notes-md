---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]], [[Cartesian Product]], [[Normal Subgroups and Quotient Groups]], [[Subgroups]]

**Def:** Let $G$ and $K$ groups, the Cartesian product $$G \times K := \{(a, b) \mid a \in G, b \in K\}$$is a group with the operation being component wise, meaning given $(a, b), (a', b') \in G \times K$ then $$(a, b)\cdot (a', b'):= (aa', bb') $$the identity element is $(e_G, e_K)$, and the inverse of $(a, b)$ is $(a^{-1}, b^{-1})$. The group $G \times K$ is known as the *direct product* of the groups $G$ and $K$.

**Prop:** Let $H$ and $G$ be groups, then $H \times G \cong G \times H$. It means that the direct product is practically commutative. 

**Prop:** If $G = H \times K$, $H_1 \triangleleft H$, and $K_1 \triangleleft K$, then $H_1 \times K_1 \triangleleft G$ and $G/(H_1 \times K_1) \cong H/H_1 \times K/K_1$. 

**Prop:** If $G = H \times K$, then $Z(G) = Z(H) \times Z(K)$. 

**Prop:** If $G = H \times K$, then $G/(H \times \{e\}) \cong K$.

**Cor:** If $H \times K = H \times L$, then $K \cong L$

**Def:** If $G$ is a group. Consider the direct product $G$ with itself: $G \times G$ and let $\Delta \subseteq G \times G$ the diagonal: $$\Delta := \{(g, g) \mid g\in G\}$$
**Prop:** We have the following properties of the diagonal:
- $\Delta \le G \times G$
- $\Delta \cong G$ 
- $\Delta \triangleleft G\times G$ iff $G$ is abelian

**Prop:** let $n, m \in \Bbb N^+$ with $(n, m) = 1$, then $\Bbb Z_{nm} \cong \Bbb Z_n \times \Bbb Z_m$

**Prop:** Let $G$ be a group, and $H, K \trianglelefteq G$. If $G = HK$ and $H \cap K = \{e\}$, then $G \cong H \times K$. In the proof of this statement, we saw that if $a\in G$ and $b\in K$, then $ab = ba$, meaning every element of $G$ commutes with every element of $K$.

**Prop:** If $H$ and $K$ are subgroups of a finite group $G$, then $$HK = \frac{|H||K|}{|H\cap K|}$$
**Def:** Let $H, K\trianglelefteq G$, such that:
- $H \cap K = \{e\}$
- $HK = G$
- Every element of $H$ commutes with every element of $K$
Then we say that $G$ is the *direct internal product* of $H$ and $K$

**Prop:** If $G$ is a finite group, and $H$ and $K$ normal subgroup of $G$ such that $G = HK$ and $|G| = |H| |K|$, then $G$ is the direct internal product of $H$ and $K$.

**Prop:** If $G$ is a group with subgroups $H, H', K$ and $K'$ such that $H \cong H'$ and $K \cong K'$, and $H \cap K = \{e\} = H' \cap K'$, then $HK \cong H'K'$ 

**Def:** Let $G_1, \dots, G_n$ be a groups with $n\in \Bbb N$, the direct product is $$\prod_{i = 1}^n G_i =G_1 \times \dots \times G_n = \{(g_1, \dots, g_n) \mid g_i \in G_i\}$$where the operation is done component-wise, and the identity element is $(e_1, \dots, e_n)$, where $e_i$ is the identity of $G_i$. This group $G :=  \prod_{i = 1}^n G_i$ is called the direct product of $G_1, \dots, G_n$. We have injective homomorphisms: $$\phi_i: G_i \to G$$defined as $\phi(g):= (e, \dots, g, \dots, e)$. If we denote $\widetilde G_i$ as the image of $\phi_i$, then $\phi_i: G_i \to \widetilde G_i$ is an isomorphism. 

**Prop:** If $H_1, \dots, H_n$ be normal subgroups of $G$ with $n \in \Bbb N$, then $\psi: G \to \prod_{i = 1}^n G/ H_i$ given by $\psi(g) := (gH_1, \dots, gH_n)$ is a surjective homomorphism with kernel: $$\ker \psi= \bigcap_{i = 1}^n H_i$$
**Prop:** Let $G = \prod_{i = 1}^n H_i$ (the Cartesian product), and $N \triangleleft G$. We define $N_i = \pi_i[N]$, then $N = \prod_{i = 1}^n N_i$, then $$G/N \cong \prod_{i = 1}^n H_i /N_i$$

**Prop:** Let $G_1, \dots, G_n$ be groups. If $G = \prod_{i = 1}^n G_i$, then:
- each $\widetilde G_i \triangleleft G$ 
- $G = \prod_{i = 1}^n \widetilde G_i$, where the multiplication being done is the one for subsets. 
- $\widetilde G_i \cap \prod_{j \ne i}^n\widetilde  G_j =\{e\}$, for each $i= 1, \dots, n$. $\widetilde G_i$ has trivial intersection with the product of all other subgroups. 

**Def:** Let $H_1, \dots, H_n \le G$ with $n \in \Bbb N$. We say that $G$ is the *direct internal product* of the subgroups $H_1, \dots, H_n$ if  it satisfies the following conditions:
- $H_i \triangleleft G$ 
- $G = H_1 \cdots H_n = \prod_{i = 1}^n H_i$ (where this is the product of subsets of $G$)
- $H_i \cap \prod_{j \ne i}^n H_j =\{e\}$, for each $i = 1, \dots, n$

**Prop:** If $G$ is the internal direct product of the subgroups $H_1, \dots, H_n$ then $$G \cong H_1 \times \dots \times H_n = \prod_{i = 1}^n H_i$$
**Prop:** Let $G$ be finite group. If $G$ is the product of normal subgroups $H_1, \dots, H_n$ and the orders of the subgroups are pairwise coprime. Then $$G \cong H_1 \times \dots \times H_n = \prod_{i = 1}^n H_i$$