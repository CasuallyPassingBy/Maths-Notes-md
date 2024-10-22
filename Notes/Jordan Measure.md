---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Riemann Integral in Rn]]

**Def:** Let $A\subseteq\Bbb R^n$ and define $\chi_A:\Bbb R^n\to \Bbb R$, the function characteristic of $A$, as follows

$$ \chi_A(x) \begin{dcases} 1 & x \in A \\ 0 & x \not\in A \end{dcases} $$

**Def:** Let $A \subseteq \Bbb R^n$ bounded, we say that $A$ is **Jordan-measurable** if the characteristic function of $A$ is integrable over some rectangle $R$, that contains $A$. In this case we say that the **Jordan measure of $A$** is (denoted by $J(A)$)

$$ J(A) := \int _R \chi_A $$

**Def:** In the context of Jordan measure we can define the Jordan outer-measure as

$$ \overline J(A) = \overline {\int_R}\chi_A $$

Similarly we can define the Jordan inner measure as

$$ \underline J(A) = \underline {\int_R} \chi_A $$

**Th:** Let $A \subseteq R' \subseteq R$, where $R$ and $R'$ be rectangles, if $\chi_A$ is integrable over $R$, then $\chi_A$ is integrable over $R'$ and $\int_R \chi_A = \int _{R'} \chi_A$. If $A\subseteq R', R$ and $\chi_A$ be integrable over $R$ and $R'$, then $\int_R \chi_A = \int _{R'} \chi_A$.

This ensures that the Jordan measure of $A$ is well defined.

********Th:******** Let $A\subseteq \Bbb R^n$ be bounded. Then all of the following are equivalent
- $A$ is Jordan measurable
- for any $\varepsilon >0$, there’s $R_1,\dots, R_k$ rectangles such that
    - $\partial A \subseteq \bigcup_{i = 1}^k R_i$
    - $\sum_{i = 1}^k m(R_i) < \varepsilon$
- $\partial A$ is Jordan measurable and $J(\partial A) =0$

Cor: Let $A \subseteq \Bbb R^n$ be a bounded set. $A$ is Jordan-measurable and $J(A) = 0$ iff for any $\varepsilon>0$ there’s $R_1,\dots, R_k$ rectangles such that
- $A \subseteq \bigcup_{i = 1}^k R_i$
- $\sum_{i = 1}^k m(R_i) < \varepsilon$

**************Lemma:************** Some basic properties are if $A\subseteq\Bbb R^n$ be bounded and Jordan-measurable:
- If $B\subseteq \Bbb R^n$ is Jordan measurable with $J(A) = J(B) =0$, then $A \cup B$ is Jordan-measurable and $J(A\cup B) =0$.
- If $B \subseteq A$, and $J(A) =0$, then $B$ is Jordan-measurable and $J(B) =0$.
- This pair of results help us show that the set of Jordan-measurable sets is an algebra, although not a $\sigma$-algebra
    If $A, B\subseteq \Bbb R^n$ are Jordan-measurable then the following sets are Jordan measurable:
    - $A \cup B$
    - $A\cap B$
    - $A\setminus B$
    And we have the following additional properties:
    - $J(A\cup B) + J(A\cap B) = J(A)+J(B)$
    - $J(A\setminus B) = J(A) -J(A\cap B)$
    - If $B\subseteq A$, then $J(B) \le J(A)$
    If $A \subseteq B \subseteq C \subseteq \Bbb R^n$ such that $A, C$ are Jordan-measurable with $J(A)=J(C)$, then $B$ is Jordan-measurable and $J(A) =J(B) =J(C)$.
    
- Some topological properties
    If $A$ is Jordan-measurable then
    - $J(A) > 0$ iff $\operatorname{int}(A) \ne \varnothing$
    - $J(A) = 0$ iff $A \subseteq \partial A$
    - $\operatorname{int}(A)$ and $\operatorname{cl}(A)$ are Jordan-measurable and $J(\operatorname{int}(A)) = J(A) = J(\operatorname{cl}(A))$
    - For any $\varepsilon>0$, there’s a compact set $K\subseteq \operatorname{int}({A})$ such that $K$ is Jordan-measurable and $J(A) - J(K) < \varepsilon$

********Lemma:********* Let $A$ be a Jordan-measurable. If $f:A\subseteq\Bbb R^n\to \Bbb R$ is continuous, then the set ${G_f=\{(x, f(x)) \in \Bbb R^{n+1} \mid x \in A\}}$, is Jordan-measurable and $J(G_f) =0$

********Th:******** Let $A$ be a Jordan-measurable. If $f,g:A\subseteq\Bbb R^n\to \Bbb R$ be continuous, such that for any $x \in A$, $f(x) \le g(x)$, then the set ${D = \{(x,y)\in\Bbb R^{n+1}\mid x \in A \land f(x) \le y\le g(x)\}}$ is Jordan-measurable.

********Th:******** Let $f:R\subset \Bbb R^n\to \Bbb R$ bounded over the rectangle $R$. If the set of $f$ discontinuities over $R$, $D(f,R)$ is Jordan-measurable. Then $J(D(f, R)) =0$, iff $f$ is integrable over $R$.
