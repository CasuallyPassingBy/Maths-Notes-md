---
tags:
  - MeasureTheory
  - FunctionalAnalysis
---
Subjects: [[Measure Theory]], [[Functional Analysis]]
Links: [[Space of Continuous Functions]], [[Local Compactness]], [[Hausdorff Spaces]], [[Space of Continuous Compactly Supported Functions]], [[Measures on Hausdorff Spaces]]

**Def:** Let $X$ be a locally compact Hausdorff space, and let $f$ be a real- or complex-valued functions on $X$. Then $f$ is said to *vanish at infinity* if for every $\varepsilon>0$ there is a compact subset of $K$ of $X$ such that $|f(x)|<\varepsilon$ holds at each $x\in X \setminus K$. We will denote by $\mathcal C_0(X)$the set of all real-value functions on $X$ that vanish at infinity, and by $\mathcal C_0(X, \Bbb C)$ the set of all complex-valued continuous functions on $X$ that vanish at infinity.

**Prop:** Let $X$ be a locally compact Hausdorff space. Then $\mathcal C_0(X)$ and $\mathcal C_0(X, \Bbb C)$ are Banach spaces using the $\|\cdot\|_\infty$-norm. 

**Prop:** Let $X$ be a locally compact Hausdorff space. Then every positive linear functional on $\mathcal C_0(X)$ is continuous. 

**Prop:** Let $X$ be a locally compact Hausdorff space. Then for each continuous linear functional $L$ on $\mathcal C_0(X)$ there are positive continuous linear functionals $L_+$ and $L_-$ on $\mathcal C_0(X)$ such that $L = L_+ - L_-$. We define $L_+$ by $$L_+(f) := \sup \{L(g) \mid g\in \mathcal C_0(X) \land 0\le g\le f\}, $$and the functional $L_- := L- L_+$. In addition, this decomposition is minimal in the sense that if $L = L_1-L_2$ is another decomposition of $L$ into a difference of positive linear functionals $L_1(f) \ge L_+(f)$ and $L_2(f) \le L_-(f)$ hold for each nonnegative $f\in \mathcal C_0(X)$. 

**Riesz–Markov–Kakutani Representation Theorem:** Let $X$ be a locally compact Hausdorff space. Then the map that takes finite signed, or complex, regular Borel measure $\mu$ to the functional $f\mapsto \int f\, d\mu$ is an isometric isomorphism of the Banach space $M_r(X, \Bbb R)$, or $M_r(X, \Bbb C)$, onto the [[Topological Dual Vector Space|dual]] of the Banach space $\mathcal C_0(X)$, or $\mathcal C_0(X, \Bbb C)$. 

**Prop:** Let $X$ be a locally compact Hausdorff space, let $X^*$ be its [[Alexandroff compactification|one-point compactification,]] and let $x_\infty$ be the point at infinity. Then a function $f: X\to \Bbb R$ belongs to $\mathcal C_0(X)$ iff the function $f^*: X^* \to \Bbb R$ defined by  $$f^*(x) := \begin{cases}f(x)& x\in X, \\ 0 & x = x_\infty, \end{cases}$$is continuous. 

**Cor:**  If $X$ is a second countable locally compact Hausdorff space, then $\mathcal C_0(X)$ is separable.

**Prop:** Let $X$ be a locally compact Hausdorff space, and let $\mu$ be a regular Borel measure on $X$ such that $\mu(X) = \infty$. Then there is a nonnegative function $f\in\mathcal C_0(X)$ such that $$\int f\, d\mu = \infty.$$