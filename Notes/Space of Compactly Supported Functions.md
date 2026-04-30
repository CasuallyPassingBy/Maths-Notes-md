---
tags:
  - MeasureTheory
  - FunctionalAnalysis
---
Subjects: [[Measure Theory]], [[Functional Analysis]]
Links: [[Compactness]], [[Continuous Functions and Homeomorphims]], [[Local Compactness]], [[Hausdorff Spaces]], [[Space of Continuous Functions]], [[Measures on Hausdorff Spaces]]

**Def:** Let $f$ be a continuous real or complex valued function on a topological space $X$. The *support* of $f$, written $$\text{supp}(f) := \text{cl}_X(\{x\in X\mid f(x) \ne 0\}).$$In the case $X$ is a locally compact Hausdorff space, we will denote by $\mathcal C_c(X)$ or ${\scr K}(X)$ the set of those continuous function $f:X \to \Bbb R$ for which $\text{supp}(f)$ is compact. Likewise, we will denote $\mathcal C_c(X, \Bbb C)$ or ${\scr K}^\Bbb C(X)$ the set of those continuous functions $f:X \to \Bbb C$ for which $\text{supp}(f)$ is compact.

It is clear that $\mathcal C_c(X)$ and $\mathcal C_c(X, \Bbb C)$ are vector spaces over $\Bbb R$ and $\Bbb C$, respectively, and that each function in $\mathcal C_c(X)$ or in $\mathcal C_c(X, \Bbb C)$ is bounded. We see that $\mathcal C_c(X)$ and $\mathcal C_c(X, \Bbb C)$ are subspaces of $C_b(X)$ and $C_b(X, \Bbb C)$, respectively. 

**Prop:** Let $X$ be a locally compact Hausdorff space, let $K$ be a compact subset of $X$, and let $U$ be an open subset of $X$ such that $K \subseteq U$. Then there is a function $f$ that belongs to $\mathcal C_c(X)$, satisfies $\chi_K \le f\le \chi_U$, and is such that $\text{supp}(f)\subseteq U$. 

**Lemma:** Let $X$ be a locally compact Hausdorff space, let $K$ be a compact subset of $X$, and let $U_1$ and $U_2$ be open subsets of $X$ such that $K\subseteq U_1\cup U_2$. Then there are compact sets $K_1$ and $K_2$ such that $K = K_1 \cup K_2$, $K_1\subseteq U_1$, and $K_2\subseteq K_2$. 

**Prop:** Let $X$ be a locally compact Hausdorff space, let $f\in \mathcal C_c(X)$, and let $U_1, \dots, U_n$ be open subsets of $X$ such that $\text{supp}(f) \subseteq \bigcup_{i = 1}^nU_i$. Then there are functions $f_1,\dots, f_n$ such that $f = f_1+f_2+\dots + f_n$ and such that $\text{supp}(f_i)\subseteq U_i$ for each $1\le i \le n$. Furthermore, if the function $f$ is nonnegative, then the functions $f_1,\dots, f_n$ can be chosen so that all are nonnegative.

**Prop:** Let $X$ be a locally compact Hausdorff space, let $K_1, \dots, K_n$ be disjoint compact subsets of $X$, and let $\alpha_1,\dots, \alpha_n$ be real/complex numbers. Then there is a function $f$ that belongs to $\mathcal C_c(X)$ or $\mathcal C_c(X, \Bbb C)$ and satisfies
- $f(x) = \alpha_i$ if $x\in K_i$ for each $1\le i \le n$, and 
- $\|f\|_\infty = \max\{|a_i|\mid 1\le i \le n\}.$ 

**Prop:** Let $X$ be a locally compact Hausdorff space. Then $\mathcal C_c(X)$ and $\mathcal C_c(X, \Bbb C)$ are dense subspaces of $\mathcal C_0(X)$ and $\mathcal C_0(X, \Bbb C)$. 

**Prop:** Let $X$ be a locally compact Hausdorff space, let $\scr A$ be a $\sigma$-algebra on $X$ that includes $\mathcal B(X)$, and let $\mu$ be a regular measure on $(X, {\scr A})$. Suppose that $1\le p <\infty$. Then $\mathcal C_c(X)$ is  dense subspace of $\mathscr L^p(X, {\scr A}, \mu, \Bbb F)$ and so determines a dense subspace of $L^p(X, {\scr A}, \mu, \Bbb F)$. 

**Prop:** Let $X$ be a locally compact Hausdorff space, and let $\mu$ be a regular Borel measure on $X$. A point $x\in X$ belongs to $\text{supp}(\mu)$ iff every nonnegative function $f$ in $\mathcal C_c(X)$ that satisfies $f(x) > 0$ also satisfies $\int f\,d\mu > 0$. 

**Lusin's Theorem:** Let $X$ be a locally compact Hausdorff space, let $\scr A$ be a $\sigma$-algebra on $X$ that includes $\mathcal B(X)$, and let $\mu$ be a regular measure on $(X, {\scr A})$, and let $f:X \to \Bbb C$ be $\scr A$-measurable. If $A\in \scr A$ and satisfies $\mu(A) <\infty$ and if $\varepsilon>0$, then there is a compact subset $K$ of $A$ such that $\mu(A\setminus K) <\varepsilon$ and such that the restriction of $f$ to $K$ is continuous. Moreover, there is a function $g\in \mathcal C_c(X, \Bbb F)$ that agrees with $f$ at each point in $K;$ if $A\neq\varnothing$ and $f$ is bounded on $A$, then the function $g$ can be chosen so that $$ \sup\{|g(x)|\mid x\in X\} \le\sup \{|f(x)|\mid x\in A\}.$$

**Prop:** Let $X$ be a locally compact Hausdorff space, and let $f$ be a nonnegative lower semicontinuous function on $X$. Then  $$f(x) = \sup\{g(x) \mid g\in \mathcal C_c(X) \land 0\le g\le f\} $$ holds at each $x\in X$. 
# Riesz Representation Theorem

**Obs:** Let $X$ be a locally compact Hausdorff space. We want to study the relationship between regular measures on $X$ and linear functionals on $\mathcal C_c(X)$. The first thing to note is that each function in $\mathcal C_c(X)$ is integrable with respect to each measure on $X$. It follows that if $\mu$ is regular Borel measure on $X$, then $f\mapsto \int f\, d\mu$ defines a linear functional on $\mathcal C_c(X)$. 

**Def:** A linear functional $I$ on $\mathcal C_c(X)$ is *positive* if for each nonnegative $f\in\mathcal C_c(X)$ we have that $I(f) \ge 0$. Note that if $\mu$ is a regular Borel measure on $X$, then the functional $f\mapsto\int f\, d\mu$ is positive. We see that a positive linear functional $I$ on $\mathcal C_c(X)$ is order preserving, in the sense that if $f, g\in \mathcal C_c(X)$ and satisfy $I(f) \le I(g)$. 

**Lemma:** Let $X$ be a locally compact Hausdorff space, and let $\mu$ be a regular Borel measure on $X$. If $U$ is an open subset of $X$, then $$\begin{align*}
\mu(U) &= \sup\left\{ \left. \int f\, d\mu \; \right\vert\; f\in \mathcal C_c(X) \land 0 \le f\le \chi_U\right\} \\
 &= \sup\left\{ \left. \int f\, d\mu \; \right\vert\; f\in \mathcal C_c(X) \land f\prec U\right\}
\end{align*} $$
**Def:** Let $X$ be a locally compact Hausdorff space, and let $I$ be a linear functional on $\mathcal C_c(X).$ We can define $\mu^*$ on the open subsets of $X$ by $$\mu^*(U) := \sup\{I(f) \mid f\in \mathcal C_c(X) \land f \prec U\}, $$and then extend it to all subsets of $X$ by $$\mu^*(A) := \inf\{\mu^*(U) \mid U\in \tau \land A\subseteq U\}.$$
 **Lemma:** Let $X$ be a locally compact Hausdorff space, and let $I$ be a linear functional on $\mathcal C_c(X)$, and let $\mu^*$ be defined just  as above. Then $\mu^*$ is an [[Outer Measures|outer measure]] on $X$, and every Borel subset of $X$ is $\mu^*$-measurable. 

**Lemma:** Let $X$ be a locally compact Hausdorff space, and let $I$ be a linear functional on $\mathcal C_c(X)$, and let $\mu^*$ be defined just  as above. Suppose that $A$ is a subset of $X$ and that $f$ belongs to $\mathcal C_c(X)$. If $\chi_A \le f$, then $\mu^*(A) \le I(f)$, while $0 \le f\le \chi_A$ and if $A$ is compact, then $I(f) \le \mu^*(A)$. 

**Prop:** Let $X$ be a locally compact Hausdorff space, and let $I$ be a linear functional on $\mathcal C_c(X)$, and let $\mu^*$ be defined just  as above, let $\mu$ be the restriction of $\mu^*$ to $\mathcal B(X)$, and let $\mu_1$ be the restriction of $\mu^*$ to the $\sigma$-algebra ${\scr M}_{\mu^*}$ of $\mu^*$-measurable sets. Then $\mu$ and $\mu_1$ are regular measures, and $$\int f\, d\mu = \int f\, d\mu_1 = I(f) $$holds for each $f\in \mathcal C_c(X)$.

**Riesz Representation Theorem:** Let $X$ be a locally compact Hausdorff space, and let $I$ be a linear functional on $\mathcal C_c(X)$. Then there is a unique regular Borel measure such that $$I(f) = \int f\,d\mu $$holds for each $f\in \mathcal C_c(X)$. 

## The $\mu^*$-measurable Sets

For this section, let $X$ be a locally compact Hausdorff space, $I$ be a positive linear functional on $\mathcal C_c(X)$. We defined an outer measure $\mu^*$ by $$\mu^*(U) := \sup\{I(f) \mid f\in \mathcal C_c(X) \land f \prec U\}, $$whenever $U$ is an open subset of $X$ and if $A\subseteq X$ $$\mu^*(A) := \inf\{\mu^*(U) \mid U\in \tau \land A\subseteq U\}.$$Let ${\scr M}_{\mu^*}$ be the $\sigma$-algebra of $\mu^*$-measurable sets. We know that $\mathcal B(X) \subseteq {\scr M}_{\mu^*}$, and that the restrictions $\mu$ and $\mu_1$ of $\mu^*$ to $\mathcal B(X)$ and to ${\scr M}_{\mu^*}$ are regular measures.

**Prop:** Let $X$ be a locally compact Hausdorff space, and let $\mu^*$ and ${\scr M}_{\mu^*}$ be as above. If $B\subseteq X$, then the following statements are equivalent.
- $B \in {\scr M}_{\mu^*}$.
- If $U$ is an open subset of $X$ and $\mu^*(U)$ is finite, then $B\cap U \in {\scr M}_{\mu^*}$.
- If $K$ is a compact subset of $X$, the $B\cap K \in{\scr M}_{\mu^*}$.

**Lemma:** Let ${\scr A}$ be a $\sigma$-algebra on $X$ that includes $\mathcal B(X)$, and let $\mu$ be a regular measure on $(X, {\scr A})$. If $K$ is a compact subset of $X$ such that $\mu(K)>0$, then there is a compact subset $K_0$ of $K$ such that $\mu(K_0) = \mu(K)$ and such that each open subset $U$ of $X$ that meets $K_0$ satisfies $\mu(U\cap K_0) > 0$. 

**Prop:** There is a disjoint of family ${\scr C}_0$ of compact subsets of $X$ such that
- if $K\in {\scr C}_0$ then $\mu_1(K)>0$,
- if $U$ is an open, if $K \in {\scr C}_0$ and if $U\cap K \neq \varnothing$ then $\mu_1(U \cap K)