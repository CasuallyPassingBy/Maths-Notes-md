---
tags:
  - Topology
  - Analysis
---
Subjects: [[Topology]], [[Metric and Normed Spaces]]
Links: [[Metrizable Spaces]], [[Paracompacteness]], [[Special Types of Collections in Topology]], [[Topological Developability]], [[Point-Regular and Regular Bases]]

**Th:** Every open cover of a pseudometrizable space has an open refinement which is both locally finite and $\sigma$-discrete; in particular, every pseudometrizable space is paracompact.

**Prop:** Every pseudometrizable space has a $\sigma$-discrete base.

**Cor:** Every pseudometrizable space has a $\sigma$-locally finite base.

**Lemma:** Every regular space which has a $\sigma$-locally finite base is perfectly normal.

**Lemma:** Let $X$ be a $T_0$ space and $\{d_n \mid n < \omega\}$ a countable family of pseudometrics on the set which are all bounded by $1$ and satisfy the following two conditions:
- $d_n: X \times X \to \Bbb R$ is a continuous function for all $n < \omega$.
- For every $x\in X$ and every nonempty closed set $A\subseteq X$ such that $x\notin X$ there exists $n <\omega$ such that $d(x, A) := \inf\{d_n(x, a) \mid a \in A\} > 0$
Then the space $X$ is metrizable and the function $d$ defined by $$
d(x, y) := \sum_{n < \omega} \frac1{2^n} d_n(x, y)
$$is a metric space on the space $X$.

**Th:** The product space $(J(\kappa))^\omega$ of the hedgehog $J(\kappa)$ is universal for all $T_3$ spaces of weight $\kappa \ge \omega$ and with a $\sigma$-locally finite base.

**Nagata-Smirnov Metrization Theorem:** A topological space is metrizable iff it is $T_3$ and has a $\sigma$-locally finite base.

**Urysohn Metrization Theorem:** A second countable space is metrizable iff it is $T_3$.

**Bing Metrization Theorem:** A topological space is metrizable iff it is $T_3$ and has a $\sigma$-discrete base.

**Kowalsky's Metrization Theorem:** The product space $(J(\kappa))^\omega$ of the hedgehog $J(\kappa)$ is universal for all metrizable spaces of weight $\kappa \ge \omega$.

**Prop:** The following statements are equivalent for a topological space $X$.
- $X$ is metrizable.
- $X$ is $T_2$, paracompact and developable.

**Smirnov Metrization Theorem:** A topological space is metrizable iff it is $T_2$, paracompact and locally metrizable. (We cannot weaken paracompact to metacompact, nor weaken $T_2$ to $T_1$). 

**Th:** If $X$ is a metrizable space and $f: X \to Y$ is a perfect function, then $Y$ is metrizable.

**Vaĭnšteĭn's Lemma:** If $f:X \to Y$ is a closed, continuous surjective function, and $X$ is metrizable, then for every $y\in Y$ such that $\chi(y, Y) \le\omega$ the set $\text{Fr}(f^{-1}\{y\})$ is compact.

**Hanai-Morita-Stone Theorem:** The following statements are equivalent if $X$ is a metrizable space, and $f: X \to Y$ is a closed, continuous and surjective function. ^fdd00b
- $Y$ is metrizable.
- $Y$ is first-countable.
- For every $y\in Y$ the set $\text{Fr}f^{-1}\{y\}$ is compact. 

**Th:** If $f:X \to Y$ is a closed, open, continuous, surjective function, and $X$ is metrizable, then $Y$ is metrizable.

**Th:** If a topological space $X$ has a point finite closed cover consisting of metrizable spaces, then $X$ is itself metrizable.

**Th:** A compact $T_2$ space $X$ is metrizable iff it has a $G_\delta$ diagonal.

**Th:** A $T_3$ space $X$ is metrizable iff it is locally finite developable.
# Metrization Theorems for $T_0$ spaces

**Bing Metrization Criterion:** A topological space is metrizable iff it is $T_0$, collectionwise normal and developable.

**Moore Metrization Theorem:** A topological space is metrizable iff it is $T_0$ and strongly developable.

**Th:** The following statements are equivalent for a topological space $X$.
- $X$ is metrizable.
- $X$ is $T_0$ and for each $x\in X$ has a local base $\mathcal B(x) = \{B(x) \mid n <\omega\}$ such that for every $n <\omega$, there's an $m <\omega$ that satisfies the following condition: if $x, y\in X$ and $B_m(x) \cap B_m(y) \neq \varnothing$, then $B_m(y) \subseteq B_n(x)$.
- *(Frink Metrization Theorem)* $X$ is $T_0$ and for each $x\in X$ has a local base $\mathcal B(x) = \{B(x) \mid n <\omega\}$ such that for every  $x\in X$ and $n <\omega$, there's an $m <\omega$ that satisfies the following condition: if $y\in X$ and $B_m(x) \cap B_m(y) \neq \varnothing$, then $B_m(y) \subseteq B_n(x)$.

**Jones Metrization Theorem:** If $X$ is $T_0$, then $X$ is metrizable iff it is $\cal K$-developable.

**Alexandroff-Urysohn Metrization Theorem:** Then following theorems are equivalent for a topological space $X$:
- $X$ is metrizable.
- $X$ is $T_0$ and and has a development $\{\mathcal W_n \mid n <\omega\}$ such that for any $n <\omega$, and $W_1, W_2 \in \mathcal W_{n+1}$ with $W_1 \cap W_2 \neq \varnothing$, then there's $W\in \mathcal W_n$ such that $W_1 \cup W_2 \subseteq W$.

**Cor:** A topological space is metrizable iff it is $T_0$ and has a development $\{\mathcal W_n\mid n <\omega\}$ such that $\mathcal W_n$ is a star-refinement of $\mathcal W_m$ for $m \le n <\omega$.

**Def:** Let $X$ be a topological space. We say that $$\left(\{U_n(x) : n <\omega\ \wedge \ x\in X\},\{V_n(x) : n <\omega\ \wedge \ x\in X \}\right) \in P(\tau_X) \times P(\tau_X)$$is a *Nagata double sequence for $X$* it for any $x, y\in X$ and $n <\omega$ it satisfies the following properties:
- $x\in V_n(x)$
- $\{U_m(x) \mid m <\omega\}$ is a local base for $X$ at $x$.
- If $y\in X\setminus U_n(x)$, then $V_n(y)\cap V_n(x)= \varnothing$.
- If $y\in V_n(x)$, then $V_n(y) \subseteq U_n(x)$.

**Obs:** If $\left(\{U_n(x) : n <\omega\ \wedge \ x\in X\},\{V_n(x) : n <\omega\ \wedge \ x\in X \}\right)$ is a Nagata double sequence for the space $X$, then for each $x\in X$ we know that $\{V_n(x)\mid n <\omega\}$ is a local base for $X$ on $x$, because $V_n(x) \subseteq U_(x)$ for every $n <\omega$.

**Lemma:** If $X$ has a Nagata double sequence, then $X$ has a Nagata double sequence $\left(\{U_n(x) : n <\omega\ \wedge \ x\in X\},\{V_n(x) : n <\omega\ \wedge \ x\in X \}\right)$ with the property that for every $x\in X$ the collections $\{U_n(x)\mid n <\omega\}$ and $\{V_n(x)\mid n <\omega\}$ are decreasing.

**Nagata's Double Sequence Metrization Theorem:** The following statements are equivalent for a topological space $X$.
- $X$ is metrizable.
- $X$ is $T_0$ and has a Nagata double sequence.

**Morita Metrization Theorem:** The following statements are equivalent for a topological space $X$.
- $X$ is metrizable.
- $X$ is $T_0$ and there's a sequence $\{\mathcal F_n\mid n <\omega\}$ formed by closed closure preserving covers of $X$ such that for every $x\in X$ and $U \in \tau_X$ with $x\in U$, there's an $n<\omega$ such that $\text{st}(x, \mathcal F_n) \subseteq U$.
- $X$ is $T_0$ and there's a sequence $\{\mathcal U_n \mid n<\omega\}$ of open covers of $X$ such that $\{\text{st}^2(x, \mathcal U_n) \mid n <\omega\}$ is a local base for $X$ at $x$. 

**Chittenden's Metrization Theorem:** The following statements are equivalent for a $T_0$ space $X$.
- $X$ is metrizable
- There's a function $\varphi: X\times X \to \Bbb R$ such that:
	- $\varphi(x, y) = \varphi(y, x) \ge 0$, for any $x, y\in X$
	- For every $\varepsilon >0$, if $\varphi(x, y) < \varepsilon$ and $\varphi(y, z)< \varepsilon$, then $\varphi(x,z) < 2\varepsilon$, for any $x, y, z\in X$.
	- The collection $\{B(x, 2^{-n})\mid n <\omega\}$ is a local base for $X$ at $x$, where $B(x, \varepsilon) := \{y \in X \mid \varphi(x, y) < \varepsilon\}$ for any $x\in X$ and $\varepsilon > 0$.


**Th:** The following statements are equivalent for a $T_0$ space $X$.
- $X$ is metrizable.
- *(Bing Metrization Criterion)* $X$ is collectionwise normal and developable.
- *(Moore Metrization Theorem)* $X$ is strongly developable.
- For each $x\in X$ has a local base $\mathcal B(x) = \{B(x) \mid n <\omega\}$ such that for every $n <\omega$, there's an $m <\omega$ that satisfies the following condition: if $x, y\in X$ and $B_m(x) \cap B_m(y) \neq \varnothing$, then $B_m(y) \subseteq B_n(x)$.
- *(Frink Metrization Theorem)* For each $x\in X$ has a local base $\mathcal B(x) = \{B(x) \mid n <\omega\}$ such that for every  $x\in X$ and $n <\omega$, there's an $m <\omega$ that satisfies the following condition: if $y\in X$ and $B_m(x) \cap B_m(y) \neq \varnothing$, then $B_m(y) \subseteq B_n(x)$.
- *(Jones Metrization Theorem)* $X$ is $\mathcal K$-developable.
- *(Alexandroff-Urysohn Metrization Theorem)* $X$ has a development $\{\mathcal W_n \mid n <\omega\}$ such that for any $n <\omega$, and $W_1, W_2 \in \mathcal W_{n+1}$ with $W_1 \cap W_2 \neq \varnothing$, then there's $W\in \mathcal W_n$ such that $W_1 \cup W_2 \subseteq W$.
- $X$ has a development $\{\mathcal W_n\mid n <\omega\}$ such that $\mathcal W_n$ is a star-refinement of $\mathcal W_m$ for $m \le n <\omega$.
- *(Nagata Double Sequence Metrization Theorem)* $X$ has a Nagata double sequence.
- *(Morita Metrization Theorem)* There's a sequence $\{\mathcal F_n\mid n <\omega\}$ formed by closed closure preserving covers of $X$ such that for every $x\in X$ and $U \in \tau_X$ with $x\in U$, there's an $n<\omega$ such that $\text{st}(x, \mathcal F_n) \subseteq U$.
- *(Morita Metrization Criterion)* There's a sequence $\{\mathcal U_n \mid n<\omega\}$ of open covers of $X$ such that $\{\text{st}^2(x, \mathcal U_n) \mid n <\omega\}$ is a local base for $X$ at $x$.
- *(Chittenden Metrization Theorem)* There's a function $\varphi: X\times X \to \Bbb R$ such that:
	- $\varphi(x, y) = \varphi(y, x) \ge 0$, for any $x, y\in X$
	- For every $\varepsilon >0$, if $\varphi(x, y) < \varepsilon$ and $\varphi(y, z)< \varepsilon$, then $\varphi(x,z) < 2\varepsilon$, for any $x, y, z\in X$.
	- The collection $\{B(x, 2^{-n})\mid n <\omega\}$ is a local base for $X$ at $x$, where $B(x, \varepsilon) := \{y \in X \mid \varphi(x, y) < \varepsilon\}$ for any $x\in X$ and $\varepsilon > 0$.

# Point-Regular and Regular Bases

**Arhangel'skiĭ Metrization Theorem:** A space $X$ is metrizable iff $X$ is $T_1$ and has a regular base.

**Alexandroff Metrization Theorem:** A topological space is metrizable iff it is $T_1$, collectionwise normal and developable.

**Arhangel'skiĭ Metrization Criterion:** The following statements are equivalent for a $T_1$ space $X$.
- $X$ is metrizable.
- $X$ has a base $\cal B$ such that for every compact subset $K \subseteq X$ and every $U \in \tau_X$ with $K \subseteq U$, then $|\{B \in \mathcal B \mid B \cap K \neq \varnothing \ \land \ B\cap (X \setminus U) \neq \varnothing\}| <\omega$.