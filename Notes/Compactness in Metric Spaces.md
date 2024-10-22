---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Compact Sets in R]], [[Compact Sets in Rn]], [[Continuity on Metric Spaces]], [[Topology on Metric Spaces]]

**Def**: A **cover** of $A$ on $X$ is a family ${\frak C}=\{ X_i \mid i \in \cal I\}$ of substets of $X$ such that

$$ A \subseteq \bigcup {\frak C} = \bigcup_{i \in \cal I} X_i $$

If additionally, $X_i$ is open in $X$ for all $i \in \cal I$, we say that $\frak C$ is an **open cover** of $A$ on $X$. A subset $\frak C'$ of $\frak C$ that is also a cover of $A$ is called an **subcover** of $A$.

**Def**: A subset $K$ of $X$ is **compact** if for every open cover $\frak C = \{ X_i \mid i \in \cal I\}$ of $K$ on $X$ has a finite subcover, i.e., there exists $X_{i_1}, \dots, X_{i_m }\in \frak C$ such that

$$ K \subseteq \bigcup_{k = 1}^m X_{i_k} $$

A set where every sequence $x_\bullet: \Bbb N \to K$, has a convergent subsequence in $K$ is called sequentially compact.

**Th**: A compact set is sequentially compact.

### Lebesgue Number Lemma
If the metric space $(X,d)$ is compact and an open cover of $X$ is given, then there exists a number $\delta > 0$ such that every subset of $X$ having diameter less than $\delta$ is contained in some member of the cover. Such a number $\delta$ is called a Lebesgue number of this cover.

The theorem above is used to prove by contradiction that: A sequentially compact set is compact.

**Def**: A set $A$ on $X$ is **bounded** if there exist $x \in X$ and $M>0$ such that $A \subseteq B_X(x, M)$.

**Prop**: Let $K$ is a compact subset of $X$, then $K$ is closed and bounded

**Prop**:Let $K$ is a compact subset of $X$. If $C\subseteq K$, and $C$ is closed on $X$, then $C$ is compact.

**Prop**:If $\phi: X\to Y$ is continuous and $K$ is a compact set of $X$, then $\phi[K]$ is a compact set of $Y$

**Cor**: If $K$ is a compact metric space, and $\phi:K \to X$ is continuous, then $\phi$ is bounded

**Th**: Let $K$ be a compact metric space,and $Y$ be a metric space. Then every continuous function ${\phi: K \to Y}$ is also uniformly continuous.

**Chad lemma:** The cube

$$ Q = [-r, r]^n $$

is compact.

### Heine-Borel Theorem
Let $K$ be a subset of $\Bbb R^n$. Then, $K$ is compact iff $K$ is closed and bounded. We can actually then know that if a set $K$ of a finite dimensional normed space $V$, is compact iff $K$ is closed and bounded by the isometric equivalence to some $\Bbb R^n$

### Reisz Lemma
Let $X$ be a normed space, $Y$ be a closed linear subspace of $X$, and $\alpha \in (0,1)$. Then there’s $x_\alpha \in S_X$ ($\|x_\alpha \| =1$), such that

$$ \|x_\alpha -y\| > \alpha \qquad \forall y \in Y $$

### Reisz Theorem
The unit sphere $S_V= \{ v \in V \mid \|v \| = 1\}$ is compact iff $\dim V<\infty$.

**Cor**: The closed ball $\overline B(0,1) =\{ v \in V \mid \|v\| \le 1\}$ is compact iff $\dim V<\infty$.

**Cor**: for any $K$ be a compact set of $V$ and any $\delta>0$ it follows that

$$ \hat K = \bigcup_{v \in K}\overline B(x, \delta) $$

is compact iff $\dim V <\infty$



$(M, d)$ be a metric space, then the following are equivalent:
- $(M, d)$ is [[Compactness|compact]]
- $(M, d)$ is [[Sequentially compactness|sequentially compact]]
- $(M, d)$ is [[Complete Metric Spaces|complete]] and [[Total Boundedness|totally bounded]]
- $(M, d)$ is [[Countable compactness|countably compact]]
- $(M, d)$ is [[Psuedocompactness|pseudocompact]]
