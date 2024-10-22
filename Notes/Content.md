---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measure]], [[Ring of sets]]

A content $\mu$ is a is a real-valued function defined on a collection $\mathcal A$ such that:
- $\mu(A) \in [0, \infty]$
- $\mu(\varnothing) = 0$
- Let $A_1, \dots A_n \in \mathcal A$, $\bigcup_{i = 1}^n A_i \in \mathcal A$, and $A_i \cap A_j = \varnothing$ when $i\ne j$ $$\mu\left(\bigcup_{i = 1}^n A_i\right) = \sum_{i = 1}^n A_i$$
We see that contents are finitely additive. Sometimes it is called a finitely additive measure, in contrast that measures are $\sigma$-additive. 

We choose $\mathcal A$ we want it to be a ring of sets, or maybe a semiring of sets

# Properties 

### On semirings

If $\mathcal A$ is a semiring  of sets then the following statements can be deduced:
- Every content $\mu$ is monotone that is; $A\subseteq B$, then $\mu(A) \le \mu(B)$ for $A, B \in \mathcal A$
- Every content $\mu$ is subadditive that is; $\mu(A \cup B) \le \mu(A) + \mu(B)$ for $A, B\in \mathcal A$

### On rings
If $\mathcal A$ is a ring of sets one gets additionally: 
- *Substractivity*: for $B\subseteq A$ satisfying that $\mu(B) < \infty$ it follows that $\mu(A\setminus B) = \mu(A) - \mu(B)$ 
- $A, B\in \mathcal A$, then  $\mu(A\cup B) + \mu(A \cap B) = \mu(A) + \mu(B)$ 
- *Subadditivity*: $A_i \in \mathcal A$, with $i \in \{1, \dots, n\}$ then $$\mu\left(\bigcup_{i = 1}^n A_i\right) \le \sum_{i = 1}^n A_i$$
- $\sigma$-*Superadditivity*: For $A_i \in \mathcal A$, with $i \in \Bbb N$, pairwise disjoint satisfying that $\bigcup_{i \in \Bbb N} A_i \in \mathcal A$, then $$\mu\left(\bigcup_{i = 1}^\infty A_i\right) \ge \sum_{i = 1}^\infty A_i $$
- If $\mu$ is a finite content that is, $A\in \mathcal A$, then $\mu(A) < \infty$, then the [[Inclusion–exclusion principle|inclusion-exclusion principle]] applies: $$ \mu\left(\bigcup_{i=1}^nA_i\right) = \sum_{k=1}^n(-1)^{k+1}\!\!\sum_{I\subseteq\{1,\dotsc,n\},\atop |I|=k}\!\!\!\!\mu\left(\bigcap_{i\in I}A_i\right)$$where $A_i \in \mathcal A$ for $i \in \{1, \dots, n\}$. 
 