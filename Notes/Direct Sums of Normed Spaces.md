---
tags:
  - FunctionalAnalysis
  - Analysis
---
Subjects: [[Functional Analysis]]
Links: [[Normed Vector Spaces]], [[Generation of Modules, Direct Sum, and Free Modules]]

**Def:** Let $X_1, \dots X_n$ be normed spaces with respective norms $\|\cdot \|_1, \dots \|\cdot \|_n$. The (*external*) *direct sum* or *direct product* of $X_1,\dots, X_n$ is the normed space whose underlying vector space is the vector space sum of $X_1, \dots, X_n$ and whose norm is the *direct sum norm* given by the formula $$\|(x_1, \dots, x_n)\| := \left(\sum_{k = 1}^n x_k^2\right)^{1/2}. $$This normed space is denoted by $X_1 \oplus \dots \oplus X_n$ or $\left(\bigoplus_{k = 1}^n X_k\right)_{\ell^2}$.

**Th:** Let $X_1, \dots, X_n$ be normed spaces. Then the product metric induced on $X_1 \times \dots \times X_n$ by the metrics of $X_1, \dots, X_n$ is the same as the metric induced by the direct sum norm, so the product topology of $X_1\times \dots \times X_n$ is the same as the topology induced by the direct sum norm.

**Prop:** Let $X_1, \dots X_n$ be normed spaces. For each integer $j$ such that $1 \le j \le n$, let $$X'_j := \{(x_1, \dots, x_n)\in X_1 \oplus \dots \oplus X_n \mid \forall k\in \{1, \dots, n\}\setminus \{j\}\  (x_k = 0)\}.$$Then $X'_j$ is a closed subspace of $X_1 \oplus \dots \oplus X_n$ that is isometrically isomorphic to the corresponding $X_j$. 

**Prop:** Let $X_1, \dots, X_n$ be normed spaces. If two direct sums are formed by permuting and associating the terms of $X_1\oplus \dots \oplus X_n$, then those two direct sums are isometrically isomorphic.

**Prop:** Let $X_1, \dots, X_n$ be normed spaces. Let $\{1, \dots, n\}$ be partitioned into two nonempty sets $\{j_1, \dots, j_p\}$ and $\{k_1, \dots, k_q\}$ and let $$X_{j_1, \dots, j_p} := \{(x_1, \dots, x_n)\in X_1 \oplus \dots \oplus X_n \mid \forall k\in \{1, \dots, n\}\setminus \{j_1, \dots, j_p\}\  (x_k = 0)\}.$$Then $(X_1\oplus \dots \oplus X_n)/X_{j_1, \dots, j_p}$ is isometrically isomorphic to $X_{k_1}\oplus \dots \oplus X_{k_q}$. 

**Th:** Let $X_1, \dots, X_n$ be normed spaces. Then $X_1 \oplus \dots \oplus X_n$ is a Banach space iff each $X_j$ is a Banach space.

**Def:** Suppose that $M_1, \dots, M_n$ are closed subspaces of a normed space $X$ such that $\sum_{k = 1}^n X$, and $M_j \cap \sum_{k \neq j} M_k = \{0\}$ when $j \in \{1, \dots, n\}$. Then the normed space $X$ is the *internal direct sum* of $M_1, \dots, M_n$. 

**Prop:**
- If $X_1, \dots, X_n$ are normed spaces and $X = X_1 \oplus \dots \oplus X_n$, then $X$ has closed subspaces $X_1', \dots, X_n'$ such that $X$ is the internal direct sum of $X_1', \dots, X_n'$ and each $X_j$ is isometrically isomorphic to the corresponding $X_j'$.
- If $X$ is a Banach space that is the internal direct sum of its closed subspaces $M_1, \dots, M_n$, then $X \cong M_1 \oplus \dots \oplus M_n$. 

**Def:** Suppose that $X_1, \dots, X_n$ and $Y_1, \dots Y_n$ are normed spaces and that $T_j$ is a linear operator from $X_j$ into $Y_j$ when $j \in \{1, \dots, n\}$. The the *direct sum* of $T_1, \dots T_n$ is the linear map $$T_1\oplus \dots \oplus T_n : X_1 \oplus \dots \oplus X_n \to Y_1 \oplus \dots \oplus Y_n $$defined by letting $$T_1 \oplus \dots \oplus T_n (x_1, \dots, x_n) = (T_1x_1, \dots, T_n x_n)$$whenever $(x_1, \dots, x_n) \in X_1 \oplus \dots \oplus X_n$. 

**Th:** Suppose that $X_1, \dots, X_n$ and $Y_1, \dots, Y_n$ are normed spaces and that $T_j$ is a linear operator from $X_j$ into $Y_j$ when $j \in \{1, \dots, n\}$. Then $T_1 \oplus \dots \oplus T_n$ is bounded iff each $T_j$ is bounded. If $T_1 \oplus \dots \oplus T_n$ is bounded, then $\| T_1 \oplus \dots \oplus T_n \| = \max\{\|T_j\| \mid 1 \le j \le n\}$. Furthermore, the operator $T_1\oplus \dots \oplus T_n$ is injective, surjective, or an isomorphism, or an isometric isomorphism, iff $T_1, \dots, T_n$ all have the same property.

**Cor:** Suppose that $X_1, \dots, X_n$ and $Y_1, \dots, Y_n$ are normed spaces. If $X_j \cong Y_j$ when $j\in \{1, \dots, n\}$, then $X_1 \oplus \dots \oplus X_n \cong Y_1 \oplus \dots \oplus Y_n$. If $X_j$ is isometrically isomorphic to $Y_j$ when $j\in \{1, \dots, n\}$, then $X_1 \oplus \dots \oplus X_n$ is isometrically isomorphic to $Y_1 \oplus \dots \oplus Y_n$.

**Def:** A subspace $M$ of a normed space $X$ is *complemented* in $X$ if it is closed in $X$ and there is a closed subspace $N$ of $X$ that is the internal direct sum of $M$ and $N$, in which case the subspace $N$ is said to be the *complementary* to $M$.