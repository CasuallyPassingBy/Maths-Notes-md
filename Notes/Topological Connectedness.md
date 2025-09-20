---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Continuous Functions and Homeomorphims]], [[Sum Topology]], [[Connected Sets in Rn]], [[Perfect and Connected Sets in R]]

**Def:** A topological space $X$ is said to be *disconnected* if it can be expressed as the union of two disjoint, nonempty open subsets. Any such subsets are said to *disconnect* $X$. If $X$ is not disconnected, it is said to be *connected*. Note that the empty set is connected.

**Prop:** A topological space $X$ is connected iff the only subsets of $X$ that are clopen in $X$ are $\varnothing$ and $X$ itself.

**Prop:** Suppose $X$ is a nonempty connected space. Then every continuous map from $X$ to a discrete space is constant.

**Cor:** Suppose $X$ is a connected topological space, and $\sim$ is an equivalence relation such that every equivalence class is open. Then there's exactly one equivalence class, namely $X.$

**Cor:** Let $X$ be a topological space. $X$ is disconnected iff there exists a nonconstant continuous function from $X$ to a discrete space $\{0, 1\}$.

**Cor:** Let $X$ be a topological space. $X$ is disconnected iff it is a homeomorphic to a disjoint union of two or more nonempty spaces. 

**Th:** Let $X$ and $Y$ be topological spaces, and let $f:X \to Y$ be a continuous map. If $X$ is connected, then $f[X]$ is connected.

**Cor:** Every space homeomorphic to a connected space is connected.

**Properties of Connected Spaces:**
- Suppose $X$ is any space $U$ and $V$ are disjoint open subsets of $X$. If $A$ is a connected subset of $X$ contained in $U \cup V$, then either $A \subseteq U$ or $A \subseteq V$.
- If $X$ is a space that contains a dense connected subset, then $X$ is connected.
- Suppose $X$ is any space and $A\subseteq X$ is connected. Then $\overline A$ is connected, as is any subset $B$ such that $A\subseteq B \subseteq \overline A$. 
- Let $X$ be a space, and let $\{B_\alpha \mid \alpha  <\kappa\}$ be a collection of connected subspace of $X$ with a point in common. Then $\bigcup_{\alpha <\kappa} B_\alpha$ is connected.
- Every product of finitely many connected spaces is connected.
- Every quotient space of a connected space is connected.

**Prop:** If $M$ is a connected manifold with nonempty boundary, then $D(M)$ is connected, where $D(M)$ represents its [[Adjunction Topology#^f1ddca|double]].

**Prop:** A nonempty subset of $\Bbb R$ is connected iff it is a singleton or interval. 

**Cor  (Intermediate Value Theorem):** Suppose $X$ is a connected topological space and $f:X \to \Bbb R$ is continuous. If $p,q \in X$, the $f$ attains every value between $f(p)$ and $f(q)$. 

**Obs:** For $n > 1$, $\Bbb R^n$ is not homeomorphic to any subset of $\Bbb R$. This is because $U\subseteq \Bbb R$ is open and $x\in U$, then $U \setminus \{x\}$ is not connected.

**[[Topological Manifolds#^ca2c82|Invariance of Dimension]], $1$-dimensional Case:** A nonempty topological space cannot tb both a $1$-manifold and $n$-manifold for $n> 1$. 

**[[Topological Manifolds#^cd5f36|Invariance of Boundary]], $1$-dimensional Case:** Suppose $M$ is a $1$-dimensional manifold with boundary. Then a point of $M$ cannot be both a boundary point and an interior point. 

## Components

**Def:** Let $X$ be a topological space. A *component of $X$* is  maximal nonempty connected subset of $X$, that is, nonempty subset that is properly contained in any other connected subset.

**Prop:** If $X$ is any topological space, its components form a partition of $X$. 

**Prop:** Let $X$ be a nonempty topological space.
- Each component of $X$ is closed in $X$
- Any nonempty connected subset of $X$ is contained in a single component.


Since connectedness is a global property we can also [[Local Connectedness]]