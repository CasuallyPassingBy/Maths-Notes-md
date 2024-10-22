---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Real Numbers]]
## Open Sets

**Def:** We define an $\varepsilon$ -neighborhood of $a$ is the set

$$ B_\varepsilon(a) := \{x \in \Bbb{R}\mid |x-a|<\varepsilon\} $$

**Def:** A set $U \subseteq \Bbb{R}$ is called *open* if for all points $a \in U$ there exist an $\varepsilon$-neighborhood ${B_\varepsilon(a) \subseteq O}$

********Th:******** The union of an arbitrary collection of open sets is open.

The intersection of a finite collection of open sets is open

$\Bbb{R}$ and $\varnothing$ are open sets

Thus we just defined a topology on $\Bbb{R}$ through the norm $|\cdot |$.

Every system of mutually disjoint open intervals in $\Bbb R$ is at most countable

Every nonempty open set of real numbers has cardinality $2^{\aleph_0}$ 

There are $2^{\aleph_0}$ open sets
## Closed sets

**Def:** A point $x$ is a _**************limit point**************_ of a set $A$, if for every $\varepsilon$ -neighborhood of $x$ intersects the set $A$ at some other point other than $x$. This can be written with mathematical symbols as

$$ \forall \varepsilon >0 \exists y \ne x[y \in A\cap B_\varepsilon (x)] $$

**Th:** A point $x$ is a limit point of a set $A$ iff $x = \lim_{n \to \infty} a_n$ for some sequence $(a_n)_{n \in \Bbb{N}} \subseteq A$ satisfying $a_n \ne x$ for all $n \in \Bbb{N}$.

**Def:** A point $a \in A$ is an _isolated point_ of $A$ if is not a limit point of $A$. The set of all limit points of $A$ is denoted as $A'$. The set of isolated points of $A$ is $A\setminus A'$. 

********Def:******** A set $F \subseteq \Bbb{R}$ is _closed_ if it contains its limit points, meaning $F' \subseteq F$ . This notion in $\Bbb{R}$ is equivalent to the topological definition of closed sets.

**Th:** A set $F\subseteq \Bbb{R}$ is closed iff for every Cauchy sequence contained in $F$ has a limit that is also contained in $F$.

********Th (Density of $\Bbb Q$ in $\Bbb{R}$):** For every $y \in \Bbb{R}$, there exists a sequence of rational numbers that converges to $y$.

********Def:******** Given $A \subseteq \Bbb{R}$, the *closure* of $A$ is defined as $\operatorname{cl}(A) = \overline A = A \cup A'$

**Th:** For any $A \subseteq \Bbb{R}$, the closure $\operatorname{cl}(A)$ is a closed set and is the smallest closed set containing $A$.

**Th (Ensuring our definitions of open and closed correspond to the ones topologically):** A set $U$ is open iff $\Bbb{R} \setminus U$ is closed. Likewise, a set $F$ is closed iff $\Bbb{R} \setminus F$ is open.

**Th:** The union of a finite collection of closed sets is closed

The intersection of an arbitrary collection of closed sets is closed

$\Bbb{R}$ and $\varnothing$ are closed sets.

**Th:** For $A \subseteq \Bbb R$, then $A'$ is closed. 

