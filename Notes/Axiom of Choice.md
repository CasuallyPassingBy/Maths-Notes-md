---
tags:
  - Axioms
  - SetTheory
  - MeasureTheory
  - FunctionalAnalysis
  - Topology
  - Analysis
  - GroupTheory
---
Subjects: [[Set Theory]]
Links: [[ZF Axioms]]
# Axiom of choice:
$$ \forall X \left[ \varnothing \notin X \implies \exists f \colon X \rightarrow \bigcup X\quad \forall A \in X \, ( f(A) \in A ) \right] \,.$$
## The Axiom of Choice and its Equivalents

All the results that the Axiom of choice in this section will be noted with an asterisk

********Def:******** Let $S$ be a system of sets. A function $g$ defined on $S$ is called a _choice function_ for $S$ if $g(X) \in X$ for all nonempty $X \in S$

********Th:******** A set $A$ can be well-ordered iff the set $\mathcal P(A)$ has a choice function.

********Th:******** Every finite system of sets has a choice function

### Axiom of choice
There exists a choice function for every system of sets

**Th:** The following statements are equivalent
- (The Axiom of Choice) There exists a choice function for every system of sets
- Every partition has a set of representatives
- If $\langle X_i \mid i \in I\rangle$ is an indexed system of nonempty sets, then there us a function $f$ such that $f(i) \in X_i$ for all $i \in I$

Th:* Every infinite set a countable subset. Equivalently, a set $A$ is infinite iff it is Dedekind Infinite. Every infinite set is equipotent to some of its proper subsets. Equivalently, Dedekind finite sets are precisely the finite sets.

_Th:_* For every infinite set $S$ there exists a unique aleph $\aleph_ \alpha$ such that $|S| = \aleph_ \alpha$

Th:* For any sets $A$ and $B$ either $|A| \le |B|$ or $|B|\le |A|$

Cor:* The set of all real numbers is not the union of countable many countable sets

Cor:* The ordinal $\omega_1$ is not the supremum of a countale set of countable ordinals

Th: $2^{\aleph_ 0} \ge \aleph_ 1$

Th:* If $f$ is a function and $A$ a set, then $|f[A]| \le |A|$

Th:******_* If $|S| \le \aleph_ \alpha$ and for all $A \in S$, $|A| \le \aleph_ \alpha$, then $|\bigcup S| \le \aleph_ \alpha$

**Def:** A system of sets $A$ has **finite characters** if $X \in A$ iff every finite subset of $X$ belongs to $A$.

********Th:******** The following statements are equivalent: 
- Set theory:
	- (The Axiom of Choice) There exists a unique choice function for every system of sets
	- (The Well-Ordering Principle) Every set can be well-ordered
	- (Zorn’s Lemma) If every chain in a ordered set has an upper bound, then the partially orderd set has a maximal element
	- For all $(A, \le )$, the set of all chains of $(A, \le )$ has a $\subseteq$-maximal element
	- If $A$ is s system of sets such that, $B \subseteq A$ which is linearly ordered by $\subseteq$, $\bigcup B \in A$ then $A$ has a $\subseteq$-maximal element
	- (Tukey’s Lemma): Every system of sets of finite characters has a $\subseteq$-maximal element
	- (Hausdorff maximal principle): Every partially ordered set has a maximal chain. Equivalently, in any partially ordered set, every chain can be extended to a maximal chain
- Alegbra:
	- Every vector space has a [[Bases and Dimension|basis]]
- Point-set Topology:
	- (Tychonoff's theorem): The Cartesian Product of any family of compact topological spaces is compact

Th:* If $(A, \preceq)$ is linear ordering such that $|\{ y \in A\mid y \preceq x\} |<\aleph_\gamma$ for $x \in A$, then $|A| \le \aleph_\gamma$

Th:* The following distributive laws:
$$ \bigcap_{t \in T}\left(\bigcup_{s \in S} A_{t, s}\right) = \bigcup_{f \in S^T} \left( \bigcap_{t \in T} A_{t, f(t)}\right) $$$$ \bigcup_{t \in T}\left(\bigcap_{s \in S} A_{t, s}\right) = \bigcap_{f \in S^T} \left( \bigcup_{t \in T} A_{t, f(t)}\right) $$

Th:* Every ordering $\preceq$ on $A$, there is linear orderingf $\le$ on $A$ such that $a \preceq b$ implies $a \le b$ for all $a, b \in A$, i.e. every partial ordering can be extended into a linear ordering.

### Principle of Dependent Choice

If $R$ is a binary relation on $M \ne \varnothing$ such that for each $x \in M$ there is $y \in M$ for which $xRy$, then there is a sequence ${\langle x_n \mid n < \omega\rangle}$ such that $x_n R x_{n+1}$ holds for $n < \omega$

### Axiom of Countable Choice

Every countable system of sets has a choice function

For what I gathered from wikipedia and other people when I looked into the axiom of choice. We have that

$$ AC_\omega < DC < AC $$

where $AC_\omega$ is the Axiom of Countable Choice; $DC$ is the Principle of Dependent Choice, and $AC$ is the Axiom of Choice. 

A use of $AC_\omega$ is actually to prove that the countable union of countable sets is countable. This is because we need to choose an surjection from $\Bbb N$ to each of the sets and thus choose countably many times. 

(Probably need to look further into it, but seems really abstract since I think is quite an avanced set theory)

---

# The Use of the Axiom of Choice in Mathematics

**************Closure Points.************** According to the usual definition, a sequence of real numbers $\langle x_n \mid n \in \Bbb N\rangle$ ************_converges to $a \in \Bbb R$_ if for every $\varepsilon >0$, there’s $N\in \Bbb N$ such that $|x_n -a| < \varepsilon$ , for $n \ge N$. We can define a closure/acumulation point as

1. $a \in \Bbb R$ is an accumulation point of $A$ iff there exists a sequence $\langle x_n \mid n \in \Bbb N\rangle$ with all values in $A$, which converges to $a$, and $x_n \ne a$ for all $n \in \Bbb N$
2. $a \in \Bbb R$ is an accumulation point of $A$ iff for every $\varepsilon >0$ there exists $x \in A$ such that ${0 < |x-a| < \varepsilon}$

It is easy to see that $1.$ implies $2.$, since if we know that the sequence exists, then we can easily verify the other. Checking that $2.$ implies $1.$, actually we need the Axiom of Countable Choice, at least.

Similarly in the case of continuity

The standard definition of continuity of real-valued function of real variable is defined as:

1. $f: \Bbb R \to \Bbb R$ is _********continuous********_ at $a \in \Bbb R$ iff for every $\varepsilon >0$, there exists $\delta >0$ such that $|f(x)-f(a)| <\varepsilon$, whenever $|x-a|< \delta$
2. $f: \Bbb R \to \Bbb R$ is _********continuous********_ at $a \in \Bbb R$ iff for every sequence $\langle x_n \mid n \in \Bbb N\rangle$ which converges to $a$, the sequence $\langle f(x_n) \mid n \in \Bbb N\rangle$ converges to $f(a)$

Similarly $1.$ implies $2.$, but $2.$ implies $1.$ is not as simple, since we need the Axiom of Countable Choice or something stronger to prove it.

### Hamel Basis
If we consider the real numbers as a vectors space over the field of rational numbers. This vector space has a basis, called a **Hamel basis** for $\Bbb R$. In other words, a set $X \subseteq \Bbb R$ is a **Hamel basis** for $\Bbb R$ if every $x \in \Bbb R$ can be expressed in a unique way as

$$ x = \sum_{i = 1}^n r_i x_i $$

for some mutually exclusive $x_1, \dots, x_n \in X$ and some nonzeroo rational numbers $r_1, \dots, r_n$.

Def: A function $f: \Bbb R \to \Bbb R$ is called additive if $f(x+y) = f(x)+f(y)$ for all $x, y \in \Bbb R$.

Easy computations show that $f(x) = a\cdot x$, for $x \in \Bbb Q$, with $a = f(1)$. It is easy to think that $f(x) = a \cdot x$ for all $x \in \Bbb R$, but this is false if we assume the Axiom of Choice. For ease, of notation, we define $f_a(x) = a\cdot x$, for all $x \in \Bbb R$

_***Th_:**** There exists an additive function $f: \Bbb R \to \Bbb R$ such that $f \ne f_a$ for all $a \in \Bbb R$

### Hahn-Banach Theorem

A function defined on a vector space $V$ over the field $\Bbb R$ of real numbers and with values in $\Bbb R$ is called a **linear functional** on $V$ if

$$ f( \alpha \cdot u + \beta \cdot v ) = \alpha \cdot f(u) + \beta\cdot f(v) $$

holds for all $u,v \in V$ and $\alpha, \beta \in \Bbb R$

A function $p$ defined on $V$ and with values in $\Bbb R$ is called a **sublinear functional** on $V$ if

$$ p(u+v) \le p(u)+p(v) $$

and

$$ p(\alpha \cdot u ) = \alpha \cdot p(u) $$

for all $u, v \in V$ and $\alpha \in \Bbb R$

**Th (Hahn-Banach Theorem):** Let $p$ be a sublinear functional on the vector space $V$, and let $f_0$ be a linear functional defined on a subspace $V_0$ of $V$ such that $f_0(u) \le p(u)$ for all $u \in V_0$. Then there is a linear functional $f$ defined on $V$ such that $f_0 \subseteq f$ and $f(v) \le p(v)$ for all $v \in V$

This is an important theorem on functional analysis.

## The Measure Problem
Ideally, we would like a $\sigma$-measure $\mu: \mathcal P(\Bbb R) \to [0, \infty]$, with the following properties:
- $\mu([a,b]) = b-a$
- $\mu(\Bbb R) = \infty$
- if $a \in \Bbb R$, $A\subseteq \Bbb R$, and $\mu(A+a) = \mu(A)$ 

Th:* There is no measure $\mu: \mathcal P(\Bbb R) \to [0, \infty]$, with the following properties:
- $\mu([a,b]) = b-a$
- $\mu(\Bbb R) = \infty$
- if $a \in \Bbb R$, $A\subseteq \Bbb R$, and $\mu(A+a) = \mu(A)$

Cor:* Let $\mu$ be a measure on a $\sigma$-algebra $\mathcal S$ of subsets of $\Bbb R$ such that
- $\mu([a,b]) = b-a$
- $\mu(\Bbb R) = \infty$
- if $a \in \Bbb R$, $A\subseteq \Bbb R$, and $\mu(A+a) = \mu(A)$
Then there exists sets of real numbers which are not $\mu$-measurable