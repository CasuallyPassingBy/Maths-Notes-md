---
tags:
  - Topology
---
deSubjects: [[Topology]]
Links: [[Weak Topology]], [[Continuous Functions and Homeomorphims]], [[Separable, First and Second Countable Spaces]], [[Functions]], [[Tychonoff spaces]], [[Separation Axioms]], [[Convergence of Nets]], [[Convergence of Filters]], [[Topological Subspaces]]

Let consider the family of nonempty topological spaces $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$, where $\kappa$ is a nonzero cardinal. Remember that $$ \prod_{\alpha< \kappa} X_i = \left\{ \left. f:\kappa\to \bigcup_{\alpha < \kappa}X_\alpha\; \right|\; \forall \alpha< \kappa[f(\alpha) \in X_\alpha]\right\} $$
For each $\alpha< \kappa$, we can define the function $\pi_\alpha: \prod_{\beta<\kappa}X_\beta \to X_\alpha$ as $\pi_\alpha(f) = f(\alpha)$ for each $\prod_{\beta<\kappa}X_\beta$. To $\pi_\alpha$ is called the *$\alpha$th projection.* We group the projections into a collection $\mathcal P = \{\pi_\alpha \mid \alpha < \kappa\}$.

**Def:** We consider initial topology $\,_\mathcal P \tau$ on $\prod_{\alpha < \kappa} X_\alpha$ induced by the projections. The pair $\left(\prod_{\alpha < \kappa} X_\alpha, \,_\mathcal P\tau\right)$ is called the *topological product* or *the Tychonoff product* of the spaces $X_\alpha$, and to $\,_\mathcal P \tau$ is called the *product topology* or *Tychonoff topology* on the product $\prod_{\alpha<\kappa} X_\alpha$. 

**Prop:** 
- For each $\alpha < \kappa$, $\pi_\alpha: \left(\prod_{\alpha < \kappa} X_\alpha, \,_\mathcal P\tau\right) \to (X_\alpha, \tau_\alpha)$ is continuous
- $\,_\mathcal P \tau$ is the smallest topology such that each $\pi_\alpha$ continuous.
- If $Z$ is a topological space and $g: Z \to \prod_{\alpha< \kappa} X_\alpha$. $g$ is continuous iff $\pi_\alpha \circ g$ is continuous for each $\alpha<\kappa$.

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
Z \arrow[dr,"\pi_\alpha \circ g"'] \arrow[r, "g"] &\prod_{\beta<\kappa}X_\beta \arrow[d, "\pi_\alpha"] \\ 
& X_\alpha
\end{tikzcd}
\end{document}
```

- The family $\mathcal S = \{\pi_\alpha^{-1}[A] \mid \alpha < \kappa, A \in \tau_\alpha\} = \bigcup_{\alpha < \kappa} \pi_\alpha^{-1}[\tau_\alpha]$ is a subbase for $\,_\mathcal P \tau$. 

**Obs**: Let $\mathcal B_\alpha$ be the base for the topological space $(X_\alpha, \tau_\alpha)$. Since $\bigcup_{\alpha < \kappa} \pi_\alpha^{-1}[\mathcal B_\alpha]$ is a subbase of the product topology, then the sets $\prod_{\alpha < \kappa} A_\alpha$ where $A_\alpha \in \mathcal B_\alpha$ with $F \in [\kappa]^{<\omega}$ and $\alpha \in \kappa\setminus F$, $A_\alpha = X_\alpha$, form a base for $\prod_{\alpha< \kappa} X_\alpha$.

**Prop:** If $\{X_\alpha\mid \alpha<\kappa\}$ is a family of topological spaces and $A_\alpha$ is a subspace of $X_\alpha$ for every $\alpha<\kappa$, then the two topologies defined on the set $A = \prod_{\alpha<\kappa} A_\alpha$, viz., the topology of the Tychonoff product of spaces $\{A_\alpha \mid \alpha<\kappa\}$ and the topology of a subspace of the Tychonoff product $\prod_{\alpha<\kappa} X_\alpha$, coincide. 

**Prop:** The projection $\pi_\alpha: \prod_{\beta < \kappa}X_\beta \to X_\alpha$ defined as $\pi_\alpha(f) = f(\alpha)$ for each $f \in \prod_{\beta< \kappa} X_\beta$, is an open function for each $\alpha < \kappa$.

**Prop:** A sequence $(x_n)_{n <\omega}$ of points in $\prod_{\beta < \kappa}X_\beta$ converges to a point $x$ of $\prod_{\beta < \kappa}X_\beta$ iff for each $\alpha < \kappa$, the sequence $(\pi_\alpha(x_n))_{n < \omega}$ converges to the point $\pi_\alpha(x)$. 

**Prop:** For every family of sets $\{A_\alpha \}_{\alpha<\kappa}$, where $A_\alpha<\kappa\subseteq X_\alpha$, in the Tychonoff product $\prod_{\alpha<\kappa} X_\alpha$ we have  $$\overline{\prod_{\alpha<\kappa} A_\alpha} = \prod_{\alpha<\kappa} \overline{A_\alpha}. $$
**Cor:** The set $\prod_{\alpha <\kappa} A_\alpha$, where $\varnothing\neq A_\alpha\subseteq X_\alpha$ is closed in the Tychonoff product $\prod_{\alpha<\kappa} X_\alpha$ iff $A_\alpha$ is closed in $X_\alpha$ for every $\alpha<\kappa$. 

**Cor:** The set $\prod_{\alpha <\kappa} A_\alpha$, where $\varnothing\neq A_\alpha\subseteq X_\alpha$ is dense in the Tychonoff product $\prod_{\alpha<\kappa} X_\alpha$ iff $A_\alpha$ is dense in $X_\alpha$ for every $\alpha<\kappa$. 

**Prop:** For any $A\subseteq X$ and $B\subseteq Y$ in the Tychonoff product $X\times Y$ we have  $$\text{Int}(A \times B) = \text{Int}(A)\times \text{Int}( B)\quad \text{and}\quad \text{Fr}(A \times B) = (\overline A \times \text{Fr}(B)) \cup (\text{Fr}(A) \times \overline B). $$

**Prop:** Let $\{X_s\mid s\in S\}$ be a family of topological spaces. If $S = \bigcup_{t\in T} S_t$, where $S_t \cap S_r = \varnothing$ for $r \neq t$. Then the spaces $\prod_{s\in S}X_s$ and $\prod_{t\in T}\left(\prod_{s\in S_t}X_s\right)$ are homeomorphic, i.e., the Tychonoff product is associative. 

**Prop:** Let $\phi: \kappa \to \kappa$ be a bijective function, and $\{X_\alpha\mid \alpha < \kappa\}$ a family of nonempty topological spaces. Then $$\prod_{\alpha < \kappa} X_\alpha \cong \prod_{\alpha < \kappa} X_{\phi(\alpha)}.$$Meaning that the topological product is commutative.

**Obs:** Let $\{X_\alpha \mid \alpha<\kappa\}$ be a collection of topological spaces. We see that the projection $\pi_\alpha: \prod_{\beta<\kappa} X_\beta\to X_\alpha$ is an open map for every $\alpha <\kappa$. The projections aren't necessarily closed, in general. 

**Prop:** Let $\{X_\alpha \mid \alpha < \kappa\}$ and $\{Y_\alpha \mid \alpha < \kappa\}$ two families of topological spaces, then if for each $\alpha < \kappa$, $X_\alpha \cong Y_\alpha$. Then $\prod_{\alpha < \kappa} X_\alpha \cong \prod_{\alpha < \kappa} Y_\alpha$. 

**Prop:** Let $\{X_\alpha \mid \alpha < \kappa\}$ be family of nonempty topological spaces.
- If for each $X_\alpha$ is second countable and $\kappa \le \omega$, then the Tychonoff product $X =\prod_{\alpha < \kappa} X_\alpha$ is second countable.
- If $X =\prod_{\alpha < \kappa} X_\alpha$ is second countable, then $X_\alpha$ is second countable.

**Prop:** Let $X = \prod_{n <\omega}X_n$ be the countable product of separable spaces, then $X$ is separable.

**Prop:** Let $X = \prod_{\alpha < \kappa} X_\alpha$ is first countable iff for each $\alpha < \kappa$, $X_\alpha$ is first countable and $\kappa \le \omega$. 

**Def:** For each $\alpha < \kappa$, there's a function $f_\alpha: X_\alpha \to Y_\alpha$ be a function between topological spaces. We can define the *product function* $\prod_{\alpha < \kappa}f_\alpha$ with domain $\prod_{\alpha < \kappa} X_\alpha$ and codomain $\prod_{\alpha < \kappa} Y_\alpha$, defined by the following way: $$
\left(\pi_\alpha\circ\prod_{\alpha < \kappa} f_\alpha\right)(x) = \left(\prod_{\beta < \kappa} f_\beta\right)(x)(\alpha) = f_\alpha(x_\alpha)
$$for each $\alpha < \kappa$. 

**Obs:** Let $\{f_\alpha:X_\alpha \to Y_\alpha\mid \alpha<\kappa\}$ a collection of continuous functions. If $\{A_\alpha\subseteq X_\alpha \mid \alpha<\kappa\}$ and $\{B_\alpha\subseteq Y_\alpha\mid \alpha<\kappa\}$, then  $$\left(\prod_{\alpha<\kappa} f_\alpha\right)\left[\prod_{\alpha<\kappa} A_\alpha\right] = \prod_{\alpha<\kappa} f_\alpha[A_\alpha] \quad \text{and}\quad \left(\prod_{\alpha<\kappa} f_\alpha\right)^{-1}\left[\prod_{\alpha<\kappa} B_\alpha\right] = \prod_{\alpha<\kappa} f_\alpha^{-1}[B_\alpha]. $$
**Prop:** Let $\{f_\alpha: X_\alpha \to Y_\alpha \mid \alpha < \kappa\}$ be a family of functions between topological spaces, then the product family $\prod_{\alpha < \kappa}f_\alpha: \prod_{\alpha < \kappa}X_\alpha \to \prod_{\alpha < \kappa}Y_\alpha$ satisfies the following:
- $\prod_{\alpha < \kappa}f_\alpha$ is continuous iff for each $\alpha<\kappa$, $f_\alpha$ is continuous.
- $\prod_{\alpha < \kappa} f_\alpha$ is open iff for each $\alpha < \kappa$, $f_\alpha$ is open. 

**Universal Property of the Product Topology:** If $Y$ is topological space, and for every $\alpha < \kappa$, $f_\alpha: Y \to X_\alpha$ is a continuous function, then there exists *precisely one* continuous map $f: Y \to \prod_{\beta<\kappa}X_\beta$ such that for every $\alpha < \kappa$ the following diagram:
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
& \prod_{\alpha<\kappa}X_\alpha \arrow[d, "\pi_\alpha"] \\ 
Y \arrow[r,"f_\alpha"'] \arrow[ur, dashed,"f"] & X_\alpha
\end{tikzcd}
\end{document}
```

**Prop:** The topological space $X$ is homeomorphic to the Tychonoff product $\prod_{\alpha<\kappa} X_\alpha$ iff there exists a family of continuous mappings $\{\pi_\alpha:X \to X_\alpha \mid \alpha<\kappa\}$, satisfying the following conditions:
- For every $Y$ and pair of functions $f, g:Y\to X$, if $\pi_\alpha\circ f= \pi_\alpha\circ g$ for every $\alpha<\kappa$, then $f=g.$
- For every space $Y$ and a continuous mappings $\{f_\alpha: Y\to X_\alpha\mid \alpha<\kappa\}$, there exists a continuous function $f: Y\to X$ such that $\pi_\alpha \circ f= f_\alpha$ for every $\alpha<\kappa$. 

**Def:** Let $X$ be a topological space and for each $\alpha < \kappa$, there's a function $f_\alpha: X \to Y_\alpha$ where $Y_\alpha$ is a topological space. We define the *diagonal function $\Delta_{\alpha<\kappa} f_\alpha$* with domain $X$ and codomain $\prod_{\alpha < \kappa}Y_\alpha$ defined as follows: $$(\Delta_{\alpha<\kappa} f_\alpha)(x)(\beta) = f_\beta(x).$$

**Obs:** Let $\{f_\alpha:X \to Y_\alpha\mid \alpha<\kappa\}$ a collection of continuous functions. If $A\subseteq X$ and $\{B_\alpha\subseteq Y_\alpha\mid \alpha<\kappa\}$, then  $$\left(\Delta_{\alpha<\kappa} f_\alpha\right)\left[A\right] \subseteq \prod_{\alpha<\kappa} f_\alpha[A] \quad \text{and}\quad \left(\Delta_{\alpha<\kappa} f_\alpha\right)^{-1}\left[\prod_{\alpha<\kappa} B_\alpha\right] = \bigcap_{\alpha<\kappa} f_\alpha^{-1}[B_\alpha]. $$

**Prop:** Let $X$ be a topological space and for each $\alpha < \kappa$, there's a function $f_\alpha: X \to Y_\alpha$ where $Y_\alpha$ is a topological space. The diagonal function $\Delta_{\alpha<\kappa} f_\alpha$ has the following properties:
- $\Delta_{\alpha<\kappa} f_\alpha$ is continuous if for each $\alpha < \kappa$, $f_\alpha$ is continuous.
- $\Delta_{\alpha<\kappa} f_\alpha$ is open if for each $\alpha < \kappa$, $f_\alpha$ is open.

**Def:** We say that a topological property $P$ is *multiplicative* if for any family $\{X_s\mid s\in S\}$ of spaces with property $P$, the sum $\prod_{s\in S}X_s$ also has the property $P$. Similarly, we say that a property is $\kappa$-*multiplicative* if we add the condition that $|S|<\kappa$, and *finitely multiplicative* if $|S| <\aleph_0.$ 

**Th:** Any Tychonoff product of $T_i$-spaces is a $T_i$ space for $i \le 3\frac12$. If the Tychonoff product $\prod_{\alpha<\kappa}X_\alpha$ is a non-empty $T_i$ space, then all $X_\alpha$'s are $T_i$-spaces for $i \le 6$. Similarly, then if $\prod_{\alpha<\kappa}X_\alpha$ is regular or normal, then all $X_\alpha$'s are regular or normal, respectively.

**Lemma:** The space $[0, \omega)^{\omega_1}$ is not a normal space.

**(Pospíšil) Cor:** Let $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ be a family of not indiscrete topological spaces with $|X_\alpha| > 1$. If $\kappa > \omega$, then $\prod_{\alpha < \kappa} X_\alpha$ is not hereditarily normal.

**Prop:** If a topological property $P$ is hereditary with respect to both closed subsets and open subsets and is countably multiplicative, then in the class of $T_2$-spaces, $P$ is hereditary with respect to $G_\delta$-sets. 

**Th:** Let $\aleph_0\le \kappa$ be a cardinal number. If $w(X_\alpha) \le \kappa$, for every $\alpha <\tau$ and $\tau\le \kappa$, then $w(\prod_{\alpha<\tau} X_\alpha)\le \kappa$. If $\chi(X_\alpha) \le \kappa$ for every $\alpha <\tau$, and $\tau\le \kappa$, then $\chi(\prod_{\alpha<\tau}X_\alpha)\le \kappa$. 

**Cor:** First-countability and second-countability are countably multiplicative properties. 

**Prop:** Let $\kappa \ge \aleph_0$ a cardinal number, and $\{X_\alpha \mid \alpha<\kappa\}$ be a collection of topological spaces such that $w(X_\alpha) > 1$ for every $\alpha<\kappa$ . If $X := \prod_{\alpha<\kappa} X_\alpha$, then $w(X) = \kappa \cdot \sup\{w(X_\alpha) \mid \alpha<\kappa\}$. 

**Prop:** Let $\kappa \ge \aleph_0$ a cardinal number, and $\{X_\alpha \mid \alpha<\kappa\}$ be a collection of topological spaces such that $X_\alpha$ is a $T_1$-space and $|X_\alpha|>1$ for every $\alpha<\kappa$ . If $X := \prod_{\alpha<\kappa} X_\alpha$ and $x\in X$, then $\chi(x, X) = \kappa\cdot \sup\{\chi(\pi_\alpha(x), X_\alpha) \mid \alpha<\kappa\}$. 

**The Hewitt-Marczewski-Pondiczery Theorem:** Let $\kappa \ge \aleph_0$ be a cardinal number. If $d(X_\alpha) \le \kappa$ for every $\alpha<\tau$ and $\tau \le 2^\kappa$, then $d(\prod_{\alpha<\tau} X_\alpha) \le \kappa$. 

**Cor:** Separability is a $\frak c$-multiplicative property.

**Th:** Let $\kappa\ge\aleph_0$ be an cardinal number. If $d(X_\alpha) \le \kappa$ for every $\alpha<\tau$, then any family of pairwise disjoint non-empty open subsets of the Tychonoff product $\prod_{\alpha<\tau} X_\alpha$ has cardinality at most $\kappa$. 

**Cor:** In the Tychonoff product of separable spaces any family of pairwise disjoint non-empty open sets is countable.

**Def:** Suppose we are given a topological space $X$, a family $\{Y_\alpha \mid \alpha<\kappa\}$ of topological spaces and a family of continuous mappings $\mathcal F := \{f_\alpha: X\to Y_\alpha\}$. We say that the family $\cal F$ *separates points* if for every pair of distinct points $x, y\in X$ there exists a mapping $f_\alpha\in \cal F$ such that $f_\alpha(x) \neq f_\alpha(y)$. If for every $x\in X$ and every closed set $F\subseteq X$ such that $x\notin F$ there exists a mapping $f_\alpha\in \cal F$ such that $f_\alpha(x) \notin \overline{f_\alpha[F]}$, then we say that the family $\cal F$ *separates points and closed sets*. 

**Obs:** Let us not that if $X$ is a $T_0$-space, then every family $\cal F$ separating points and closed sets separates points as well. 

**Lemma:** If the continuous mapping $f:X \to Y$ is injective and the one-element family $\{f\}$ separates points and closed sets, then $f$ is a homeomorphic embedding. 

**The Diagonal Theorem:** Let $X$ be a topological space, and $\{Y_\alpha\mid \alpha<\kappa\}$ be a family of topological spaces. If the family ${\cal F} := \{f_\alpha: X\to Y_\alpha\mid \alpha<\kappa\}$  of continuous functions separates points, then the diagonal $\Delta_{\alpha<\kappa} f_\alpha: X \to \prod_{\alpha<\kappa} Y_\alpha$ is a injective function. If, in addition, the family $\cal F$ separates points and closed sets, then $f$ is a homeomorphic embedding. In particular, if there is an $\alpha<\kappa$ such that $f_\alpha$ is a homeomorphic embedding, then $f$ is a homeomorphic embedding. 

**Prop:** Let $X$ be a topological space, let $\{Y_\alpha\mid \alpha<\kappa\}$ be a family of topological spaces, and let ${\cal F} := \{f_\alpha: X\to Y_\alpha\mid \alpha<\kappa\}$be a family of continuous functions. The diagonal $f = \Delta_{\alpha<\kappa} f_\alpha$ is a homeomorphic embedding iff the family $\cal F$ separates points and the family $\{f_F \mid F\in [\kappa]^{<\omega}\}$ separates points and closed sets $f_F := \Delta_{\alpha\in F} f_\alpha .$

**Cor:** The diagonal $\Delta$ of the Tychonoff product $X^\kappa$ is homeomorphic to $X$.  

**Def:** By the *graph of a mapping* $f$ of space $X$ to a space $Y$, we mean the subset of the Tychonoff product $X \times Y$ defined by $$ \Gamma(f) := \{(x, y) \in X \times Y \mid y = f(x) \}. $$
**Cor:** For every continuos $f:X \to Y$ the graph $\Gamma(f)$ is the image of $X$ under the homeomorphic embedding $\text{id}_X \Delta f: X \to X\times Y$. The restriction $\pi|_{\Gamma(f)}$ of the projection $\pi: X\times Y \to X$ is a homeomorphism. if $Y$ is Hausdorff, then $\Gamma(f)$ is closed subset of $X\times Y$.

**Prop:** If The Cartesian product $f:= \prod_{\alpha<\kappa} f_\alpha$, where $f_\alpha: X_\alpha\to Y_\alpha$ and $X_\alpha \neq \varnothing$  for $\alpha<\kappa$ is closed, then all mappings $f_\alpha$ are closed. 

**Prop:** If The Cartesian product $f:= \prod_{\alpha<\kappa} f_\alpha$, where $f_\alpha: X_\alpha\to Y_\alpha$ and $X_\alpha \neq \varnothing$  for $\alpha<\kappa$ is open iff all the functions $f_\alpha$ are open and there exists a finite set $F\in [\kappa]^{<\omega}$ such that $f_\alpha$ is surjective for $\alpha \in \kappa\setminus F$. 

**Prop:** If the mappings $f_0, \dots, f_k$ where $f_i: X\to Y_i$ are closed $Y_0$ is a $T_0$-space and $Y_1,\dots, Y_k$ are $T_3$-spaces, then the diagonal $\Delta_{n<k+1} f_n$ is closed. 

**Prop:** If the diagonal $\Delta_{\alpha<\kappa} f_\alpha$, where $f_\alpha: X\to Y_\alpha$, is open, then all mappings $f_\alpha$ are open. 

**Prop:** A net $(x_\sigma)_{\sigma\in \Sigma}$ in the Tychonoff product $\prod_{\alpha<\kappa} X_\alpha$ converges to $x\in \prod_{\alpha<\kappa} X_\alpha$ iff the net $(\pi_\alpha(x_\sigma))_{\sigma\in\Sigma}$  converges to $\pi_\alpha(x)$ for every $\alpha<\kappa$. 

**Prop:** If $\cal F$ is filter in the Tychonoff product $\prod_{\alpha<\kappa} X_\alpha$ converges to $x\in \prod_{\alpha<\kappa} X_\alpha$ iff the filter $\pi_\alpha[\mathcal F]$  converges to $\pi_\alpha(x)$ for every $\alpha<\kappa$. 