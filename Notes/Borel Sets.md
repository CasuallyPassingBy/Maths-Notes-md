---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]], [[Topology]], [[Set Theory]]
Links: [[Rings and Algebras of Sets]], [[Ordinal Numbers#The Transfinite Induction Principle|Transfinite Induction]], [[Topological Spaces]], [[Perfect Spaces]]

# Borel Hierarchy

**Def:** Let $X$ be a topological space define $\Sigma_1^0$ to be the open subsets of $X$. For $\alpha> 1$ define $A\in \Sigma_\alpha^0$ iff there exists a sequence of $\langle B_n\mid n<\omega\rangle$ with each $B_n \in \Sigma_{\beta_n}^0$ for some $\beta_n<\alpha$ such that $$A = \bigcup_{n<\omega} X\setminus B_n. $$We define $$\Pi_\alpha^0 := \{X\setminus B \mid B\in \Sigma_\alpha^0\}, \quad \text{and} \quad \Delta_\alpha^0 := \Sigma_\alpha^0 \cap \Pi_\alpha^0.$$The Borel subsets of $X$ are defined by $$\mathcal B(X) := \bigcup_{\alpha< \omega_1} \Sigma_\alpha^0(X).$$We see that it is the smallest family of sets containing the open subsets of $X$ and closed under countable unions and complementations.

**Th:** $\Sigma_\alpha^0$ is closed under countable unions $\Pi_\alpha^0$ is closed under countable intersections, and $\Delta_\alpha^0$ is closed under complements. For any $\alpha$,  $$\Pi_\alpha ^0(X) \subseteq \Sigma_{\alpha+1}^0(X)\quad \text{and} \quad \Sigma_\alpha^0(X)\subseteq\Pi_{\alpha+1}^0(X) $$

**Th:** If $f:X \to Y$ is continuous and $A\in \Sigma_\alpha^0(Y)$, then $f^{-1}[A]$ is in $\Sigma_\alpha^0(X)$. This happens similarly, if we substitute $\Sigma_\alpha^0$ with $\Pi_\alpha^0$ and $\Delta_\alpha^0$.

**Th:** Suppose $X$ is a subspace of $Y$, then $$\Sigma_\alpha^0(X) = \{A \cap X \mid A\in \Sigma_\alpha^0(Y)\}. $$This happens similarly, if we substitute $\Sigma_\alpha^0$ with $\Pi_\alpha^0$ and $\Delta_\alpha^0$.

Note that $\Sigma_2^0$ is also referred to as $F_\sigma$ and the class $\Pi_2^0$ as $G_\delta$. 

**Th:** For $X$ a topological space and $\Pi_1^0(X)\subseteq \Pi_2^0(X)$, i.e., closed sets are $G_\delta$, then
- $\Pi_\alpha^0(X) \subseteq \Pi_{\alpha +1 }^0(X)$,
- $\Sigma_\alpha^0(X)\subseteq \Sigma_{\alpha +1 }^0(X)$, and hence
- $\Pi_\alpha^0(X) \cup \Sigma_\alpha^0(X) \subseteq \Delta^0_{\alpha +1}(X)$
- $\Sigma_\alpha^0$ is closed under finite intersections,
- $\Pi_\alpha^0$ is closed under finite unions, and
- $\Delta_\alpha^0$ is closed under finite intersections, finite unions, and complements.

**Lemma:** Suppose $X$ is second countable, then for every $\alpha$ with $\alpha \in \omega_1\setminus 1$ there exists a universal $\Sigma_\alpha^0$ set $U\subseteq 2^\omega\times X$, i.e., a set $U$ which is $\Sigma_\alpha^0(2^\omega\times X)$ such that for every $A\in \Sigma_\alpha^0(X)$ there exists $x\in 2^\omega$ such that $A = U_x$ where $U_x := \{y\in X \mid (x, y)\in U\}$. 

**Lebesgue Theorem:** For every $\alpha$ with $\alpha \in \omega_1\setminus 1$,  $$\Sigma_\alpha^0(2^\omega ) \neq \Pi_{\alpha}^0(2^\omega).$$
**Def:** We define $\text{ord}(X)$ to be the least $\alpha$ such that $\mathcal B(X) = \Sigma_{\alpha}^0(X)$. 

**Cor:** For any space $X$ which contains a homeomorphic copy of $2^\omega$ we have that $\text{ord}(X) = \omega_1$, consequently, $\omega^\omega$, $\Bbb R$ and any [[Polish Spaces|Polish space]] $X$ have $\text{ord}(X) = \omega_1$. 

## Abstract Borel Hierarchies