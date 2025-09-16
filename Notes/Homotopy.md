---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Continuous Functions and Homeomorphims]]

**Def:** Let $X$ and $Y$ be topological spaces, and let $f, g:X \to Y$ be continuous maps. A *homotopy from $f$ to $g$* is a continuous map $H:X \times I \to Y$ such that for all $x\in X$ $$H(x, 0) = f(x), \qquad H(x, 1) =g(x).$$If there exists a homotopy from $f$ to $g$, we say that $f$ and $g$ are *homotopic*, and write $f \simeq g$, of $H: f\simeq g$ if we want to emphasise the homotopy. If $f$ is homotopic to a constant map, we say it is *null homotopic*.

**Obs:** A homotopy defined a one-parameter family of continuous maps $H_t:X \to Y$, by $H_t(x) := H(x, t)$, such that $H_0 = f$ and $H_1 = g$. 

We think of the parameter $t$ as time, and think of $H$ as giving a ways to deform $f$ into $g$ as $t$ goes from $0$ to $1$. The idea is that a homotopy represents a continuous deformation of one map into another.

**Prop:** For any topological spaces $X$ and $Y$, homotopy is an equivalence relation on the set of all continuous maps from $X$ to $Y$. 

**Prop:** The homotopy relation is preserved by composition: if $f_0, f_1: X \to Y$ and $g_0, g_1:Y \to Z$ are continuous maps with $f_0\simeq f_1$ and $g_0\simeq g_1$, then $g_0 \circ f_0 \simeq g_1 \circ f_1$. 

**Example:** Let $B\subseteq \Bbb R^n$ and let $X$ be a topological space. Suppose $f,g :X \to B$ are any tw continuous maps with the property that for all $x\in X$, the line segment from $f(x)$ to $g(x)$ lies in $B$. We define a homotopy $H: f \simeq g$ by letting $H(x, t) := f(x) + t(g(x)-f(x))$. This is called the *straight-line homotopy between $f$ and $g$*. 