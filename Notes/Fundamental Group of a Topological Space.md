---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Homotopy]], [[Path Connectedness]], [[Groups]]

Let $X$ be a topological space. A *path* in $X$ is a continuous map $f: [0, 1] \to X$. The points $p = f(0)$ and $q = f(1)$ are called the *initial point* and *terminal point* of $f$, respectively, and we say that $f$ is a *path from $p$ to $q$*. If a path starts and ends at the same point we call it a *loop*. 

Let $X$ and $Y$ be topological spaces, and $A\subseteq X$ an arbitrary subset. A homotopy $H$ between maps $f, g:X \to Y$ is said to be *stationary on $X$* if $H(x, t) = f(x)$ for all $x\in A$ and $t\in [0, 1]$. If there exists such a homotopy $G$, we say that $f$ and $g$ are *homotopic relative to $A$*, and $H$ is also called a *homotopy relative to $A$*. A requirement, for two maps to be homotopic relative to $A$ is that they must agree on $A$. Sometimes when two maps are homotopic but the homotopy is not assumed to be stationary on any particular subspace, we say they are *free homotopic.* ^0f8fb7

Now suppose $f$ and $g$ are two paths in $X$. A *path homotopy from $f$ to $g$* is homotopy that is stationary on the subset $\{0, 1\} \subseteq [0, 1]$, a homotopy that fixes the endpoints for all time. If there exists a path homotopy between $f$ and $g$, we say that they are *path homotopic*, and write $f\sim g$. 

**Prop:** Let $X$ be a topological space. For any two points $p,q \in X$, path homotopy is an equivalence relation on the set of all paths in $X$ from $p$ to $q$. 

For any path $f\in X$, we denote the path homotopy equivalence class of $f$ by $[f]$, and call it the *path class of $f$.* If $f$ is a loop whose initial and terminal point is $p\in X$, we say that $f$ is *based at $p$*, and we call $p$ the *base point of $f$*. The set of all loops in $X$ based at $p$ is denoted by $\Omega(X, p)$. The *constant loop* $c_p\in \Omega(X, p)$ is the map $c_p \equiv p$. A *null-homotopic loop* is one that is *path-homotopic* to a constant loop.

A *reparametrisation* of a path $f:[0, 1] \to X$ is a path of the form $f\circ \varphi$ for some continuous map $\varphi: [0, 1] \to [0, 1]$ fixing $0$ and $1$. 

**Lemma:** Any reparametrisation of a path $p$ is path-homotopic to $f$.

**Def:** We define the *fundamental group of $X$ based at $p$*, denoted to $\pi_1(X, p)$, to be the set of path classes of loops based at $p$. 

**Def:** Let $f, g: [0, 1] \to X$ be paths. We say that $f$ and $g$ are *composable paths* if $f(1) = g(0)$. If $f$ and $g$ are composable, we define their product $f \cdot g : [0, 1] \to X$ by $$f \cdot g (s) := \begin{cases}f(2s) & 0\le s \le 1/2, \\ g(2s-1) & 1/2 \le s \le 1.\end{cases} $$The condition $f(1) = g(0)$ guarantees that $f\cdot g$.

**Homotopy Invariance of Path Multiplication:** The operation of path multiplication is well defined on path classes. More precisely, if $f_0 \sim f_1$ and $g_0 \sim g_1$, and if $f_0$ and $g_0$ are composable, then $f_1$ and $g_1$ are composable and $f_0 \cdot g_0 \sim f_1 \cdot g_1$. 

**Def:** We define the *product of path classes* by setting $[f] \cdot [g] := [f \cdot g]$ whenever $f$ and $g$ are composable. In particular, it is always defiened for $[f], [g] \in \pi_1(X, p)$. 

**Def:** For any path $f$, we define the *reverse path $\bar f$* by $\bar f(s) ;= f(1-s)$; this just retraces $f$ from its terminal point to its initial point.

**Prop:** Let $f,g: [0, 1] \to X$ be two paths from $p$ to $q$. We see that $f\sim g$ iff $f \cdot \bar g \sim c_p$. 

**Properties of Path Class Product:** Let $f$ by any path from $p$ to $q$ in a space $X$, and let $g$ and $h$ be any paths in $X$. Path multiplication satisfies the following properties:
- $[c_p] \cdot [f] = [f] \cdot [c_q] = f$.
- $[f] \cdot [\bar f] = [c_p]$, and $[\bar f] \cdot [f] = [c_q]$.
- $[f] \cdot( [g] \cdot [h]) = ([f] \cdot [g]) \cdot [h]$ whenever either side is defined.

**Cor:** For any space $X$ and any point $p\in X$, $\pi_1(X, p)$ is a group.

**Change of Base Point:** Suppose $X$ is path-connected, $p, q \in X$, and $g$ is any path from $p$ to $q$. Then map $\Phi_g: \pi(X, p) \to \pi_1(X, q)$ defined by $$\Phi_g([f]) := [\bar g] \cdot [f] \cdot [g]$$is an isomorphism, whose inverse is $\Phi_{\bar g}$.

When $X$ is path-connected we sometimes use the imprecise notation $\pi_1(X)$ to refer to the fundamental group of $X$ with respect to an unspecified base point, if the base point is irrelevant. 

**Def:** If $X$ is path connected, we say that $\pi_1(X)$ is *trivial* if $\pi_1(X, p) = \{[c_p]\}$ for each $p\in X$. We say that $X$ is *simply connected*, if $\pi_1(X)$ is trivial.

**Prop:** $X$ is simply connected iff any two paths in $X$ with the same initial and terminal points are path-homotopic.

**Obs:** We see that every convex set in $\Bbb R^n$ is simply connected, and, in particular, $\Bbb R^n$ is simply connected.

**Prop:** Let $X$ be a path-connected topological space, and let $p, q\in X$. If all paths from $p$ to $q$ give the same isomorphism of $\pi_1(X, p)$ with $\pi_1(X, q)$ iff $\pi_1(X, p)$ is abelian.

## Circle Representatives

Let us consider $\Bbb S^1$ as a subset of the complex plane. Let $\omega: [0, 1] \to \Bbb S^1$ denote the loop given by $\omega(s) := \exp(2\pi i s)$. This loop travels once around the circle and maps $0$ and $1$ to the base point $1\in \Bbb S^1$. We see that it is a quotient map. If $f:[0, 1] \to X$ is any loop in space $X$, it passes to the quotient to give a unique map $\tilde f: \Bbb S^1 \to X$ such that $\tilde f \circ \omega = f$, or that this diagram commutes: 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[sep = .5 cm]
[0,1]\arrow[d, two heads, "\omega"'] \arrow[dr, "f"] \\
\mathbb{S}^1 \arrow[r, "\tilde f"'] & X
\end{tikzcd}
\end{document}
```
We call $\tilde f$ the *circle representative of $f$*. Conversely, any continuous map $\tilde f$ from the circle fo  $X$ is the circle representative of the map $f = \tilde f \circ \omega$. 

**Prop:** Let $X$ be a topological space. Suppose $f: I \to X$ is a loops based at $p\in X$, and $\tilde f : \Bbb S^1 \to X$ is circle representative. The following statements are equivalent.
- $f$ is a null-homotopic loop.
- $\tilde f$ is freely homotopic to a constant map.
- $\tilde f$ extends to a continuous map from the closed disk into $X$.

**Square Lemma:** Let $F: [0, 1] \times [0,  1] \to X$ be a continuous map, and let $f, g, h$, and $k$ be paths in $X$ defined by $$\begin{align*}
f(s)  & := F(s , 0) \\
g(s)  & := F(1 , s) \\
h(s)  & := F(0 , s) \\
k(s)  & := F(s , 1) \\
\end{align*} $$Then $f \cdot g \sim h \cdot k$. 

**Prop:** For any path connected space $X$ and any base point $X$, there's a bijection between the set of conjugacy classes of elements of $\pi_1(X, p)$ and $[\Bbb S^1, X]$. 

# Fundamental Group in Manifolds

**Lemma:** Suppose $M$ is a manifold of dimension $n \ge 2$. If $f$ is a path in $M$ from $p_1$ to $p_2$ and $q$ is any point in $M \setminus \{p_1, p_2\}$, then $f$ is path-homotopic to a path that does not pass through $q$. 

The proof of this lemma depends on the [[Compactness in Metric Spaces#Lebesgue Number Lemma|Lebesgue Number Lemma]]. 

**Th:** For $n \ge 2$, $\Bbb S^2$ is simply connected.

**Th:** The fundamental group of a manifold is countable.

# Homomorphisms Induced by Continuous Maps

**Prop:** The path homotopy relation is preserved by composition with continuous maps. That is, if $f_0, f_1: [0, 1] \to X$ are path homotopic and $\varphi:X \to Y$ is continuous, then $\varphi \circ f_0$ and $\varphi \circ f_1$ are path homotopic.

**Def:** Let $\varphi: X \to Y$ be a continuous map. $\varphi$ induces a well-defined map $\varphi_*: \pi_1(X, p) \to \pi_1(Y, \varphi(p))$ be setting $\varphi_*([f]) = [\varphi \circ f]$.

**Prop:** For any continuous map $\varphi$, $\varphi_*$ is a group homomorphism.

The homomorphism $\varphi_*: \pi_1(X, p) \to \pi_1(Y, \varphi(p))$ is called the *homomorphism induced by $\varphi$*

**Properties of the Induced Homomorphism:** 
- If $\varphi:X \to Y$ and $\psi:Y \to Z$ are continuous maps $(\psi \circ \varphi)_* = \psi_* \circ \varphi_*$. 
- If $\text{Id}_X: X \to X$ denotes the identity map of $X$, then for any $p\in X$, $(\text{Id}_X)_*$ is the identity map of $\pi_1(X, p)$. 

**Topological Invariance of $\pi_1$:** Homeomorphic spaces have isomorphic funfamental groups. Specifically, if $\varphi: X \to Y$ is a homeomorphism, then $\varphi_*:\pi_1(X, p) \to \pi_1(Y, \varphi(p))$ is an isomorphism.

We see that $\pi_1: \mathsf{Top}_*\to \mathsf{Grp}$ assigns to each pointed topological space $(X, p)$ its fundamental group based at $p$, and to each pointed continuous map its induced homomorphism. We see that *fundamental group functor $\pi_1$* is [[Categories and Functors#^66a925|covariant]].

**Prop:** Suppose $A$ is a [[Topological Subspaces#Retractions|retract]] of $X$. If $r:X \to A$ is any retraction, then for any $p\in A$, $(\iota_A)_*: \pi_1(A, p) \to \pi_1(X, p)$ is injective and $r_*: \pi_1(X, p) \to \pi_1(A, p)$ is surjective. 

**Cor:** A retract of a simply connected space is simply connected.

**Prop:** Let $X$ be a homogeneous space and $x\in X$, then $\pi_1(X, x)$ is indepentent of choice of base point.

**Prop:** Let $G$ be a topological group. $\pi_1(G, g)$ is abelian. 

### Fundamental Groups of Product Spaces

Let $\{X_\alpha \mid \alpha < \kappa\}$ is a family of topological spaces, and let $p_\alpha: \prod_\beta X_\beta \to X_\alpha$ denote projection on the $\alpha$th factor. Choosing base points $\x_\alpha \in X_\alpha, we get the maps $$(p_\alpha)_*: \pi_1\left(\prod_{\alpha <\kappa} X_\alpha, f\right) \to \pi_1(X_\alpha, x_\alpha),$$where $f\in \prod_\alpha X_\alpha$ and $f(\alpha) = x_\alpha$ for all $\alpha< \kappa$. With this maps together define the map $$P: \pi_1\left(\prod_{\alpha <\kappa} X_\alpha, f\right) \to \prod_{\alpha < \kappa} \pi_1(X_\alpha, x_\alpha)$$by $$P([g])(\alpha) =(p_\alpha)_*([g])$$for all $\alpha < \kappa$. 

**Prop:** If $\{X_\alpha \mid \alpha< \kappa\}$ are any topological spaces, the map $P$ defined above is an isomorphism. 