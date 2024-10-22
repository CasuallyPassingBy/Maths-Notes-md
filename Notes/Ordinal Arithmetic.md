---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Orderings]], [[Well-Orderings]], [[Ordinal Numbers]]

**Def: Addition of Ordinal numbers:** for all ordinals $\beta$,
- $\beta +0 = \beta$
- $\beta+(\alpha+1) = (\beta+\alpha)+1$ for all $\alpha$
- $\beta + \alpha = \sup \{\beta + \gamma \mid \gamma < \alpha\}$ for all $\alpha \ne 0$

********Th:******** Let $(W_1, <_1)$ and $(W_2, <_2)$ be well-ordered sets, isomorphic to ordinals $\alpha_1$ and $\alpha_2$, respectively, and let $(W ,<)$ be the sum of $(W_1, <_1)$ and $(W_2, <_2)$. Then $(W,<)$ is isomorphic to the ordinal $\alpha_1 +\alpha_2$.

********Lemma:********
- If $\alpha_1$, $\alpha_2$ are ordinals, then $\alpha_1 < \alpha_2$ iff $\beta +\alpha_1 < \beta +\alpha_2$
- For all ordinals $\alpha_1$, $\alpha_2$ and $\beta$, $\beta +\alpha_1 = \beta+\alpha_2$ iff $\alpha_1= \alpha_2$
- $(\alpha+\beta)+\gamma = \alpha +(\beta+\gamma)$

**************Lemma:************** for every ordinal $\alpha$, there is a unique limit ordinal $\beta$ and a unique natural number $n$ such that $\alpha = \beta +n$

**************Lemma:************** If $\alpha \le \beta$ then there’s a unique ordinal number $\xi$ such that $\alpha +\xi = \beta$

**Def: Multiplication of ordinals:** for all ordinals $\beta$

- $\beta\cdot 0 =0$
- $\beta\cdot (\alpha+1) = \beta\cdot \alpha+ \beta$ for all $\alpha$
- $\beta\cdot \alpha = \sup\{ \beta\cdot \gamma \mid \gamma < \alpha\}$ for all limit $\alpha \ne 0$

********Th:******** Let $\alpha$ and $\beta$ be ordinal numbers. Both the lexicographical and the anti-lexicographical orderings of the product $\alpha \times \beta$ are well-orderings. The order type of the anti-lexicographical ordering of ${\alpha \times \beta}$ is $\alpha \cdot \beta$, while the lexicographical ordering of $\alpha \times \beta$ is $\beta\cdot \alpha$

**Lemma:**
- If $\alpha_1$, $\alpha_2$ are ordinals, and $\beta \ne 0$, then $\alpha_1 < \alpha_2$ iff $\beta \cdot \alpha_1 < \beta \cdot \alpha_2$
- For all ordinals $\alpha_1$, $\alpha_2$ and $\beta$, and $\beta \ne 0$, $\beta \cdot \alpha_1 = \beta\cdot \alpha_2$ iff $\alpha_1= \alpha_2$
- $(\alpha\cdot\beta)\cdot \gamma = \alpha \cdot(\beta\cdot\gamma)$
- $\alpha\cdot (\beta+\gamma) = \alpha \cdot\beta+ \alpha \cdot\gamma$

********************************************************************************Def: Exponentiation of Ordinal Numbers:******************************************************************************** for all $\beta$,

- $\beta^0 =1$
- $\beta^{\alpha+1} = \beta^\alpha \cdot \beta$ for all $\alpha$
- $\beta^\alpha = \sup\{\beta^\gamma \mid \gamma< \alpha\}$ for all limit $\alpha \ne 0$

**Th:** Let $\alpha$ and $\beta$ be ordinals. For $f: \beta \to \alpha$, let $s(f)= \{\xi <\beta\mid f(\xi ) \ne 0\}$. Let $S(\beta, \alpha) = \{f \mid f:\beta \to \alpha \text{ and } s(f) \text{ is finite}\}$. We define $\prec$ on $S(\beta, \alpha)$ as: $f\prec g$ iff there’s $\xi _0 < \beta$ such that $f(\xi_0) < g(\xi_0)$ and $f(\xi) = g(\xi )$ for all $\xi > \xi_0$. Then $(S(\beta, \alpha), \prec)$ is isomorphic to ${(\alpha^\beta, <)}$

**Lemma:**
- $\alpha ^{\beta+\gamma} = \alpha ^\beta \cdot \alpha^\gamma$
- $(\alpha^\beta)^\gamma = \alpha^{\beta\cdot \gamma}$
- If $\alpha \le \beta$, then $\alpha ^\gamma \le \beta^\gamma$
- if $\alpha>1$ and if $\beta< \gamma$, then $\alpha ^\beta < \alpha ^\gamma$

**Def:** We want to add an important ordinal defined as

$$ \varepsilon_0 := \sup\{ {^n \omega} \mid n < \omega\} = \sup \{ \omega, \omega^\omega, \omega^{\omega^\omega}, \dots, \} $$

and has the property of being the smallest ordinal number $\alpha$ such that $\omega^\alpha = \alpha$.