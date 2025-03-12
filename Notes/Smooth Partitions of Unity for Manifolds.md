---
tags:
  - DifferentialGeometry
---
Subjects: [[Topology]], [[Differential Geometry]]
Links: [[Partitions of Unity]], [[Topological Manifolds]], [[Smooth or Differentiable Manifolds]], [[Locally Finite Collections]], [[Smooth Functions on Smooth Manifolds]]

# Bump Functions

**Def:** The *support* of a real-valued function $f$ on a manifold is define to be the closure in $M$ of the subset on which $f\neq 0$. $$\text{supp} (f) := \text{cl}_M (f^{-1}[\Bbb R^\times]) $$
Let $q$ be a point in $M$, and $U$ a neighbourhood of $q$. By a *bump function at $q$ supported in $U$* we mean any continuous nonnegative function $\rho$ on $M$ that is $1$ in a neighbourhood of $q$ with $\text{supp}(\rho) \subseteq U$. 

To define a smooth bump function on $0$ supported in $(-b, b)$, with $b>0$. We need a couple preliminary functions. Let $f: \Bbb R\to \Bbb R$ defined as $$f(x) = \begin{cases}e^{-1/x} & x  > 0 \\0 & x \le 0\end {cases}$$Note that $f$ is smooth. Using $f$, we can construct a smooth step function $g: \Bbb R \to \Bbb R$, defined by $$g(x) = \frac{f(x)}{f(x)+ f(1-x)}.$$If we calculate the cases, we have if $x \le 0$, then $g(x) = 0$, if $x\ge 1$, we have that $1-x \le 0$, then $g(x) = 1$. Lastly, we see that $g$ is smooth since the denominator is never equal to $0$, and the two functions of the numerator and denominator are smooth. 

Given two positive real numbers $0< a< b$, we make a linear change of variables to map $[a^2, b^2]$ to $[0, 1]$: $$x \mapsto \frac{x-a^2}{b^2-a^2}$$Then $$h (x) = g\left(\frac{x-a^2}{b^2-a^2}\right)$$and so $h$ is a smooth step function such that $x  \le a^2$, then $h(x) = 0$ and $x \ge b^2$ then $h(x) = 1$. If we replace $x$ by $x^2$ to make the function symmetric in $x$, $k(x) = h(x^2)$. We se that if $|x| \le a$ then $k(x) = 0$ and if $|x| \ge b$, then $k(x) = 1$. 

This is the opposite of what we want. Then defining $\rho(x) = 1- k(x)$, we have that $\rho$ is a smooth bump function at $0$ in $\Bbb R$ that is identically $1$ on $[-a, a]$ and has support in $[-b, b]$. For any $q \in \Bbb R$, $\rho(x-q)$ is a smooth bump function at $q$.

We can extend the construction of the bump function from $\Bbb R$ to $\Bbb R^n$. To get a smooth bump function at $0$ in $\Bbb R^n$ that is $1$ on the closed ball $\bar B(0,a)$ and has support in the closed ball $\bar B(0,b)$, set $$\sigma (x) = \rho(\|x\|)$$ As a composition of smooth functions, $\sigma$ is smooth. To get a smooth bump function at $q$ in $\Bbb R^n$ take $\sigma(x - q)$.

**Cor:** Let $q$ be a point and $U$ any neighbourhood of $q$ in a manifold. Then there's a bump function at $q$ supported in $U$.

**Prop (Smooth extension of a function):** Suppose $f$ is a smooth function defined on a neighbourhood $U$ of a point $p$ in a manifold $M$. Then there is a smooth function $\tilde f$ on $M$ that agrees with $f$ in some possible smaller neighbourhood of $p$.

**Prop:** Let $F: N \to M$ be a smooth map of manifolds and $h: M \to \Bbb R$ s smooth real valued function. Then $\text{supp}(F^* h) \subseteq F^{-1}[\text{supp} (h)]$ 

**Cor:** Let $f: M \to \Bbb R$ be a smooth function on a manifold $M$. If $N$ is another manifold and $\pi_M: M\times N \to N$ is the projection to the first factor, then $\text{suppo}(\pi^* f) = \text{supp}(f) \times N = \pi^{-1}[\text{supp}(f)]$. 

# Smooth Partitions of Unity

**Def:** A *smooth partition of unity* on a manifold is a collection of nonnegative smooth functions $\{\rho_\alpha: M \to \Bbb R \mid \alpha < \kappa\}$ such that: the collection of supports $\{\text{supp}(\rho_\alpha) \mid \alpha < \kappa\}$ is locally finite, and $$\sum_{\alpha < \kappa} \rho_\alpha = 1$$
Given an open cover $\{U_\alpha \mid \alpha < \kappa\}$ of $M$, we say that the partition of unity $\{\rho_\alpha \mid \alpha < \kappa\}$ is *subordinate to the open cover* $\{U_\alpha \mid \alpha < \kappa\}$ if $\text{supp}(\rho_\alpha) \subseteq U_\alpha$ for every $\alpha < \kappa$. 

**Obs:** Suppose $\{f_\alpha \mid \alpha < \kappa\}$ is a collection of smooth functions on manifold $M$ such that the collection of its supports $\{\text{supp}(f_\alpha) \mid \alpha < \kappa\}$ is locally finite. Then every point $q$ in $M$ has a neighbourhood $W_q$ that intersects finite elements of $\{\text{supp}(f_\alpha) \mid \alpha < \kappa\}$. Thus on $W_q$ the sum $\sum_{\alpha < \kappa} f_\alpha$ is actually a finite sum. This shows that the function $f = \sum_{\alpha< \kappa} f_\alpha$ is well defied and a smooth on manifold. $M$. We call such a sum a *locally finite sum*.

## Existence of a Partition of Unity

**Lemma:** If  $\{\rho_\alpha: M \to \Bbb R \mid \alpha < \kappa\}$ a collection of smooth functions such that the collection of their supports is locally finite, then $$ \text{supp}\left(\sum_{\alpha < \kappa} \rho_\alpha\right) \subseteq \bigcup_{\alpha< \kappa} \text{supp}(\rho_\alpha)$$
**Prop:** Let $M$ be a compact manifold and $\{U_\alpha \mid \alpha < \kappa\}$ on open cover of $M$. There exists a smooth partition of unity $\{\rho_\alpha: M \to \Bbb R \mid \alpha < \kappa\}$ subordinate to $\{U_\alpha \mid \alpha < \kappa\}$. 

**Th (Existence of a smooth partition of unity):** Let $\{U_\alpha \mid \alpha < \kappa\}$ be an open cover of a manifold $M$:
- There is a smooth partition of unity $\{\varphi_k \mid k < \omega\}$ with every $\varphi_k$ having compact support such that for each $k$, $\text{supp}(\varphi_k) \subseteq U_\alpha$ for some $\alpha < \kappa$.
- If we do not require compact support, then there is a smooth partition of unity $\{\rho_\alpha \mid \alpha < \kappa\}$ subordinate to $\{U_\alpha \mid \alpha < \kappa\}$.

**Cor (Existence of Bump function)**: Let $M$ be a manifold, and $A \subseteq M$ a closed set, and $U \subseteq M$ an open set containing $A$. Then, there's a smooth function $f: M \to \Bbb R$ such that $f|_B = 1$ and $\text{supp}(f) \subseteq U$. 

**Cor (Smooth Uryshon Lemma):** Let $M$ be a manifold. If $A, B\subseteq M$ are closed sets such that $A \cap B = \varnothing$, then there exists a smooth function $f: M \to \Bbb R$ such that $f|_A = 0$ and $f|_B = 1$.

**Prop:** Suppose $\{\rho_\alpha \mid \alpha < \kappa \}$ is a partition of unity on a manifold $M$ subordinate to an open cover $\{U_\alpha \mid \alpha < \kappa\}$ of $M$ and $F: N \to M$ is a smooth map. Then the collection of functions $\{F^*\rho_\alpha \mid \alpha < \kappa \}$ is a partition of unity on $N$ subordinate to the open cover $\{F^{-1}[U_\alpha] \mid \alpha < \kappa\}$ of $N$.