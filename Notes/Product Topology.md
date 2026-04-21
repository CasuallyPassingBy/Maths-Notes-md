---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Initial Topology]], [[Continuous Functions and Homeomorphims]], [[Separable, First and Second Countable Spaces]], [[Functions]]

# Finite Products

**Def:** We call the functions $\pi_X: X \times Y \to X$ and $\pi_Y: X \times Y \to X$, defined as $\pi_X(x, y) = x$ and $\pi_Y(x, y) =y$ are the *projections*. 

**Def:** Given two topological spaces $(X, \tau_X)$ and $(Y, \tau_Y)$, we call the *product topology* or *the Tychonoff Topology* on $X \times Y$, to the initial topology induced by their projections. Meaning is the smallest topology on $X \times Y$ that make $\pi_X$ and $\pi_Y$ continuous.

**Obs:** We can see that $\{U \times V \mid U \in \tau_X, V \in \tau_Y\}$ forms a base of the product topology $\tau$.

Since we can define the product topology of two spaces, then we can inductively define for a finite product of spaces. Let $(X_1, \tau_1), \dots, (X_k, \tau_k)$ be topological spaces, then the product topology of $X_1 \times \dots \times X_k$ is the initial topology induced by $\{\pi_i: X_1 \times \dots \times X_k \to X_i \mid i\in \{1, \dots, k\}\}$ where $\pi_i: X_1 \times \dots \times X_k \to X_i$ is the *projection to the $i$th coordinate* ($\pi_i(x_1, \dots, x_k) = x_i$). When all of the sets are the same, then we denote it as $X^k$ instead of $X \times \dots \times X$ $k$-times.

**Prop:** Let $\pi_X: X \times Y \to X$ and $\pi_Y: X \times Y \to X$ are continuous and open functions when we consider $X\times Y$ having the the product topology.

**Def:** When a topological property $P$ that is shared between $X$ and $Y$, and is conserved when we consider the product topology on $X\times Y$ we say that $P$ is a *finitely productive property*. 

**Prop:** If $X$ and $Y$ are topological spaces that are second countable/first countable/separable, then $X \times Y$ is also second countable/first countable/separable.

# Arbitrary Products

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

**Prop:** The projection $\pi_\alpha: \prod_{\beta < \kappa}X_\beta \to X_\alpha$ defined as $\pi_\alpha(f) = f(\alpha)$ for each $f \in \prod_{\beta< \kappa} X_\beta$, is an open function for each $\alpha < \kappa$.

**Prop:** A sequence $(x_n)_{n <\omega}$ of points in $\prod_{\beta < \kappa}X_\beta$ converges to a point $x$ of $\prod_{\beta < \kappa}X_\beta$ iff for each $\alpha < \kappa$, the sequence $(\pi_\alpha(x_n))_{n < \omega}$ converges to the point $\pi_\alpha(x)$. 

**Prop:** Let $\phi: \kappa \to \kappa$ be a bijective function, and $\{X_\alpha\mid \alpha < \kappa\}$ a family of nonempty topological spaces. Then $$\prod_{\alpha < \kappa} X_\alpha \cong \prod_{\alpha < \kappa} X_{\phi(\alpha)}.$$Meaning that the topological product is commutative.

**Prop:** Let $\{X_\alpha \mid \alpha < \kappa\}$ and $\{Y_\alpha \mid \alpha < \kappa\}$ two families of topological spaces, then if for each $\alpha < \kappa$, $X_\alpha \cong Y_\alpha$. Then $\prod_{\alpha < \kappa} X_\alpha \cong \prod_{\alpha < \kappa} Y_\alpha$. 

**Prop:** Let $\{X_\alpha \mid \alpha < \kappa\}$ be family of nonempty topological spaces.
- If for each $X_\alpha$ is second countable and $\kappa \le \omega$, then the Tychonoff product $X =\prod_{\alpha < \kappa} X_\alpha$ is second countable.
- If $X =\prod_{\alpha < \kappa} X_\alpha$ is second countable, then $X_\alpha$ is second countable.

**Prop:** Let $X = \prod_{n <\omega}X_n$ be the countable product of separable spaces, then $X$ is separable.

**Prop:** Let $X = \prod_{\alpha < \kappa} X_\alpha$ is first countable iff for each $\alpha < \kappa$, $X_\alpha$ is first countable and $\kappa \le \omega$. 

**Def:** For each $\alpha < \kappa$, there's a function $f_\alpha: X_\alpha \to Y_\alpha$ be a function between topological spaces. We can define the *product function* $\prod_{\alpha < \kappa}f_\alpha$ with domain $\prod_{\alpha < \kappa} X_\alpha$ and codomain $\prod_{\alpha < \kappa} Y_\alpha$, defined by the following way: $$
\left(\pi_\alpha\circ\prod_{\alpha < \kappa} f_\alpha\right)(x) = \left(\prod_{\beta < \kappa} f_\beta\right)(x)(\alpha) = f_\alpha(x_\alpha)
$$for each $\alpha < \kappa$.

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

**Def:** Let $X$ be a topological space and for each $\alpha < \kappa$, there's a function $f_\alpha: X \to Y_\alpha$ where $Y_\alpha$ is a topological space. We define the *diagonal function $\Delta_{\alpha<\kappa} f_\alpha$* with domain $X$ and codomain $\prod_{\alpha < \kappa}Y_\alpha$ defined as follows: $$(\Delta_{\alpha<\kappa} f_\alpha)(x)(\beta) = f_\beta(x).$$
**Prop:** Let $X$ be a topological space and for each $\alpha < \kappa$, there's a function $f_\alpha: X \to Y_\alpha$ where $Y_\alpha$ is a topological space. The diagonal function $\Delta_{\alpha<\kappa} f_\alpha$ has the following properties:
- $\Delta_{\alpha<\kappa} f_\alpha$ is continuous if for each $\alpha < \kappa$, $f_\alpha$ is continuous.
- $\Delta_{\alpha<\kappa} f_\alpha$ is open if for each $\alpha < \kappa$, $f_\alpha$ is open.