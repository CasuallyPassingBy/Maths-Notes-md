---
tags:
  - Analysis
  - Topology
---
Subjects: [[Metric and Normed Spaces]], [[Topology]]
Links: [[Continuity on Metric Spaces]], [[Topological Characterization of Continuity in Rn]], [[Open and Closed Sets in R]], [[Metric Spaces]]

**Def:** Given a metric space $(X, d)$ we can define the set that have a distance less than a real number $r$ from $x \in X$, it is called *************_the open ball with center $x$ and radius $r$:_

$$ B_r(x)=B(x, r) = \{y \in X \mid d(x,y) < r\} $$

We can reformulate the idea of continuity as, let $\phi: X \to Y$ be _continuous at $x_0$_ if for every ${\varepsilon >0}$, there’s a $\delta >0$ such that

$$ \phi(B_X(x_0, \delta)) \subseteq B_Y(\phi(x_0), \varepsilon) $$

**Def:** Given $(X, d)$ a metric space and $A\subseteq X$, let $x \in X$ is called an **interior point** if there’s $\varepsilon>0$such that $B_X(x, \varepsilon )\subseteq A$. The set of all interior points of $A$ is called the **interior of $A$ in** $X$, denoted as $\operatorname{int}_X(A)$, or simply $\operatorname{int}(A)$. We say that $A$ is **open on $X$** if $A = \operatorname{int}(A)$

**Def**: In any metric space $X=(X, d)$, the open ball

$$ B_X(x_0, \varepsilon) =\{ x\in X \mid d(x_0, x) < \varepsilon\} $$

with center at $x_0$ and radius of $\varepsilon$ is an open set of $X$

**Prop**: The interior $\operatorname{int}(A)$ of any subset $A$ of $X$ is open in $X$

**Def**: A point $x \in X$ is called a _**limit point**_ of $A$ if $B_X(x, \varepsilon) \cap A\ne \varnothing$ for all $\varepsilon>0$. The set of all limit points of $A$ is called the **closure of $A$ on $X$**, and it is denoted as $\operatorname{cl}_X(A)$, ($\operatorname{cerr}_X(A)$) or simply $\overline A$. We say that $A$ is **closed** in $X$_if $A = \overline A$

**Def**: The closed ball on $X$ with center $x_0$ and radius $\varepsilon >0$ is the set

$$ \overline B_X(x_0,\varepsilon) =\{x \in X \mid d(x, x_0) \le \varepsilon\} $$

is a closed set in $X$

**Prop**: For any subset $A$ of $X$, a metric space, we have that

$$ X \setminus \overline A = \operatorname{int}(X\setminus A) $$

In consequence, $A$ is closed in $X$ iff $X\setminus A$ is open in $X$

**Prop**: The closure $\overline A$ of any subset $A$ of $X$ is closed in $X$

**Prop**: We have some important properties of the interior and closure of sets, such as:
- If $A \subseteq B$, then $\operatorname{int}(A) \subseteq \operatorname{int}(B)$ and $\overline A \subseteq \overline B$
- $\operatorname{int}(A) \cap \operatorname{int}(B) = \operatorname{int}(A\cap B)$
- $\operatorname{int}(A) \cup \operatorname{int}(B) \subseteq \operatorname{int}(A\cup B)$
- $\overline{ A\cup B} = \overline A \cup \overline B$
- $\overline{A \cap B} \subseteq \overline A \cap \overline B$

**Prop**: If $V =(V, \| \cdot \|)$ is a normed space, then the closure of the open ball $B(v_0, \varepsilon)$ is the closed ball $\overline B(v_0, \varepsilon)$. In other words in normed spaces $\overline{B(v_0, \varepsilon)} = \overline B(v_0, \varepsilon)$.

**Th**: Let $X$ and $Y$ be metric spaces, and $\phi: X \to Y$ a function. Then the following affirmations are equivalent:
- $\phi: X \to Y$ is continuous
- $\phi^{-1}[U]$ is open in $X$ for all open substet $U$ of $Y$
- $\phi^{-1}[C]$ is closed in $X$ for all closed substet $C$ of $Y$

**Th**: In any metric space $X=(X, d)$ it is true that:

- $\varnothing$ and $X$, are open in $X$
- Let $\{ U_\lambda \mid \lambda \in \Lambda\}$ be a family of open sets in $X$, then $\bigcup\limits_{\lambda \in \Lambda} U_ \lambda$ is also open in $X$
- Let $U$ and $V$ be open sets in $X$, then $U \cap V$ is also open in $X$

Which means, that we have a topological space from a metric space.

**Def**: From this we can derive the rest of the topological definitions such as, the boundary of a set ${A \subseteq X}$, as $\partial A =\operatorname{Fr}(A) := \overline A\setminus \operatorname{int}(A)$.

**Prop**: From this we can derive the useful equivalence that $x \in \partial A$, iff for every $r >0$, $B(x, r) \cap A \ne \varnothing$ and $B(x,r)\setminus A \ne \varnothing$ . Finally we get that $\partial A = \overline A \cap \overline {(X\setminus A)}$. From this we know that for every $A \subseteq X$, that $\partial A$ is closed. From the definition we can see that $\partial A \cap \operatorname{int}(A) = \varnothing$, and that $\partial A \cup \operatorname{int}(A) = \overline A$. Lastly, we have that if $A$ is open or closed, then $\operatorname{int}(\partial A) = \varnothing$.

**Prop**: Let $V=(V, \| \cdot \|)$ be a normed vector space, and we define the set ${S(v_0, \varepsilon) := \{ v \in V\mid \|v-v_0\| = \varepsilon\}}$, referring to the sphere with center $v_0$ and radius $\varepsilon$, then

$$ \partial(B(v_0, \varepsilon)) = S(v_0, \varepsilon) $$

**Def**: We can also define the exterior of a set $A \subseteq X$, as $\operatorname{ext}(A) := \operatorname{int}(X \setminus A)$

**Prop**: Then we can see that $\operatorname{ext}(A) = X\setminus \overline A$, and $\operatorname{int}(A) \sqcup \partial A \sqcup \operatorname{ext}(A) = X$, and all of those are pairwise disjoint.

## Topology of Submetric Spaces
**Def**: Let $(X, d)$ be a metric space, and $A$ be a subset of $X$, we define for any $x, y \in A$,

$$ d_A(x, y) = d(x, y) $$

It is clear that this is a metric on $A$, that is called **the induced metric** by $d$. The set $A$ with this metric is called a ******************_metric subspace of $X$_

**Prop**: Let $Y \subseteq X$, from this we can check several important properites, such as
- $B_Y(y,\varepsilon ) = Y\cap B_X(y, \varepsilon)$
- $\operatorname{cl}_Y(A) = Y \cap \operatorname{cl}_X(A)$
- $Y\cap \operatorname{int}_X(A) \subseteq \operatorname{int}_Y(A)$
- $\operatorname{Fr}_Y (A) \subseteq Y \cap \operatorname{Fr}_X(A)$