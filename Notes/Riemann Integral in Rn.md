---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Darboux Sums in Rn]], [[Riemann Integral in R]]

**Def:** Let $f: R\subseteq \Bbb R^n\to \Bbb R$ bounded over the rectangle $R$. We say that $f$ is **Riemann integrable*** (or simply _********integrable)*********_ over $R$ if the lower integral and the upper integral of $f$ over $R$ are equal. In other words
$$ \underline{\int _R} f = \overline {\int_R} f $$
in this case, this number is called ***************_the integral of $f$ over $R$_ and denoted by

$$ \int_R f $$

### Riemann Criterion of Integrability
Let $f:R\to \Bbb R$ bounded over $R$. $f$ is integrable over $R$ with integral $I$ iff for any $\varepsilon >0$ there’s a $\delta>0$ such that any partition $P$ into rectangles $R_1, R_2, \dots, R_N$ with sides $< \delta$ and if ${x_1 \in R_1, x_2 \in R_2, \dots ,x_N\in R_N}$ we have that

	$$ \left|\sum_{k = 1}^N f(x_i)\cdot m(R_i) - I\right| < \varepsilon $$

### Darboux Criterion of Integrability
Let $f:R \to \Bbb R$ bounded over $R$. $f$ is Integrable over $R$ iff for all $\varepsilon >0$ there’s a partition $\mathcal P$ such that

$$ U(f, \mathcal P) -L(f, \mathcal P) < \varepsilon $$

since it can be used a lot the difference of the upper and lower sum. I will use the shorter notation

$$ \Delta(f, \mathcal P) := U(f, \mathcal P) -L(f, \cal P) $$

********Th:******** Let $f:R\to \Bbb R$ be continuous over the rectangle $R$. Then $f$ is integrable over $R$.

**************Lemma:************** If $f:R \to \Bbb R$ is integrable over $R$, and $R'$ is a subrectangle of $R$. Then $f$ is integrable over $R'$

**************Lemma:************** If $f:R\to \Bbb R$ be integrable over $R$. Then for any $\varepsilon>0$, there’s a partition such that there’s an $i \in \{1, \dots, k\}$ where $k$ is the number of subrectangles of the partition such that

$$ M_i -m_i < \varepsilon $$

***************Th:*************** Let $f:R \to \Bbb R$ be integrable over $R$. Then there’s an $x_0 \in \operatorname{int}(R)$ such that $f$ is continuous at $x_0$

********Def:********* Let $f: A \subseteq \Bbb R^n \to \Bbb R$. Then the set $D_{f, A}$ or $D(f, A)$ is the set of all discontinuities of $f$ over $A$, or

$$ D(f, A) := \{x \in A\mid f \text{ is discontinuous at }x\} $$

********Cor:******** Let $f: R\to \Bbb R$ is integrable over $R$. Then $\operatorname{int}(D(f, A)= \varnothing$.

**********Cor:********** Let $f:R\to \Bbb R$ is integrable over $R$. Then $R\setminus (D(f,A))$ is dense in $R$.

- Algebraic Properties of the Integral
    ******Th:****** Let $f, g :R\subseteq \Bbb R^n\to \Bbb R$, then
    
    - $f+g$ is integrable over $R$ and
        $$ \int_R f+g = \int_R f+\int_R g $$
    - If $c \in \Bbb R$, then $cf$ is integrable over $R$ and$$ \int_R cf = c\int_R f $$
    - $f^2$ is integrable over $R$
    - $fg$ is integrable over $R$
    - $|f|$ is integrable over $R$ and $$ \left|\int_R f\right|\le \int_R |f| $$
        
    - $f \ge 0$ then $$ \int_R f \ge 0 $$
        
    - $f\ge g$ then $$ \int_R f \ge \int_R g $$
    - the functions $\max\{f,g\}$ and $\min\{f,g\}$ are integrable over $R$  

***Prop:********* Let $f:R\subseteq\Bbb R^n\to \Bbb R$ be integrable over $R$ such $f\ge 0$. If $f$ is continuous at $x_0$ and $f(x_0) >0$ then

$$ \int_R f >0 $$

********Prop:******** Let $f:R\subseteq\Bbb R^n\to \Bbb R$ be integrable over $R$ such that $f> 0$. Then

$$ \int_R f >0 $$

********Th:******** Let $f:R\subseteq\Bbb R^n\to [a,b]\subset \Bbb R$ is integrable over $R$ and $h:[a,b]\to \Bbb R$ be continuous, then $h\circ f$ is integrable over $R$.

### Mean Value Theorem for Integrals

Let $f,g:R\subseteq\Bbb R^n\to \Bbb R$ such that $f$ is continuous over $R$ and $g$ is integrable over $R$. Then

- $\int_R f = f(x_0) \cdot m(R)$ for some $x_0 \in R$
- if $g\ge 0$ then $\int_R fg = f(x_0) \int_R g$ for some $x_0 \in R$