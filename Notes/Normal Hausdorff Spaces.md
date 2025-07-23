---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Separation Axioms]], [[Fréchet Spaces]], [[Separation of Sets]], [[Topological Subspaces]], [[Hausdorff Spaces]], [[Continuous Functions and Homeomorphims]], [[Limit and Colimit Topology]]

**Def:** A topological space $(X, \tau)$ is *normal* if for any two disjoint closed subsets of $X$, $F$ and $G$ , there are disjoint open sets $U$ and $V$ such that $F \subseteq U$ and $G \subseteq V$.

**Def:** A topological space $(X,\tau)$ is a $T_4$ *space* if it is normal and a $T_1$ space. 

**Obs:** A $T_4$ space is also $T_0, T_1, T_2,$ and $T_3$. 

**Prop:** Let $(X, \tau)$ a $T_1$ space. The following are equivalent
- The space $X$ is $T_4$ 
- for any closed subset $F\subseteq X$ and $A\in \tau$ such that $F \subseteq A$, then there's $B \in \tau$ such that $F \subseteq B \subseteq \text{cl}(B) \subseteq A$.
- For every $U, V\in \tau$ such that $U\cup V = X$, then there are closed subsets $F$ and $G$ of $X$, such that $F\subseteq U$, $G\subseteq V$, and $F\cup G = X$.

**Urysohn's Lemma:** For every pair $A,B$ of disjoint closed subsets of a $T_4$ space $X$ there exists a function $f: X \to I$ such that $f(x) = 0$ for $x\in A$ and $f(x) = 1$ for $x\in B$. 

**Cor:** A topological space $X$ a $T_4$ space iff for any two disjoint closed set $F$ and $G$, there exits a continuous function $f:X\to I$ such that $f[F] = \{0\}$ and $f[G] =\{1\}$.

**Cor:** A subset $A$ of a $T_4$ space $X$ is a closed $G_\delta$-set iff there exists a continuous function $f:X\to I$ such that $A = f^{-1}\{0\}$. 

**Cor:** A subset $A$ of a $T_4$ space $X$ is an open $F_\sigma$-set iff there exists a continuous function $f:X\to I$ such that $A = f^{-1}[(0, 1]]$. 

**Obs:** Every zero set is a closed $G_\delta$ and a co-zero set is an open $F_\sigma$. 

Meaning that closed $G_\delta$ and open $F_\sigma$ on a $T_4$ space are precisely the zero sets and co-zero sets.

**Lemma:** If $X$ is a $T_1$ space and for every closed set $F \subseteq X$ and every open $W \subseteq X$ that contains $F$ there exists a sequence $W_0, W_1, W_2, \dots$ of open subsets such that $F \subseteq \bigcup_{n <\omega}W_n$ and $\text{cl}(W_n) \subseteq W$ for $n <\omega$, then $X$ is a $T_4$ space. 

**Th:** Every second countable $T_3$ space is a $T_4$ space.

**Th:** Every countable $T_3$ space is a $T_4$ space.

**Th:** Let $X$ be a topological space. $X$ is normal iff every [[Special Types of Collections in Topology|point-finite]] open cover of $X$ admits a [[Shrinking Space|shrinking]].

**Th:** If $X$ is a normal space and $f: X\to Y$ is a closed, continuous and surjective function, then $Y$ is normal.

**Prop:** If $Y$ is a normal space and $f: X \to Y$ is a closed, continuous and surjective function. the $X$ is normal.

**Prop:** Normality is hereditary with respect to closed sets.

**Prop:** Normality is hereditary with respect to $F_\sigma$ sets.

**Tietze Extension theorem:** Every continuous function from a closed subspace $M$ of $T_4$ space $X$ to $[0, 1]$ or $\Bbb R$ is continuously extendable over $X$.

**Cor:** If a continuous mapping of a dense subset of a topological space $X$ to a $T_2$ space $Y$ is continuously extendable over $X$, then the extension is uniquely determined by $f$.

**Cor:** Let $f$ be a continuous mapping fo a closed set $F$ of a normal space $X$ into $\mathbb S^n$. Then we can continuously extend $f$ over an open cover of $X$ which contains $F$. 

**Cor:** No separable $T_4$ space contains a closed discrete subspace of cardinality $\frak c = 2^{\aleph_0}$.

**Prop:** Let $\cal U$ be a locally finite open covering of a normal space $X$. Then $\cal U$ has a $\sigma$-discrete refinement and a $\sigma$-discrete closed refinement.

**Th:** For every countable discrete $\{F_n : n <\omega\}$ of closed subsets of a $T_4$ space $X$ there exists a family $\{U_n : n < \omega\}$ of open subsets of $X$ such that $F_n \subseteq U_n$ for $n <\omega$ and $\text{cl}(U_n) \cap \text{cl}(U_m) = \varnothing$ for $n \neq m$. 

**Th:** Let $X$ be a topological space. If $\{X_n \mid n <\omega\}$ is an increasing family of closed normal subspaces of $X$ such that $X = \bigcup_{n < \omega} X_n$, then  $X$ is normal. 

This result can be put in the languages of category theory theore as:

If $(i_n: X_n \to X_{n+1})_{n < \omega}$ is a sequence of closed embeddings between normal spaces, then the colimit $\varinjlim X_n$ is also normal.

# Hereditarily Normal

**Def:** A space $X$ is hereditarily normal if every subspace is normal. A space $X$ is $T_5$ if it is hereditarily normal and $T_1$. 

**Obs:** $T_5$ is a hereditary property.

**Th:** For every $T_1$-space $X$ the following conditions are equivalent:
- The space $X$ is $T_5$.
- Every open subspace of $X$ is $T_4$.
- For every pair of separated sets $A, B \subseteq X$, then $A, B$ are *separated by neighbourhoods*.

**Lemma:** The space $[0, \omega)^{\omega_1}$ is not a normal space.

**Cor:** Let $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ be a family of not indiscrete topological spaces. If $\kappa > \omega$, then $\prod_{\alpha < \kappa} X_\alpha$ is not hereditarily normal.

One can be tempted to compare [[collectionwise normal spaces]] to hereditarily normal spaces, but these properties are completely independent of each other.

****

# Perfect Normality

**Def:** A topological space $X$ is called a *perfectly normal space* if $X$ is a normal space and every closed subset of $X$ is a $G_\delta$-set. 

**Def:** A topological space $X$ is called a $T_6$ space if $X$ is perfectly normal and $T_1$. 

**Obs:** A second countable $T_4$ space is a $T_6$ space. 

**Vedenisoff Theorem:** For a $T_1$ space the following conditions are equivalent:
- The space $X$ is $T_6$.
- Open subsets of $X$ are co-zero sets
- Closed subsets of $X$ are zero sets
- For a pair of disjoint closed subsets $A, B \subseteq X$, then they are precisely separated by a continuous function. 

**Th:** The class of $T_6$ spaces are invariant under continuous closed mappings.

**Prop:** $T_6$ is hereditary.