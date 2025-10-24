---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Rings and Fields]], [[Ring Homomorphisms]]

**Def:** Let $\{R_i \mid i \in I\}$ is a collection of rings. If $R = \prod_{i \in I} R_i$, then we define its operations componentwise and  for every $i\in I$ we have a surjective group homomorphism $\pi_i:R \to R_i$ which projects the product of the $i$th coordinate. 

**Th:** Let $\{R_i \mid i \in I\}$ is a collection of rings. If $R = \prod_{i \in I} R_i$, then the product $R$ together with the property $\pi$ has the following universal property. If $S$ is any ring and $\{f_i: S \to R_i\mid i \in I\}$ is a collection of ring homomorphism, then there exists precisely one ring homomorphism $f: S \to R$ such that $\pi_i \circ f = f_i$ for every $i\in I$. 

**Obs:** Let $R$ and $S$ be nonzero rings, then $R\times S$ is never a integral domain. 

**Obs:** Let $\{R_i \mid i \in I\}$ is a collection of rings. If $\{A_i \mid i \in I\}$ is a collection of ideals such that $A_i \le R_i$ for every $i\in I$, then $\prod_{i \in I} A_i$ is an ideal of $\prod_{i \in I} R_i$. 

**Prop:** Let $\{R_i \mid i\in\{1,\dots, n\}\}$ be a finite collection of ring, If $I$ is an ideal of $\prod_{i = 1}^n R_i$, then there are ideals $A_i \le R_i$ for every $i\in\{1,\dots, n\}$ such that $I = \prod_{i = 1}^n A_i$. 

**Prop:** If $e$ be an idenpotent in $R$ and $e\in Z(R)$, then $Re$ and $R(1-e)$ are two-sided ideals, $R \cong Re \times R(1-e)$, and $e$ and $(1-e)$ are identities for the subrings $Re$ and $R(1-e)$, respectively. 

**Cor:** If $R$ be a finite unital Boolean ring, then $R\cong (\Bbb Z/2\Bbb Z)^n$ for some $n$. 