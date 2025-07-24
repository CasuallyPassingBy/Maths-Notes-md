---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Weak, Partial, and Total Separations]], [[Topological Spaces]], [[Ultraparacompactness]], [[Paracompacteness]], [[Metrization Theorems]], [[Collectionwise Normal Spaces]], [[Collectionwise Hausdorff spaces]], [[Lašnev Spaces]], [[Zero Dimensional Spaces]]

For the rest of this note, we will consider that $X$ is a $T_1$ space. We will consider the collection $\text{Fin}(X)= \mathcal F(X) := \{A\subseteq X \mid 0 < |A| <\omega\} = [X]^{< \omega}\setminus \{\varnothing\}$ of the nonempty subsets of $X$. Let $n \in \omega\setminus 1$, then we can consider the set $\text{Fin}_n(X) = \mathcal F_n(X) := \{F \subseteq X \mid 0 < |F| \le n\} = [X]^{\leq n}\setminus \{\varnothing\}$.

Let $(X, \tau)$ be a topological. For any $F\in \mathcal F(X)$ and $S\in \mathcal P(X)$, we define the set $$ [F, S] := \{G \in \mathcal F(X) \mid F \subseteq G \subseteq S\},$$the fact that $[F, S] \cap [G, T] = [F \cup G, S \cap T]$, whenever $F, G\in \mathcal F(X)$, and $S, T \in \mathcal P(X)$, let us define the a topological base $\{[F, U] \mid F\in \mathcal F(X) \land U \in \tau\}$, for the *Pixley-Roy Hyperspace.* The symbol $\mathcal F[X]$ represents the set $\mathcal F(X)$ with this topology. Similarly, we can consider $\mathcal F_n[X]$ as a subspace of $\mathcal F[X]$ for all $n \in \omega\setminus 1$. 

**Prop:** Let $A$ be a subspace of $X$, then $\mathcal F[A]$ is a closed subspace of $\mathcal F[X]$.

**Prop:** If $F\in \mathcal F[X]$ and $S\in \mathcal P(X)$, then $[F, S]$ is a closed subspace of $\mathcal F[X]$.

**Cor:** $\mathcal F[X]$ is zero-dimensional and $T_1$.

**Question:** ¿Is $\mathcal F[X]$ is strongly zero-dimensional for any topological space $X$? If not, ¿when does $\mathcal F[X]$ is strongly zero-dimensional?

**Prop:** $\mathcal F[X]$ is hereditarily metacompact.

**Prop:** The following statements are equivalent.
- $\mathcal F[X]$ is a Moore space.
- $\mathcal F[X]$ is first countable.
- $\mathcal F_2[X]$ is first countable.
- $X$ is first countable.

**Prop:** If $X$ and $Y$ are topological spaces and $X \cap Y = \varnothing$, then $\mathcal F[X\oplus Y] \cong \mathcal F[X] \oplus \mathcal F[Y] \oplus \mathcal F[X] \times \mathcal F[Y].$

**Cor:** If $n \in \omega\setminus 1$ and $\{X_m \mid m < n\}$ is a family of topological spaces, then $$
\mathcal F\left[\bigoplus_{m < n} (X_m \times \{m\})\right]\cong \bigoplus_{A \in \mathcal F[n]} \left(\prod_{m \in A} \mathcal F[X_m]\right)$$
**Obs:** For each $n \in \omega\setminus 1$, the subspaces $\mathcal F_n[X]$, and $[X]^n$ are closed and discrete subspace of $\mathcal F[X]$, respectively. 

**Def:** Let $X$ be a topological space, $n \in \omega\setminus 1$, and $\mathcal V\subseteq \tau_{\mathcal F[X]}^+$ a celular family. We say that $\cal V$ is a *$n$-proper family* if $\mathcal F_n[X] \subseteq \bigcup\cal V$ and for each $V\in \cal V$ there are $F\in \mathcal F[X]$ and $U\in \tau_X$ with the property that $|F| \le n$ and $V = [F, U]$.  On the other hand, $\cal V$ is an *$\omega$-proper family* is $\mathcal F[X] = \bigcup \cal V$, and for every $V\in \cal V$ there exist $F\in \mathcal F[X]$ and $U \in \tau_X$ such that $V = [F, U]$.

**Obs:** If $X$ is a topological space, then for any $\omega$-proper is discrete. Additionally, if $\{\mathcal V_b \mid n \in \omega\setminus 1\}$ is a increasing sequence such that$\mathcal V_n$ is an $n$-proper family for each $n \in \omega\setminus 1$, then $\bigcup_{n \in\omega\setminus 1} \mathcal V_n$ is an $\omega$-proper family. 

**Lemma:** If $X$ is a topological space, $n\in \omega\setminus 1$, and $\cal U$ is a $n$-proper family, then $\cal U$ is discrete.

**Lemma:** If $\mathcal F[X]$ has a $1$-proper family and $\cal G$ is a open cover of $\mathcal F[X]$, then there's $1$-proper family inscribed in $\cal G$.

**Lemma:** If $X$ is a topological space, $n \in \omega\setminus 1$, $\cal G$ an open cover of $\mathcal F[X]$, $\cal U$ is a $n$-proper family inscribed on $\cal G$ and for each $F\in \mathcal F_{n+1}[X]\setminus \bigcup \mathcal U$ there's $O_F\in \tau_{\mathcal F[X]}$ with $F\in O_F$ such that $\{O_F \mid F \in \mathcal F_{n+1}[X] \setminus \bigcup \mathcal U\}$ is a celular family, then there's $\cal V$ a $(n+1)$-proper family that extends $\cal U$ and it is inscribed in $\cal G$.

**Cor:** If $n \in \omega\setminus 1$, $\cal G$ is an open cover of $\mathcal F[X]$, $\cal U$ is a$n$-proper family inscribed in $\cal G$ and $\mathcal F[X]$ is collectionwise Hausdorff, then there's $\cal V$ a $(n+1)$-proper family that extends $\cal U$ and it is inscribed in $\cal G$.

**Cor:** If $\cal G$ is an open cover of $\mathcal F[X]$ and $\mathcal F[X]$ is collectionwise Hausdorff, then there's an increasing sequence $\{\mathcal V_n \mid n \in \omega\setminus 1\}$ such that $\mathcal V_n$ is an $n$-proper family inscribed in $\cal G$ for all $n \in\omega\setminus 1$.

**Cor:** If $\cal G$ is an open cover of $\mathcal F[X]$ and $\mathcal F[X]$ is collectionwise Hausdorff, then there's an $\omega$-proper family inscribed in $\cal G$.

**Prop:** The following statements are equivalent for a topological space $X$.
- $X$ is weakly separated.
- $\mathcal F[X]$ has a $1$-proper family.
- $\mathcal F[X]$ has a $n$-proper family for some $n \in \omega\setminus 1$.

**Question:** Is it true, if $X$ is weakly separated, then for each $n \in \omega\setminus 2$ there's a $n$-proper family?

**Prop:** If $X$ is partially separated, then $\mathcal F[X]$ has $n$-proper families for every $n \in \omega\setminus 1$.

**Obs:** If $X$ is totally separated and $\{U_x \mid x \in X\}$ be the neighbourhood system that totally separates the space $X$, then $\{[\{x\}, U_x] \mid x\in X\}$ is an $n$-proper family for all $n \in \omega\setminus1$. 

# Paracompactness

**Cor:** If $\mathcal F[X]$ is collectionwise Hausdordd, then $\mathcal F[X]$ is paracompact.

**Def:** Let $X$ be a topological space. We will consider the following statements on the family $\{V_F \mid F\in \mathcal F[X]\}\subseteq \tau_X$:
1. $F \subseteq V_F$ for all $F\in \mathcal F[X]$. 
2. If $F, G \in \mathcal F[X]$ satisfy $F\subseteq V_G$ and $G\subseteq V_F$, then $F \cap G \neq \varnothing$.
3. If $F, G \in \mathcal F[X]$ satisfy $F\subseteq V_G$ and $G\subseteq V_F$, then $F \subseteq G$ or $G\subseteq F$.
If the family $\{V_F \mid F\in \mathcal F[X]\}$ is an *interlaced family* if it satisfies $(1)$ and $(2)$. On the other hand, we say that $\{V_F \mid F\in \mathcal F[X]\}$ is a *linearly interlaced family* if it satisfies $(1)$ and $(3)$. Lastly, we say that $\mathcal F[X]$ is  *interlaced* (*linearly interlaced*) if it has an interlaced (a linearly interlaced) family.

**Lemma:** If $X$ and $Y$ are topological spaces with $X\cap Y \neq \varnothing$. If $\mathcal F[X]$ and $\mathcal F[Y]$ are interlaced, then $\mathcal F[X\oplus Y]$ are interlaced.

**Cor:** If $n \in \omega\setminus 1$, $\{X_m \mid m < n\}$ is a family of topological spaces and $\mathcal F[X_m]$ is interlaces for each $m < n$, then $\mathcal F\left[\bigoplus_{m < n} X_m\right]$ is interlaced.

**Lemma:** If $\mathcal F[X]$ is linearly interlaced, then $\mathcal F\left[\bigoplus_{m < n} (X \times \{m\})\right]$ is linearly interlaced for every $n \in \omega\setminus 1$.

**Lemma:** If $\mathcal F[X]$ has an $\omega$-proper family, then $\mathcal F[X]$ is interlaced.

**Prop:** If $\mathcal F[X]$ is interlaced, then every open cover of $\mathcal F[X]$ has an $\omega$-proper refinement.

**Cor:** If $\mathcal F[X]$ is interlaced, then $\mathcal F[X]$ is ultraparacompact; in particular, is paracompact.

**Th:** The following statements are equivalent for a topological space $X$.
- $\mathcal F[X]$ is paracompact.
- $\mathcal F[X]$ is ultraparacompact.
- $\mathcal F[X]^n$ is paracompact for each $n \in \omega\setminus 1$.
- $\mathcal F[X]$ is collectionwise normal.
- $\mathcal F[X]$ is strongly collectionwise Hausdorff.
- $\mathcal F[X]$ is collectionwise Hausdorff.
- $\mathcal F[X]$ has an $\omega$-proper family.
- $\mathcal F[X]$ is interlaced.

**Prop:** Let $(S, <)$ be a partially ordered set, and suppose that $X = \bigcup_{s\in S}X_s$, where $\{X_s \mid s\in S\}$ is pairwise disjoint family such that $\bigcup_{t<s} X_t\in \tau_X$ for each $s\in S$. If for each $s\in S$ satisfies that $\mathcal F[X_s]$ is paracompact, then $\mathcal F[X]$ is paracompact.

**Obs:** Note that if $(S, <)$ is a partially ordered set satisfies that $\bigcup_{t\le s}X_t\in \tau_X$ for each $s\in S$, the $\bigcup_{t < s}X_t \in \tau_X$ whenever $s\in S$, because $$
\bigcup_{t < s} X_t = \bigcup_{t<s}\left(\bigcup_{r \leq t} X_r\right).
$$
**Cor:** If $X$ is partially separated, then $\mathcal F[X]$ is paracompact.

**Cor:** If $\cal A$ is a closed $\sigma$-locally finite cover of $X$ such that $\mathcal F[A]$ is paracompact for each $A\in \cal A$, then $\mathcal F[X]$ is paracompact.

**Cor:** If $\{A_x \mid x\in X\}\subseteq \mathcal P(X)$ satisfies that $x\in \text{int}(A_x)$ and $\mathcal F[A_x]$ is paracompact for each $x\in X$, then $\mathcal F[X]$ is paracompact.

**Cor:** Let $n \in \omega\setminus 1$ and $\{X_m \mid m < n\}$ is a family of topological space. If $\mathcal F[X_m]$ is paracompact whenever $m < n$, then $\prod_{m < n} \mathcal F[X_m]$ is paracompact.

**Lemma:** If $\mathcal F[X]$ is linearly interlaced, then $\mathcal F[X]$ is hereditarily paracompact.

**Th:** The following statements are equivalent for a topological space $X$.
- $\mathcal F[X]$ is hereditarily paracompact.
- $\mathcal F[X]^n$ is hereditarily paracompact for each $n \in \omega\setminus 1$.
- $\mathcal F[X]$ is hereditarily collectionwise Hausdorff.
- $\mathcal F[X]$ is linearly interlaced.

**Cor:** If $f: X \to Y$ is a condensation (bijective and continuous function) and $\mathcal F[Y]$ is paracompact (resp., hereditarily paracompact), then $\mathcal F[X]$ is paracompact (resp., hereditarily paracompact).

**Cor:** Let $f: X\to Y$ be a finite-to-one, closed, continuous, and surjective function. If $\mathcal F[X]$ is paracompact (resp., hereditarily paracompact), then $\mathcal F[Y]$ is paracompact (resp., hereditarily paracompact).

**Th:** The following statements are equivalent.
- $\mathcal F[X]$ is paracompact.
- $\mathcal F\langle X \rangle$ ([[Finite Vietoris Hyperspace]]) is weakly separated.

**Lemma:** Let $n\in \omega\setminus1$, and $\cal A$ be a clopen subset of $\mathcal F[X]$ such that $\mathcal F_n[X] \subseteq \cal A$. For each $F\in \mathcal F_{n+1}[X] \setminus \cal A$, let $U(F)\in\tau_X$ such that $F\subseteq U(F)$ and $[F, U(F)] \cap \mathcal A = \varnothing$. Let $\mathcal W := \{[F, U(F)] \mid \mathcal F_{n+1}[X] \setminus \mathcal A\}$. If $\cal W$ is a pairwise disjoint collection, then $\cal W$ is discrete. 

**Lemma:** Let $n\in \omega\setminus 1$ and $\cal A$ be a clopen subset of $\mathcal F[X]$ such that $\mathcal F_n[X]\subseteq \cal A$. For each $F\in \mathcal F_{n+1}[X] \setminus \cal A$, let $\{W_F(x) \mid x\in F\} \subseteq \tau_X$ such that:
- $x\in W_F(x)$ for each $x\in F$;
- $[F, \bigcup_{x\in F} W_F(x)] \cap \mathcal A = \varnothing$, and
- $[G, \bigcup_{x\in G} W_F(x)] \subseteq \mathcal A$, for each $G \subset F$.
If $[F, \bigcup_{x\in F} W_F(x)] \cap [H, \bigcup_{x\in H} W_H(x)] \neq \varnothing$ for some $F$ and $H$ in $\mathcal F_{n+1}[X]\setminus \cal A$, then each $W_F(x)$ contains exactly one element of $H$. 

**Prop:**  The following statements are equivalent for a topological space $X$.
- $\mathcal F_3[X]$ is paracompact.
- $\mathcal F_2[X]$ is paracompact.
- $\mathcal F_2[X]$ is collectionwise Hausdorff.
- $X$ is weakly separated. 

**Th:** Suppose that $\mathcal F[X]$ is paracompact (resp., hereditarily paracompact), then $\mathcal F[X^2]$ is paracompact (resp., hereditarily paracompact).

**Cor:** Suppose that $\mathcal F[X]$ and $\mathcal F[Y]$ are paracompact, then $\mathcal F[X\times Y]$ is paracompact.

**Th:** The following conditions are equivalent.
- $\mathcal F[X]$ is paracompact.
- $\mathcal F[X^2]$ is paracompact.
- $\mathcal F[X^n]$ is paracompact for each $n \in \omega\setminus 1$.
- $\mathcal F[X^n]^m$ is paracompact for each $n, m\in \omega\setminus 1$. 

**Th:** The following conditions are equivalent.
- $\mathcal F[X]$ is hereditarily paracompact.
- $\mathcal F[X^2]$ is hereditarily paracompact.
- $\mathcal F[X^n]$ is hereditarily paracompact for each $n \in \omega\setminus 1$.
- $\mathcal F[X^n]^m$ is hereditarily paracompact for each $n, m\in \omega\setminus 1$. 

**Th:** Let $n \in \omega\setminus 1$ and $\{X_m \mid m < n \}$ be a collection of topological spaces such that $\mathcal F[X_m]$ is paracompact for each $m < n$, then $\mathcal F\left[\prod_{m  < n} X_m^{k_m}\right]$ is paracompact for $\{k_m \mid m < n\} \subseteq \omega$.

# Metrization

**Obs:** If $\mathcal F[X]$ is metrizable, then $X$ is first countable.

**Th:** The following statements are equivalent for a topological space $X$. 
- $\mathcal F[X]$ is ultrametrizable.
- $\mathcal F[X]$ is metrizable.
- $\mathcal F[X]$ is paracompact and a Moore space.
- $\mathcal F[X]$ is paracompact and first countable.
- $\mathcal F[X]$ is paracompact and $X$ is first countable.
- $\mathcal F\langle X \rangle$ ([[Finite Vietoris Hyperspace]]) is weakly separated, and $X$ is first countable.

**Th:** The following conditions are equivalent.
- $\mathcal F[X]$ is metrizable.
- $\mathcal F[X^2]$ is metrizable.
- $\mathcal F[X^n]$ is metrizable for each $n \in \omega\setminus 1$.
- $\mathcal F[X^n]^m$ is metrizable for each $n, m\in \omega\setminus 1$. 

**Cor:** If $X$ is partially separated and first countable, then $\mathcal F[X]$ is metrizable.

**Th:** The following statements are equivalent for a topological space $X$. 
- $\mathcal F[X]$ is metrizable.
- $\mathcal F[X]$ is a Lašnev space.