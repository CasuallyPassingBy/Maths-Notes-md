---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Open and Closed Sets in R]]

## Perfect Sets

**Def:** A set $P\subseteq \Bbb{R}$ is **perfect** if is closed and contains no isolated points. Also $P' = P$ and $P\ne \varnothing$ is the same as to be perfect. 

Let $\mathcal P$ be the system of all perfect subsets of $\Bbb R$.

**Lemma:** There are functions $G_0$ and $G_1$ from $\mathcal P$ into $\mathcal P$ such that for each $F \in \mathcal P$, $G_0(F), G_1(F) \subseteq F$ and $G_0(F) \cap G_1(F) = \varnothing$. 

For any bounded set $A \subseteq \Bbb R$, we define the *diameter* of $A$, $\text{diam}(A)$ as $\sup A - \inf A$ 

**Lemma:** There is a function $H: \mathcal P \times N^+ \to \mathcal P$ such that for each $F \in \mathcal P$, and $n \in \Bbb N^+$, $H(F, n) \subseteq F$, and $\text{diam}(H(F, n)) \le 1/n$

**Th:** A nonempty perfect set has a cardinality of $2^{\aleph_0}$. This can be done with these lemma's or directly with an argument of looking for convergent subsequences.

**Th:** Every uncountable closed set contains a perfect subset. The proof of this statement: can be of 2 ways, using the axiom of choice to know that the countable union of countable sets is countable; or using transfinite recursion.

To prove it without using the axiom of choice, we need to study closed sets

**Th:** Every closed set has at most countably many isolated points

Let $F\ne \varnothing$ be a closed set. If $F = F'$, $F$ is perfect and $|F| = 2^{\aleph_0}$. Otherwise, $F= (F \setminus F') \sqcup F'$, and $|F\setminus F'| \le \aleph_0$, so it remains to determine the cardinality of the smaller closed set $F'$. If $F' = \varnothing$ then $F = F - F'$ has only isolated points and $|F| \le \aleph_0$. 

If $F'$ is perfect, the $|F'| = 2^{\aleph_0}$, so $|F| = 2^{\aleph_0}$. It is possible that $F'$ again has isolated points. in this case we can repeat the procedure and examine $F'' = (F')'$. If $F'' = \varnothing$ or $F''$ is perfect, we get that $|F| \le \aleph_0$ or $|F| = 2^{\aleph_0}$. But $F''$ may have isolated points, and the analysis must continue. We can define an infinite sequence $\langle F_n \mid n \in \Bbb N\rangle$ by recursion:
$$\begin{align*}F_0 &= F \\ F_{n+1} &= (F_n)' \end{align*}$$All $F_n$ are closed sets; if for some $n \in \Bbb N$ $F_n = \varnothing$ of $F_n$ is perfect, we get $|F| \le {\aleph_0}$ or $|F| = 2^{\aleph_0}$. Unfortunately, it may happen that for all $F_n$'s have isolated points. We could define $$F_\omega = \bigcap\limits_{n \in \Bbb N} F_n$$If $F_\omega$ is perfect, we get that $|F| \ge |F_\omega|  = 2^{\aleph_0}$, and if $F_\omega = \varnothing$, $$F = \bigcup_{n \in \Bbb N} (F_n\setminus F_{n+1})$$is a countable union of countable sets, which can be proved to be countable WITHOUT the use of the axiom of choice. 

The problem is that $F_\omega$ can have isolated points. So we have to consider $F_{\omega +1} = F_\omega'$, and so on, if necessary, even  $$ F_{\omega+ \omega} = \bigcap_{n \in \Bbb N} F_{\omega + n}$$and so on. As the sets get smaller, there is good hope that the process will eventually stop, by reaching either a perfect set of $\varnothing$. This is the original motivation that led Georg Cantor to the development of this theory of transfinite or [[ordinal numbers]]

**Def:** Let $A \subseteq \Bbb R$. For every ordinal $\alpha$ we define by recursion$$\begin{align*}
	A^{(0)} &= A \\
	A^{(\alpha +1)} &= (A^{(\alpha)})' \\
	A^{(\alpha)} &= \bigcap_{\gamma < \alpha} A^{(\gamma)} \quad (\alpha\text{ a limit ordinal})
\end{align*}$$
**Th:** Let $F$ be a closed set of reals. There exists an at most countable ordinal $\Theta$ such that:
- $\Theta < \omega_1$
- for every $\alpha < \Theta$, the set $F^{(\alpha)} \setminus F^{(\alpha +1)}$ is nonempty and at most countable
- $F^{(\Theta +1)} = F^{(\Theta)}$ 
- $P = F^{(\Theta)}$ is either perfect or empty
- $C = F\setminus P$ is at most countable

**Cor:** Every uncountable closed set has a perfect subset. 

**Th:** There's an uncountable set without a perfect subset

**Cor:** Every closed set of reals is either at most countable or has cardinality $2^{\aleph_0}$.

## Connected Sets

**Def:** Two nonempty sets $A, B \subseteq \Bbb{R}$ are separated if $\operatorname{cl}(A) \cap B = A \cap \operatorname{cl}(B) = \varnothing$. A set $E \subseteq \Bbb{R}$ is **disconnected** if it can be written as $E= A\cup B$, where $A$ and $B$ are separated sets. A set that isn’t disconnected is **connected.**

**Th:** Let $A \subseteq \Bbb{R}$. $A$ is connected iff there’s no $U,V \subseteq \Bbb{R}$ open sets such that:

- $A \subseteq U \cup V$
- $A\cap U \ne \varnothing$ and $A\cap V \ne \varnothing$
- $A\cap U\cap V = \varnothing$

**Def:** A set $E$ is _********************totally disconnected********************_ if, given two distinct points $x, y \in E$, there exists $x \in A$ and $y \in B$ such that are separated sets and $E = A\cup B$

**Th:** A set $E \subseteq \Bbb{R}$ is connected iff, for all disjoint sets $A$ and $B$ satisfying $E = A \cup B$, there always exists a convergent sequence $x_n \to x$ with $(x_n)$ contained in one of $A$ or $B$, and $x$ an element of the other.

**Th:** A set $E\subseteq \Bbb{R}$ is connected iff whenever $a <c<b$ with $a, b \in E$, it follows that $c \in E$