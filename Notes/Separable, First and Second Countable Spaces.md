---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Special Sets in Topological Spaces]], [[Dense Subsets]]

**Def:** Let $(X, \tau)$ be a topological space
- $(X, \tau)$ is *separable* if it contains a dense countable set
- The space $(X,\tau)$ is *first countable* if for every $x\in X$ has a countable neighbourhood basis
- The space $(X,\tau)$ is *second countable* if there's a countable base for $\tau$

The properties of *first countable* and *second countable* are known as the first axiom of countability and the second axiom of countability. 

**Prop:** If $X$ is a second countable space and $B$ is any base of $X$, then $B$ contains a countable base of $X$

**Prop:** If $(X, \tau)$ is second countable, then $X$ is also separable and first countable

**Prop:** Let $x$ be a point of the space $(X, \tau)$, and suppose that $x$ have a countable local base of neighbourhoods. Then we can construct a local basis $\{B_1, \dots, B_n, \dots \}$ of $X$ such that $B_{n+1}\subseteq B_n$ 

**Obs:** Every metric space is first countable

**Prop:** Let $(X, \tau_d)$ be a [[Metrizable Spaces|metrizable space]]. If $(X, \tau_d)$ is separable, then $(X, \tau_d)$ is second countable. Meaning, in metrizable spaces separable is equivalent to second countable.

## Image under Continuous Functions

If $(X, \tau)$ is first/second countable space, and $Y$ a subspace of $X$, then $(Y, \tau|_Y)$ is also first/second countable. Meaning countability is hereditary. 

Let $X$ and $Y$ be topological spaces and $f:X \to Y$ be a surjective continuous function. If $D$ is a dense subset of $X$, the $f[D]$ is dense in $Y$. In particular, if $X$ is separable then so is $Y$

Let $X$ be a topological space and ${\cal B}(x)$ be a local base of $x$ on $X$. Let $f:X\to Y$ be a continuous and open function. Then the collection $\{f[B] \mid B\in {\cal B}(x)\}$ is a local base of $f(x) =y$ on $Y$.

The continuous and open image of any first/second countable space is first/second countable. Countability is preserved under continuous and open mappings. 