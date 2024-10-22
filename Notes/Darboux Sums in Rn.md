---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Riemann and Darboux Sums in R]]

**Def:** Let $R$ _be a rectangle_ in $\Bbb R^n$ if it is of the form

$$ R = \prod_{i = 1}^n [a_i, b_i] $$

where each $[a_i, b_i]$ is a closed interval of real numbers. The number

$$ d(R) = \left(\sum_{i = 1}^n(b_i-a_i)^2\right)^{1/2} $$

will be called the *diagonal* of $R$, and the number

$$ m(R) = \prod_{i = 1}^n (b_i -a_i) $$

will be called the measure of $R$. In the case that $m(R)>0$, then $R$ is called **non-degenerate.**

**********Def:********** Let $R = \prod_{i = 1}^n[a_i, b_i]$. If $\mathcal P_i$ is a partition of the interval $[a_i, b_i]$, for each $1 \le i \le n$, we say that

$$ \cal P = \prod_{i = 1}^n P_i $$

is a partition of $R$. Note that $\mathcal P$ is a finite subset of $R$, that consists of the vertices of each of the subrectangles of $R$ induced by $\cal P$. The partition $\cal P_i$ is called the $i$th coordinate partition of $\cal P$. We will denote $\mathbf P_R$ as the set of all partitions of the rectangle $R$.

**************Lemma:************** Let $R\subseteq \Bbb R^n$ be a rectangle for any $\varepsilon >0$ there’s a $R \subseteq R'$ with rational dimensions such that ${m(R') - m(R) < \varepsilon}$

**Def:** Let $\cal P$ and $\cal Q$ be two partitions of $R$, with $\cal P = \prod _{i = 1}^n P_i$ and $\cal Q = \prod _{i = 1}^n Q_i$. We say that $\cal Q$ **_refines $\cal P$_ if for all $1 \le i \le n$, $\cal P_i \subseteq Q_i$. This is equivalent to $\cal P \subseteq Q$.

**Def:** Given two partitions of $R$, $\cal P$ and $\cal Q$ there’s not necessarily a relationship of refinement between each other, but there exists a third partition that refines both $\cal P$ and $\cal Q$ denoted as

$$ \cal P \uplus Q := \prod_{i = 1}^n (P_i \cup Q_i) $$

**Def:** Let $f$ be a real-valued function defined and bounded on the rectangle $R \subseteq \Bbb R^n$ and $\cal P$ be a partition of $\cal P$. If $R_1, \dots, R_k$ are the corresponding subrectangles of $R$ induced by $\cal P$, we can define _the lower sum of $f$over the partition $\cal P$,_ denoted as $L(f, \cal P)$ or $\underline S (f, \cal P)$

$$ L(f, \mathcal P ) = \sum_{i = 1}^k m_i \cdot m(R_i) \quad \text{ where } \quad m_i = \inf_{x \in R_i}f(x) \quad \text{for } 1 \le i \le k $$

Similarly, we can define the ************_upper sum of $f$ over the partition $\cal P$_, denoted as $U(f, \cal P)$ or $\overline S(f , P)$

$$ U(f, \mathcal P) = \sum_{i = 1}^k M_i\cdot m(R_i) \quad \text{ where } \quad M_i = \sup_{x \in R_i}f(x) \quad \text{for } 1 \le i \le k $$

**Prop:** Let $\cal P$ be any partition of $R$, then $L(f, \mathcal P) \le U(f, \cal P)$ .

**Prop:** Let $\mathcal {P, Q} \in \mathbf P_R$. If $\cal Q$ refines $\cal P$ then $L(f, \mathcal P) \le L(f, \cal Q)$ and $U(f, \mathcal Q) \le U(f, \cal P)$

**Prop:** Let $\cal P$ and $\cal Q$ be partitions of $R$, then $L(f, \mathcal P) \le U (f, \cal Q)$

**Def:** Since the following sets are bounded $\{L(f, \mathcal P) \mid \mathcal P \in \mathbf P_R\}$ and $\{U(f, \mathcal P) \mid \mathcal P \in \mathbf P_R\}$, then we can consider their supremum and infimum respectively. Then

$$ \underline{\int_R} f := \sup_{\mathcal P \in \mathbf P_R} L(f, \cal P) $$

and

$$ \overline{\int_R} f := \inf_{\mathcal P \in \mathbf P_R} L(f, \cal P) $$

are called the **************_lower integral $f$ over $R$_ and ********_the upper integral of $f$ over $R$._ In general it is true that

$$ \underline{\int _R} f \le \overline{\int _R} f $$