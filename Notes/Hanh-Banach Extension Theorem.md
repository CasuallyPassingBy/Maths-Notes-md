---
tags:
  - FunctionalAnalysis
---
Subjects: [[Functional Analysis]]
Links: [[Bounded Linear Operators]], [[Normed Vector Spaces]], [[Axiom of Choice]]

**Th:** Suppose that $M$ is a dense subspace of a normed space $X$, that $Y$ is a Banach space, and that $T_0: M \to Y$ is a bounded linear operator. Then, there is a unique continuous function $T:X \to Y$ that agrees on $T_0$ on $M$. This function is a bounded linear operator, and $\|T\| = \|T_0\|$. If $T_0$ is an isomorphism or isometric isomorphism, then $T$ has the same property.

**Def:** Let $X$ be a complex vector space. A *real-linear functional* on $X$ is a real-valued function $f$ on $X$ such that $x,y\in X$ and $\alpha \in \Bbb R$. then $f(x+y) = f(x) + f(y)$ and $f(\alpha x) = \alpha f(x)$. We call $f$ a *complex-linear functional* if it is a linear functional on $X$.

**Prop:** Let $X$ be a complex vector space and let $X_r$ be the corresponding real vector space.
- If $f$ is a complex linear functional on $X$ and $u$ is the real part of $f$, then $u$ is a real-linear functional on $X$, and $f(x) = u(x) + i u(ix)$ whenever $x\in X$. 
- If $u$ is a real-linear functional on $X$, then there is a unique complex-linear functional $f$ on $X$ such that $u$ is the real part of $f$, and $f(x) = u(x) + i u(ix)$ whenever $x\in X$. 
- Suppose that $X$ is complex normed space and that $f$ is complex-linear functional on $X$ with real part $u$. Then $f$ is bounded linear functional on $X$ iff $u$ is a bounded linear functional on $X_r$. If $f$ is bounded, then $\|f\| = |\|u\|$.

**Def:** Let $p$ be a real-valued function on a vector space $X$. Then $p$ is *positive-homogeneous* if $p(tx) = tp(x)$ whenever $t>0$ and $x\in X$, and is *(finitely) subadditive* if $p(x+y) \le p(x) + p(y)$ whenever $x, y\in X$. If $p$ has both properties, then it is said to be *sublinear functional*.

**The Vector Space Version of the Hanh-Banach Extension Theorem:** Suppose $p$ is a sublinear functional on a real vector space $X$ and that $f_0$ is linear functional on a subspace $Y$ of $X$ such that $f_0(y) \le p(y)$ whenever $y\in Y$. Then there is a linear functional $f$ on all $X$ such that the restriction of $f$ to $Y$ is $f_0$ and $f(x) \le p(x)$ whenever $x\in X$. That is, the linear functional $f_0$ can be extended to a linear functional  on $X$ that is still dominated by $p$.

**The Normed Space Version of the Hanh-Banach Extension Theorem:** Suppose $f_0$ is a bounded linear functional on a subspace $Y$ of a normed space $X$. Then there is a bounded linear functional $f$ on all $X$ such that $\|f\| = \|f_0\|$ and the restriction of $f$ to $Y$ is $f_0$. That is, the functional $f_0$ can be extended to be a bounded linear functional on $X$ having the same norm.

**Cor:** Let $Y$ be a closed subspace of a normed space $X$. Suppose that $x\in X\setminus Y$. Then there's a bounded linear functional $f$ on $X$ such that $\|f\| = 1$, $f(x) = d(x, Y)$, and $Y \subseteq \ker (f)$.

**Cor:** If $x$ is a nonzero element of a normed space $X$, then there is a bounded linear functional $f$ on $X$ such that $\|f\| = 1$ and $f(x) = \|x\|$.

**Cor:** If $x, y\in X$ such that $x\neq y$, then there's a bounded linear functional $f$ on $X$ such that $f(x)\neq f(y)$.

**Th:** Suppose that $X$ is a normed space. Let $A$ be a nonempty subset of $X$ and let $\{c_x \mid x\in A\}$ be a corresponding collection of scalars. Then the following are equivalent:
- There is a bounded linear functional $f$  on $X$ such that $f(x) = c_x$ for each $x\in A$.
- There is nonnegative real number $M$ such that $$\left|\sum_{i = 1}^n \alpha_i c_{x_i}\right| \le M \left\|\sum_{i = 1}^n \alpha_i x_i\right\|$$for each linear combination $\sum_{i = 1}^n \alpha_i x_i$ of elements of $A$, that is for each element of $\langle A \rangle$.

**Lemma:** Suppose that $f$ and $f_1, \dots, f_n$ are linear functionals on the same vector space. Then $f$ is a linear combination of $f_1, \dots, f_n$ iff $\displaystyle\bigcap_{i = 1}^n \ker f_i \subseteq \ker f$.
**Helly's Theorem:** Suppose that $X$ is normed space. Let $f_1, \dots, f_n$ be a nonempty finite collection of bounded linear functionals of $X$ and let $c_1, \dots, c_n$ be a corresponding collection of scalars. Then the following are equivalent.
- There's $x_0 \in X$ such that $f_j(x_0) = c_j$ when $j =1, \dots, n$.
- There is a nonnegative real number $M$ such that $$\left|\sum_{i = 1}^n \alpha_i c_{x_i}\right| \le M \left\|\sum_{i = 1}^n \alpha_i f_i\right\|$$for each linear combination $\sum_{i = 1}^n \alpha_i f_i$ of $f_1, \dots, f_n$, that is, for each $\langle\{f_1, \dots, f_n \}\rangle$. 

**Def:** Let $A$ be an absorbing subset of a vector space $X$. For each $x \in X$, let $\mu_A(x) := 