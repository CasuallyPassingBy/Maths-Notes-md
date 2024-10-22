---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Jordan Measure]], [[Riemann Integral in Rn]], [[Lebesgue Criterion]]

**********Def:********** Let $f:A\subseteq\Bbb R^n \to \Bbb R$ be bounded over $A$. We define $f_A: \Bbb R^n\to \Bbb R$ as

$$ f_A(x) =\begin{dcases} f(x) & x\in A \\ 0 & x\not \in A \end{dcases} $$

We say that $f$ is integrable over $A$ if the function $f_A$ is integrable over a rectangle $R$ that contains $A$. In this case the integral of $f$ over $A$ is given by:

$$ \int_A f = \int_R f_A $$

Similarly, we prove that no matter the rectangle $R$ that contains $A$, we will obtain the same quantity ensuring the integral of $f$ over $A$ is well-defined.

**************Lemma:************** Let $f:A\subseteq \Bbb R^n\to \Bbb R$ be bounded over $A$ and $R$ a rectangle such that $A \subseteq R$. Then $D(f_A, R) \subseteq \partial A \cup D(f, A)$

**************Th:************** Let $f:A\subseteq \Bbb R^n\to \Bbb R$ be bounded over $A$, a Jordan-measurable set. If the set of discontinuities of $f$ over $A$, $D(f, A)$, is Jordan-measurable. Then $J(D(f, A))=0$, then $f$ is integrable over $A$.

**************Cor:************** Let $f:A\subseteq \Bbb R^n\to \Bbb R$ be bounded over $A$, a Jordan-measurable set. If $f$ is continuous over $A$, then $f$ is integrable over $A$.

- Algebraic Properties of the Integral over Jordan-measurable sets
    
    **Th:*** Let $f, g :A\subseteq \Bbb R^n\to \Bbb R$, then
    - $f+g$ is integrable over $A$ and
        $$ \int_A f+g = \int_A f+\int_A g $$
    - If $c \in \Bbb R$, then $cf$ is integrable over $A$ and
        $$ \int_A f = c\int_A f $$
    - $f^2$ is integrable over $A$
    - $fg$ is integrable over $A$
    - $|f|$ is integrable over $A$ and
        $$ \left|\int_A f\right|\le \int_A |f| $$
    - $f \ge 0$ then
        $$ \int_A f \ge 0 $$
    - $f\ge g$ then
        $$ \int_A f \ge \int_A g $$
    - the functions $\max\{f,g\}$ and $\min\{f,g\}$ are integrable over $A$
### Mean Value Theorem for Integrals
Let $f,g:A\subseteq\Bbb R^n\to \Bbb R$ such that $f$ is continuous over $A$ and $g$ is integrable over $A$, with $A$ being a connected set. Then
- $\int_A f = f(x_0) \cdot J(A)$ for some $x_0 \in A$
- if $g\ge 0$ then $\int_A fg = f(x_0) \int_A g$ for some $x_0 \in A$

********Th:******** If $f:A\cup B \subseteq\Bbb R^n\to \Bbb R$ be integrable over $A$ and $B$, then $f$ is integrable over $A\cup B$ and $A\cap B$, furthermore
$$ \int_{A\cup B} f = \int_A f+ \int_B f-\int_{A\cap B}f $$
