---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]], [[Subgroups]], [[Integers modulo n]], [[Equivalence Relations and Partitions]], [[Symmetric Groups]], [[Alternating Groups]], [[Quotient of Vector Spaces]]

# Cosets

If $H\le G$, we can define two equivalence relations:
- $a\equiv_l b \pmod H\iff a^{-1}b\in H$, we should call the *left congruence relation modulo $H$*. 
- $a\equiv_r b \pmod H\iff ab^{-1}\in H$, we should call the *right congruence relation modulo $H$*. 

The equivalence class $[\sigma]$ of $\sigma$ under $\equiv_l$ is $\sigma H$, and under $\equiv_r$ is $H \sigma$, which are called the *left coset of $H$*, and *right coset of $H$*, respectively. They are defined as $$\sigma H := \{g \in G \mid \exists h\in H[g = \sigma h]\} \qquad H\sigma := \{g \in G \mid \exists h\in H[g = h\sigma]\}$$
**Cor:** If $H \le G$:
- The left cosets $\sigma H$ form a partition $G$
- The right cosets $H\sigma$ form a partition $G$
- There exists a bijection of the left cosets of $H$ and the right cosets of $H$

**Lemma:** Let $H\le G$. Then
- The left cosets $\sigma H$ has the same cardinality as $H$
- The right cosets $H\sigma$ has the same cardinality as $H$

**Lagrange:** Let $G$ be a finite group of order $n$, and let $H\le G$ be a subgroup. Then $|H|  \mid | G|$. 

**Cor:** If $G$ is a finite group and $\sigma \in G$, then $O(\sigma) \mid |G|$

**Cor:** If $G$ is a finite group of order $n$ and $\sigma\in G$, then $\sigma^n = e$

**Cor:** Every finite group of prime order is cyclic

# Normal Subgroups

**Def:** If $A$ and $B$ be subsets of a group $G$ we define $$AB := \{ab \mid a\in A, b\in B\}$$then $AB$ is a subset of $G$. Note that the multiplication of subsets of $G$ is associative because the operation in $G$ is associative. 

This definition is natural, and when considering $A =\{a\}$ and $B= H\le G$, then $$A B = \{a\} H = aH \qquad BA = H\{a\}=Ha$$and if $A =B = H\le G$, then $AB = HH = H$. 

If $H\le G$ we denote as the set of all left cosets $gH$ of $H$ in $G$ by $G/H$. We would like to have that $G/H$ have a group structure, by inheriting something of the structure of $G$. So to left cosets $\sigma H$ and $\tau H$ and multiply them together, let's say $$(\sigma H)(\tau H) = \theta H$$and we define the operation between the two left cosets as $$(\sigma H)(\tau H) := (\sigma h) (\tau h') H = (\sigma \tau )H$$
with $\sigma h$ and $\tau h'$ being representatives of the cosets $\sigma H$ and $\tau H$, respectively, this operation is well defined if it doesn't depend on representatives 

**Lemma:** Let $H\le G$ and we suppose where the above operation on $G/H$ is well defined. Then, $G/H$ is a group under this operation and it is called the *quotient group of $G$ by $H$*. 

**Th:** Let $H \le G$. The multiplication of left cosets on $G/H$ is well defined iff every left coset is a right coset of $H$ on $G$. Meaning, iff $\sigma H = H \sigma$ for all $\sigma \in G$. 

**Cor:** Let $H \le G$. The following are equivalent:
- $aHa^{-1} \subseteq H$, for all $a\in G$
- $aHa^{-1} = H$, for all $a\in G$
- $aH = Ha$, fo all $a \in G$

**Def:** Let $H \le G$, if it satisfies any of the above conditions, then $H$ is called a *normal subgroup of* $G$, and it is denoted as $H \trianglelefteq G$. Then $G/H$ is a group and it is called the *quotient group* of $G$ by $H$. 

**Prop:** If $G$ is cyclic and $H \le G$, then $H \trianglelefteq G$ and $G/H$ is also cyclic.

**Correspondence Theorem:** If $N \trianglelefteq G$, then there exists a bijection between the family of subgroups of $G/N$ and the subgroups $H \le G$ such that $N \le H$. The correspondence is given by $$N \le H \le G \mapsto H/N \le G/N$$
we also have that $H \trianglelefteq G$ iff $H/N \trianglelefteq G/N$. 

**Cor:** If $H \le G$ and $[G: H] = 2$, then $H \trianglelefteq G$. 

**Prop:** If $H, K \trianglelefteq G$, then $HK \trianglelefteq G$

**Th:** If $G$ is abelian, then any subgroup is a normal subgroup.

