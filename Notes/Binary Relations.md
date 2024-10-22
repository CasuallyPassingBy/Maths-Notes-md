---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Cartesian Product]]

A set $R$ is a binary relation if for any $z \in R$, then there exists $x$ and $y$ such that $z = (x,y )$. It is usually said that $x$ _is in relation $R$ with $y$_ iff $xRy$, which is the same as $(x, y) \in R$.

The _domain of_ $R$ is the set of all $x$ such that there’s a $y$ that $x R y$, ${\text{dom}\,R=\{x\mid \exists y[xRy]\}}$

The _range of $R$_ is the set of all $y$ such that there’s an $x$ that $xRy$, ${\text{ran}\,R = \{y \mid \exists x [xRy]\}}$

The _field of $R$_ is just $\text{dom}\,R \cup \text{ran}\,R = \text{field}\,R$

If $\text{field}\,R \subseteq X$, then $R$ is a _relation in_ $X$, or that is a relation _between_ elements of $X$. $R$ is a relation in $X$ iff $R \subseteq X \times X$.

The _image of $A$ under $R$,_ is the set of all $y$ from the $\text{ran}R$ related to some element in $A$, denoted as $R[A]$,

$$ R[A]= \{y \in \text{ran}\,R \mid \exists x \in A[x R y]\} $$

The _inverse image of $B$ under $R$_ is the set of all $x\in \text{dom} R$, related to some element in $B$, denoted as $R^{-1}[B]$,

$$ R^{-1}[B] = \{x \in \text{dom}\,R \mid \exists y \in B[xRy]\} $$

Let $R$ be a binary relation, the _inverse of $R$_ is the set

$$ R^{-1} = \{(x,y) \mid \exists x, y [yR x]\} $$

The inverse image of $B$ under $R$ is equal to the image $B$ under $R^{-1}$.

Let $R$ and $S$ be binary relations. The _composition_ of $R$ and $S$ is the relation

$$ S \circ R = \{(x, z) \mid \exists y [xRy \land y S z] $$

- Some properties about the image and inverse image of $R$:
    - $A_1 \subseteq A_2 \implies R[A_1] \subseteq R[A_2]$
    - $R[A \cup B] = R[A] \cup R[B]$
    - $R[A\cap B] \subseteq R[A] \cap R[B]$
    - $R[A\setminus B] \supseteq R[A] \setminus R[B]$
    - $A_1 \subseteq A_2 \implies R^{-1}[A_1] \subseteq R^{-1}[A_2]$
    - $R^{-1}[A \cup B] = R^{-1}[A] \cup R^{-1}[B]$
    - $R^{-1}[A\cap B] \subseteq R^{-1}[A] \cap R^{-1}[B]$
    - $R^{-1}[A\setminus B] \supseteq R^{-1}[A] \setminus R^{-1}[B]$

- Some properties about binary relations on $A$ may have are, let $R$ be a binary relation on $A$:
    - $R$ is _reflexive_ if for any $a\in A$, then $aRa$.
    - $R$ is _irreflexive_ if for any $a\in A$, then $(a,a) \not\in R$
    - $R$ is _symmetric_ if for any $a, b\in A$, $aRb$ implies $b Ra$.
    - $R$ is _antisymmetric_ if for any $a, b\in A$, $aRb$ and $b Ra$ implies $a = b$.
    - $R$ is _asymmetric_ if for any $a, b\in A$, $aRb$ implies $(b,a)\not\in R$.
    - $R$ is _transitive_ if for any $a, b,c \in A$, $aRb$ and $bRc$ implies $aRc$.
    - $R$ is _connected_ if for any $a, b\in A$, and $a\ne b$, then $aRb$ or $b R a$.
    - $R$ is _strongly connected_ if for any $a, b\in A$, then $aRb$ or $b R a$.

[[Cofinal and Coinitial Subsets]]