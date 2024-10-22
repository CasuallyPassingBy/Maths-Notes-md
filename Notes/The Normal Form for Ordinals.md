---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Ordinal Arithmetic]], [[Ordinal Numbers]]

We can define a limit of transfinite sequence of ordinals. Let $\beta_\nu$ be a transfinite sequence of ordinals, with domain $\gamma$ a limit ordinal, then we define the limit of the sequence $\beta_\nu$ such that $\beta$ if

$$ \beta = \sup_{\nu < \gamma} \beta_\nu $$

With this we can check that, addition, multiplication and, exponentiation are _********continuous********_ given that 

- $\alpha + \beta = \sup_{\nu <\gamma} (\alpha +\beta_\nu)$
- $\alpha \cdot \beta = \sup_{\nu <\gamma} (\alpha \cdot\beta_\nu)$
- $\alpha ^ \beta = \sup_{\nu <\gamma} (\alpha ^{\beta_\nu})$

It is immediate from the definitions

**Lemma**
- If $0< \alpha \le \gamma$ , then there is a greatest ordinal $\beta$ such that $\alpha \cdot \beta \le \gamma$
- If $1 < \alpha \le \gamma$, then there is a greatest ordinal $\beta$ such that $\alpha^\beta \le \gamma$

**************Lemma:************** If $\gamma$ is an arbitrary ordinal and if $\alpha \ne 0$, then there exists a unique ordinal $\beta$ and a unique $\rho<\alpha$ such that $\gamma = \alpha \cdot \beta +\rho$

********Th:******** Every ordinal $\alpha >0$ can be expresses uniquely as

$$ \alpha = \omega^{\beta_1}\cdot k_1+ \omega^{\beta_2}\cdot k_2+\cdots+ \omega^{\beta_n}\cdot k_n $$

where $\beta_1>\beta_2>\cdots>\beta_n$ and $k_i >0$ are finite for all $i <n+1$. This is an analogue of division of integers

**Def:** A weak Goodstein’s sequences starting at $m >0$ is a sequence $m_0, m_1, m_2, \dots$ of natural numbers defined as follows:

First $m = m_0$, and write $m_0$ in base $2$

$$ m_0 = \sum_{k =1}^n 2^{k_i} $$

to obtain $m_1$, increase the base by $1$ (from $2$ to $3$) and then subtract $1$:

$$ m_1 =\left( \sum_{k =1}^n 3^{k_i}\right) -1 $$

In general, to obtain $m_{k+1}$ from $m_k$ (as long $m _k \ne0$), write $m_k$ in base $k+2$, increase the base by $1$, and subtract $1$.

********Th:******** For each $m>0$, the _weak Goodstein sequence starting_ at $m$ eventually terminates with $m _n=0$ for some $n$

********Def:******** The Goodstein sequence starting at $m>0$ is a sequence $m_0, m_1, \dots$ obtained as follows: Let $m_0 =m$ and write $m_0$ in hereditary base $2$ notation. To define $m_1$ replace $2$ by $3$, and then subtract $1$, to get $m_{k+1}$ write $m_k$ in hereditary base $k+2$ notation, replace each $k+2$ by ${k+3}$, and subtract $1$.

********Th:******** For each $m>0$, the ******_Goodstein sequence starting at $m$_ eventually terminates with $m_n =0$ for some $n$