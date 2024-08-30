---
tags:
  - SetTheory
---
Links: [[Pi-System]]

Let $S$ be a nonempty set. A *filter* on $S$ is a collection $F$ of subsets of $S$ that satisfies the following conditions:
- $S \in F$, $\varnothing \notin F$
- If $X, Y \in F$ then $X \cap Y \in F$
- If $X \in F$, and $X \subseteq Y \subseteq S$, then $Y \in F$

A trivial example of a filter on $S$ is the collection $F = \{S\}$ that consists only of the set $S$ itself. This *trivial filter* on $S$ is the smallest filter on $S$; it is included in every filter on $S$.

Let $A$ be a nonempty subset of $S$, and let us consider the collection $$
	F = \{X \subseteq S\mid A \subseteq X \}
$$The collection $F$ is called the *principal filter* on $S$ *generated* by $A$. 

If we set $A = \{a\}$, where $a \in S$, the principal filter $$ F = \{X\subseteq S \mid a \in X\}$$is *maximal*: there is no filter $F'$ on $S$ such that $F\subset F'$. We get that if $A$ has at least $2$ elements, then the principal filter of $A$ is not maximal

**Def**: Let $P$ be a nonempty family of subsets of $S$, then the *kernel of* $P$ is the intersection of all sets in $P$:
$$ \ker P := \bigcap P = \bigcap_{B \in P} B$$
a nonempty family of sets $P$ is called:
- *free* if $\ker P = \varnothing$, and *fixed* if $\ker P \ne \varnothing$
- *principal* if $\ker P \in P$
- *principal at a point* if $\ker P \in P$ and $\ker P$ is a singleton set, $\ker P =\{x\}$ then $P$ is said to be *principal at* $x$. 

We see that any principal filter is not free.

A filter is free iff  it contains the Fréchet filter

Let $S$ be infinite, and let $F = \{X\subseteq S\mid |S\setminus X| < \aleph_0\}$. $F$ is the filter of all *cofinite* subsets of $S$. This is special and called a *Fréchet filter*

The *trivial* ideal on $S$ is $\{\varnothing\}$. A *principal ideal* is an ideal of the form $$I = \{X \mid X \subseteq A\} = \mathcal P(A)$$ where $A\subseteq S$. 

To see how filters and ideals are related, note that if $F$ is a filter on $S$, then $$ I = \{S\setminus X \mid X \in F\}$$is an ideal, and vice versa, if $I$ is an ideal, then $$F = \{S\setminus X \mid X\in I\}$$is a filter. Two objects related by the equations above are called *dual* to each other. 

**Def:** Let $S$ be a nonempty set. An *ideal* of $S$ is a collection $I$ of subsets of $S$ that satisfies the following properties:
- $\varnothing \in I$, and $S\notin I$
- If $X, Y \in I$, then $X\cup Y \in S$
- if $Y \in I$, and $X \subseteq Y$, then $X\in S$

**Def:** Given a filter $F$ on the set $X$, a nonempty sub collection $B$ of $F$ is a *filter base* or *prefilter* for $F$ if it satisfies that for every $A \in F$, there's a $C \in B$, such that $C \subseteq A$.

## Filter Base or Prefilters

**Prop:** Let $X$ be a set and $B$ be a nonempty family of $X$. Then $B$ is filter base on $X$ iff $\varnothing \notin B$, for any $A_1, A_2\in B$, there exists a $A_3 \in B$ such that $A_3 \subseteq A_1 \cap A_2$. 

If $B$ is a nonempty family of subsets of $X$, such that satisfies the condition:
$$(\star) \varnothing \notin B \land \forall A_1, A_2 \in B \exists A_3\in B [A_3 \subseteq A_1\cap A_2] $$
then the filter that contains $B$ as a filter base is the collection $$F_B = \{F \subseteq X \mid \exists A \in B [A \subseteq F]\}$$ The filter $F_B$ is the *filter generated by the filter base* $B$. 

**Def:** Let $F_1$ and $F_2$ be prefilters on $X$, then we can add a preorder them: we say that $F_2$ *refines* $F_1$ and write $F_1 \le F_2$ if for the corresponding filters $\mathcal F_1 \subseteq \mathcal F_2$. It is not hard that this holds iff for every $A_1 \in F_1$ there exists $A_2\in F_2$  such that $A_2 \subseteq A_1$. If $F_1 \le F_2 \le F_1$ We say that $F_1$ and $F_2$ are *equivalent* prefilters and write $F_1 \sim F_2$.  

**Def**: A system of sets $S$ has the *finite intersection property* if every nonempty finite subsystem of $S$ has nonempty intersection. Sometimes systems with this property are called *centered*. 

Any filter and any filter base have the finite intersection property. 

If we have a nonempty system $S$ with the finite intersection property, then $\varnothing \notin \pi(S)$, the $\pi$-system generated by $S$, is a filter base, and we can generate a filter $F_{\pi(S)}$. 

**Lemma:** Let $G$ be a nonempty collection of subsets of $S$ and let $G$ have the finite intersection property. Then there's is a filter $F$ on $S$, such that $G\subseteq F$. The proof is the argument above, and it is the smallest filter that contains $G$. 

**Prop:** Let $I$ be a family of subsets of $X$, the following are equivalent:
- $I$ has the finite intersection property
- there exists a prefilter $F$, such that $I \subseteq F$
- there exists a filter $\mathcal F$ such that $I\subseteq \mathcal F$

This is why, in the context of filters, sets with the finite intersection property are called filter subbase.

**Def:** A family of prefilters $\{F_i\}_{i \in I}$ on a set $X$ is *compatible* if there exists a prefilter $F \supseteq \bigcup_{i \in I} F_i$, i.e., $\bigcup_{i \in I} F_i$ is a filter subbase. This occurs iff every finite subset $J\subseteq I$ and any assignment $j\mapsto A_j\in F_j$  we have that $\bigcap_{j\in J} A_j \ne \varnothing$. 

# Ultrafilters

**Def:** A filter $U$ on $S$ is an *ultrafilter* if for every $X\subseteq S$, either $X\in U$ or $S\setminus X \in U$. 

**Def:** An ideal $I$ on $S$ is a *prime ideal* if for every $X\subseteq S$, either $X\in I$ or $S\setminus X \in I$

**Lemma:** A filter $F$ on $S$ is an ultrafilter iff $F$ is a maximal filter.

**Th:** Let $X$ be a set.  The following are equivalent:
- $F$ is an ultrafilter on $X$
- $F$ is a maximal centered family
- $F$ is a filter base with the property: for all $A \subseteq X$, if $A\cap B\ne \varnothing$ for all $B\in F$, then $A \in F$
- $F$ is a maximal filter
- $F$ is a centered family with the property: for all $A\subseteq X$, either $A\in F$ or $X\setminus A \in F$

**Th:** Every filter $F$ on $S$, can be extended to an ultrafilter on $S$.

**Cor:** Every centered family on $S$ can be extended to an ultrafilter on $S$

**Lemma:** If $C$ is a subset of filters on $S$ and if every $F_1, F_2 \in C$ either $F_1 \subseteq F_2$ or $F_2 \subseteq F_1$, then the union of $C$ is also a filter on $S$

There is a natural relation between ultrafilters and [[Measure|measures]]. Let us call a content $m$ on $S$ *two-valued* if it only takes values $0$ or $1$; for every $A\subseteq S$, $m(A) \in \{0, 1\}$. 

**Th:** 
- If $m$ is a two-valued content on $S$ then $U = \{A \subseteq S\mid m(A) = 1\} = m^{-1}[\{1\}]$ is an ultrafilter
- If $U$ is an ultrafilter on $S$, then the function $m: \mathcal P(S) \to \{0, 1\} =2$ defined as $m(A) = 1$ if $A\in U$, and $m(A) = 0$ if $A \notin U$, is a two valued content on $S$. 

**Prop:** A nonprincipal ultrafilter is free. Meaning a ultrafilter is nonprincipal iff it is free. 

**Cor:** An ultrafilter is nonprincipal iff doesn't contain a finite subset of $X$. 

**Th:** Let $X$ be a set, if $X$ is finite there are $|X|$ ultrafilters, if $X$ is infinite, there are $2^{2^{|X|}}$ ultrafilters

**Cor:** if $X$ is infinite, there are $2^{2^{|X|}}$ nonprincipal ultrafilters

**Def**: A nonempty family $U$ of subsets of $X$ is called *ultra* if $\varnothing \notin U$ and for every $S\subseteq X$, there exists $B\in U$, such that $B\subseteq S$ or $B\subseteq X\setminus S$ (or equivalently such that $B\cap S = B$ or $B\cap S = \varnothing$)

**Prop:** A nonempty family $U$ of subsets of $X$ is called *ultra* if $\varnothing \notin U$ and any of the following equivalent are satisfied:
- For every set $S\subseteq X$ there exists $B\in U$ such that $B\cap S =B$ or $B\cap S = \varnothing$
- For every $S \subseteq \bigcup U$ there exists $B\in U$ such that $B\cap S = B$ or $B\cap S = \varnothing$ 
- For *every set* $S$, there exists $B\in U$ such that $B\cap S = B$ or $B\cap S = \varnothing$
The last two characterizations we see that don't depend on $X$, so we see that $U$ is ultra is independent of the set $X$

We see that a ultrafilter is a filter that is ultra. 

**Def:** An ultra prefilter is a filter base that is ultra. 

**Prop:** A *maximal prefilter on* $X$ is a prefilter $U$ on $X$ that satisfies any of the following equivalent conditions:
- $U$ is ultra
- $U$ is maximal with respect to the preorder of prefilters
- if a filter $F$ on $X$ satisfies that $U\le F$ then $F\le U$ (using the preorder on the prefilters)
- the filter generated by $U$ is ultra
