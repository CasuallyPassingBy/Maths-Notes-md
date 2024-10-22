---
tags:
  - VectorAnalysis
---
Links: [[Riemann Integral in Rn]], [[Riemann-Steiltjes Integral on R]]

We can have really similar definitions to the Riemann-Stieltjes integral on $\Bbb R$. We need to actually know what we mean by $\Delta \alpha$, since we have more dimensions to move about. One possible way to do it is by what I found studying probability theory. We can look at the special case of the functions $\alpha: \Bbb R^n \to \Bbb R$ that have the property: 
For any numbers $a_1 < b_1, a_2 < b_2, \dots a_n < b_n$, 
$$
\sum_{x_i \in \{a_i, b_i\}} (-1)^{\#a} \alpha(x_1, \dots, x_n) \ge 0
$$
where $\#a$ is the number of times that the variables $x_i$ takes the value $a_i$ in the evaluation of $\alpha$. Let the rectangle $R = \prod_{i = 1}^n[a_i, b_i]$, then we can define $$\Delta \alpha(R) := \sum_{x_i \in \{a_i, b_i\}} (-1)^{\#a} \alpha(x_1, \dots, x_n) \ge 0$$
We can all it an $n$ increasing function. 

## Reimann Sums
Let $f:R\to\mathbb{R}$, a _**Reimann-Stieltjes**_ sum is defined as follows, given $\dot{\mathcal{P}}\in\dot{\wp}_I$:

$$ R(f; \dot{\mathcal{P}}, \alpha) = \sum_{i= 1}^n f(t_i)\cdot \Delta \alpha(R_i) $$

### Integrability
Let $f:I\to\mathbb{R}$, be _**Reimann-Stieltjes Integrable**_ iff:

$$ \exists L\in\mathbb{R} \forall\varepsilon>0 \exists\delta>0 \forall\dot{\mathcal{P}}\in\dot{\wp}_I [\|\dot{\mathcal{P}}\|< \delta \Rightarrow |R(f,\dot{\mathcal{P}}, \alpha)-L|] $$

$L$ is called the _Riemann-Stieltjes integral_ of $f$ with respect to $\alpha$ along $I$, denoted as:

$$ \int_If(x) \,d\alpha(x) = \int_I f \,d\alpha $$


# Darboux Sums

**Def:** Let $f$ be a real-valued function defined and bounded on the rectangle $R \subseteq \Bbb R^n$, $\alpha:R \to \Bbb R$  be a $n-$increasing function, and $\cal P$ be a partition of $\cal P$. If $R_1, \dots, R_k$ are the corresponding subrectangles of $R$ induced by $\cal P$, we can define _the lower sum of $f$ over the partition $\cal P$ with respect to $\alpha$,_ denoted as $L(f, {\cal P}, \alpha)$ or $\underline S (f,{\cal P}, \alpha)$
$$
L(f, \mathcal P, \alpha ) = \sum_{i = 1}^k m_i \cdot \Delta \alpha(R_i) \quad \text{ where } \quad m_i = \inf_{x \in R_i}f(x) \quad \text{for } 1 \le i \le k $$
Similarly, we can define the ************_upper sum of $f$ over the partition $\cal P$ with respect to $\alpha$_, denoted as $U(f, \cal P)$ or $\overline S(f , P)$
$$
U(f, \mathcal P, \alpha) = \sum_{i = 1}^k M_i\cdot \Delta \alpha(R_i) \quad \text{ where } \quad M_i = \sup_{x \in R_i}f(x) \quad \text{for } 1 \le i \le k
$$

************Prop:************ Let $\cal P$ be any partition of $R$, then $L(f, \mathcal P, \alpha) \le U(f, \cal P, \alpha)$ .

************Prop:************ Let $\mathcal {P, Q} \in \mathbf P_R$. If $\cal Q$ refines $\cal P$ then $L(f, \mathcal P, \alpha) \le L(f, \cal Q, \alpha)$ and $U(f, \mathcal Q, \alpha) \le U(f, \cal P, \alpha)$

**********Prop:********** Let $\cal P$ and $\cal Q$ be partitions of $R$, then $L(f, \mathcal P, \alpha) \le U (f, \cal Q, \alpha)$

**********Def:********** Since the following sets are bounded $\{L(f, \mathcal P) \mid \mathcal P \in \mathbf P_R\}$ and $\{U(f, \mathcal P) \mid \mathcal P \in \mathbf P_R\}$, then we can consider their supremum and infimum respectively. Then

$$ \underline{\int_R} f \, d\alpha:= \sup_{\mathcal P \in \mathbf P_R} L(f, \cal P, \alpha) $$

and

$$ \overline{\int_R} f \, d\alpha:= \inf_{\mathcal P \in \mathbf P_R} L(f, \cal P, \alpha) $$

are called the **************_lower integral $f$ over $R$_ and ********_the upper integral of $f$ over $R$ with respect to $\alpha$._ In general it is true that

$$ \underline{\int _R} f\, d\alpha\le \overline{\int _R} f \, d\alpha$$
### Integrability
$f:R\to\mathbb{R}$ is _Reimann-Stieltjes integrable_ iff:

$$ \underline{\int_R}f\,d\alpha = \overline{\int_R}f\,d\alpha $$

_**Darboux-Cauchy Criterion**_ $f:I\to\mathbb{R}$ is _Reimann-Stieltjes integrable_ $(f\in\mathcal{R}_{R}(\alpha))$ iff:

$$ \forall\varepsilon>0\exists\mathcal{P}\in\wp_R(U(f,P,\alpha) - L(f,P,\alpha)<\varepsilon) $$

_**Theorem:**_
1. Given an $\varepsilon > 0$, and there’s a $\mathcal{P}$ such that satisfies the _Darboux-Cauchy Criterion,_ any refinement of $\mathcal{P}$ also satisfies it.
    
2. Given an $\varepsilon > 0$, and there’s a $\mathcal{P}$ such that satisfies the _Darboux-Cauchy Criterion,_ any $t_i, s_i \in R_i$ then:
	$$ \sum_{i=i}^n|f(s_i) - f(t_i)|\cdot \Delta \alpha(R_i) <\varepsilon $$
3. If $f\in\mathcal{R}_I(\alpha)$, and $(2)$ is satisfied, then:
$$ \left|\sum_{i=1}^nf(t_i)\cdot \Delta \alpha(R_i) -\int_I f\,d\alpha\right| $$
