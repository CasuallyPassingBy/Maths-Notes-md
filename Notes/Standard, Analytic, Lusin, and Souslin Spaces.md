---
tags:
  - MeasureTheory
  - Topology
  - SetTheory
  - Analysis
---
Subjects: [[Measure Theory]], [[Metric and Normed Spaces]], [[Topology]], [[Set Theory]]
Links: [[Polish Spaces]], [[Rings and Algebras of Sets]], [[Measurable Functions]], [[Hausdorff Spaces]]

**Def:** A measurable space $(X, {\scr A})$ is *standard* if there is a Polish space $Z$ such that $(X, {\scr A})$ is isomorphic to $(Z, \mathcal B(Z))$, and is *analytic* if there is a Polish space $Z$ and an analytic subset $A$ of $Z$ such that $(X,{\scr A})$ is isomorphic to $(A, \mathcal B(A))$. 

**Obs:** We see that if $(X, {\scr A})$ is a standard space, then either $X$ is countable and $\scr A$ is the power set of $X$ or else $(X, {\scr A})$ is isomorphic to $(\Bbb R, \mathcal B(\Bbb R))$. 

**Def:** Let $(X, {\scr A})$ be a measurable space. A subfamily $\scr C$ of $\scr A$ *generates* $\scr A$ if $\sigma({\scr C}) = \scr A$. The $\sigma$-algebra $\scr A$, or the measurable space, is *countably generated* if $\scr A$ has a countable subfamily that generates it. A family $\scr C$ of subsets of $X$ *separates the points* of $X$ if for each pair $x, y$ of distinct points in $X$ there is a member $\scr C$ that contains exactly one of $x$ and $y$. The space $(X, {\scr A})$, or the $\sigma$-algebra $\scr A$, is *separated* if $\scr A$ separates the points of $X$, and is *countably separated* if $\scr A$ has a countable subfamily that separates the points of $X$. 

**Prop:** Let $(X, {\scr A})$ be a measurable space. If $\scr A$ is separated and countably generated, then $\scr A$ is countably generated.

**Lemma:** Let $(X, {\scr  A})$ be an analytic measurable space, let $Y$ be a Polish space, and let $f:X\to Y$ be measurable with respect to $\scr A$ and $\mathcal B(Y)$. Then the images of $f$ of the sets in $\scr A$ are analytic. 

**Prop:** Each bijective measurable map between analytic measurable spaces is an isomorphism.

**Lemma:** Let $(X, {\scr A})$ be a countably generated measurable space, and suppose that the collection $\{A_n\mid n<\omega\}$ generate $\scr A$. Define $F:X \to 2^\omega$ by letting $F$ take $x$ to the sequence $(\chi_{A_n}(x))_{n<\omega}$. Then ${\scr A} = F^{-1}[\mathcal B(2^\omega)].$

**Cor:** Let $(X, {\scr A})$ be a separated and countably generated measurable space. Then there is a subset $A$ of $2^\omega$ such that $(X, {\scr A})$ is isomorphic to $(A,\mathcal B(A))$. 

**Prop:** Let $(X, {\scr A})$ be an analytic measurable space, let $(Y, \mathscr B)$ be a separated and countably generated measurable space, and let $f: X\to Y$ be surjective and measurable. Then $(Y, \mathscr B)$ is analytic. 

**Prop:** Let $(X, {\scr A})$ be a standard measurable space, let $(Y, {\scr B})$ be a separated and countably measurable space, and let $f: X\to Y$ be a bijective and measurable. Then $(Y, {\scr B})$ is standard.

**Def:** Let $(X, {\scr A})$ be a measurable space, and let $x\in X$. The *atom* of $\scr A$ determined by $x$ is the intersection of those sets that belong to $\scr A$ and contain $x$. 

**Obs:** It is easy to check that atoms of $\scr A$ form a partition of $X$, and that an atom of $\scr A$ doesn't necessarily belong to $\scr A$.

**Prop:** Let $(X, {\scr A})$ be a measurable space. Then each atom of $\scr A$ contains only one point iff $\scr A$ separates points of $X$. 

**Th (Blackwell):** Let $(X, {\scr A})$ be an analytic measurable space, and let ${\scr A}_0$ be a countably generated sub-$\sigma$-algebra of $\scr A$. Then a subset of $X$ belongs to ${\scr A}_0$ iff it belongs to $\scr A$ and is the union of a family of atoms of ${\scr A}_0$.

**Cor:** Let $(X, {\scr A})$ be an analytic measurable space, and let ${\scr A}_0$ be a separated and countably generated sub-$\sigma$-algebra of $\scr A$. Then ${\scr A} = {\scr A}_0$. 

**Cor:** Let $(X, {\scr A})$ be an analytic measurable space, let $(Y, {\scr B})$ be a countably separated measure space, and let $f:X\to Y$ be a surjective and measurable. Then $(Y, {\scr B})$ is analytic. 

**Cor:** Let $(X, {\scr A})$ be a standard measurable space, let $(Y, {\scr B})$ be a countably separated measurable space, and let $f:X\to Y$ be bijective and measurable. Then $(Y, {\scr B})$ is standard. 

**Def:** A *Lusin space* is a Hausdorff space that is the image of a Polish space under a continuous bijection, and a *Souslin space* is a Hausdorff space that is the image of a Polish space under a continuous surjection. 

**Obs:** Every Lusin space is a Souslin space.

**Obs:** Every Souslin space is separable.

**Examples:**
- We see that the Souslin subspaces of Polish space $X$ are exactly the analytic subsets of $X$. The Lusin subspaces of a Polish space are exactly the Borel subsets of $X$. 
- Suppose that $X$ is a Polish space, and let $X_0$ be a constructed by replacing the topology of $X$ with a weaker Hausdorff topology. The function $f:X\to X_0$ defined by $f(x) = x$ is continuous, and so $X_0$ is a Lusin space. In particular, if $X$ is a separable Banach space, then $X$ with its weak topology is a Lusin space. Likewise, if the dual $X^*$ of the Banach space $X$ is separable, then $X^*$ with its weak$^*$ topology is a Lusin space. Furthermore, if the Banach space $X$ is infinite dimensional, then the weak topology on $X$ and weak$^*$ topology on $X^*$ are not metrizable. Thus non-metrizable Lusin spaces arise in a natural way.

**Lemma:** If $X$ is a Souslin space, then $\mathcal B(X)$ is countably separated.

**Prop:** If $X$ is a Souslin space, then $(X, \mathcal B(X))$ is an analytic measurable space, while $X$ is a Lusin space, then $(X, {\cal B}(X))$ is a standard measurable space.

**Th:** Every finite Borel measure on a Souslin space is regular. 

**Prop:** Let $X$ be a Souslin space. If $\scr U$ is a collection of open subsets of $X$, then there is a countable subcollection ${\scr U_0}$ of $\scr U$ such that $\bigcup {\scr U} = \bigcup {\scr U}_0$. 

**Prop:** If $X$ and $Y$ are Souslin spaces, then $\mathcal B(X\times Y) = \mathcal B(X) \otimes \mathcal B(Y)$.

**Prop:** Every locally compact Souslin space is metrizable. 