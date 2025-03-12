---
tags:
  - VectorAnalysis
---

Links: [[Jordan Measure]], [[Topological Characterization of Continuity in Rn]], [[Inverse Function Theorem in Rn]]

**Def:** Let $g:A\subseteq \Bbb R^n\to \Bbb R^m$, satisfying satisfies the Lipschitz uniformity condition on $A$ if there exist $L>0$, and $\delta>0$ such that for any $x, y \in A$, if $\|x-y\| < \delta$
$$ \|g(x)-g(y)\| \le L \|x-y\| $$

**Prop:** Let $g:A\subseteq \Bbb R^n\to \Bbb R^m$, satisfying satisfies the Lipschitz uniformity condition on $A$, with $L>0$ and $\delta >0$, then $g$ is uniformly continuous.

********Lemma:******** Let $D \subseteq \Bbb R^n$ be an open set and $K \subseteq D$ compact. If $g: D\to \Bbb R^n$ satisfies the Lipschitz uniformity condition with $L>0$ and $\delta>0$, if for some $a > 0$
$$ \overline J(A) < \dfrac{a}{4(2L\sqrt{n})^n} $$
then $$ \overline J(g(A)) < a $$**Th:** Let $D \subseteq \Bbb R^n$ be an open set and $K \subseteq D$ compact. If $g: D\to \Bbb R^n$ satisfies the Lipschitz uniformity condition with $L>0$ and $\delta>0$ and $J(K) = 0$, then $J(g[K]) = 0$

********Lemma:******** Let $D \subseteq \Bbb R^n$ be an open set and $K \subseteq D$ compact. If $g: D \to \Bbb R^n$ is $\mathcal C^1$ on $D$, then $g$ satisfies the Lipschitz uniformity condition on $K$.

**Prop:** Let $A \subseteq \Bbb R$ an open set and $B \subseteq A$. If $f:A\to \Bbb R$ is a differentiable function on $A$ and satisfies the Lipschitz uniformity condition, then $f'$ is bounded on $B$.

********Lemma:******** Let $\Omega \subseteq \Bbb R^n$ be an open set, let $D \subseteq \Bbb R^n$ bounded such that $\operatorname{cl}(D) \subseteq \Omega$. If ${g:\Omega \to \Bbb R^n}$ is a $\cal C^1$ function on $\Omega$ and $\det (dg_x) \ne 0$, for any $x \in \operatorname{int}(D)$, then ${\partial (g[D]) \subseteq g[\partial D]}$.

### Important Theorem

********Th:******** Let $\Omega \subseteq \Bbb R^n$ be an open set, let $D \subseteq \Bbb R^n$ Jordan-measurable and such that $\operatorname{cl}(D) \subseteq \Omega$. If ${g:\Omega \to \Bbb R^n}$ is a $\cal C^1$ function on $\Omega$ and $\det (dg_x) \ne 0$, for any $x \in \operatorname{int}(D)$, then $g[D]$ is Jordan-measurable.