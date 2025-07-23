---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Topological Spaces]], [[Bases, Subbases, and Local Basis for Topological Spaces]], [[Initial Topology]], [[Continuous Functions and Homeomorphims]], [[Separation Axioms]]

Given a topological space $(X, \tau)$, and $Y \subseteq X$, we can define the set
$$
\tau|Y = \tau_Y = \tau|_Y = \{ A \cap Y \mid A  \in \tau\} 
$$
We can see that $\tau|_Y$ is a topology on $Y$, and we call it the relative topology of $Y$ with respect to $(X, \tau)$, and say that $(Y, \tau|_Y)$ is a subspace of $(X, \tau)$. 

[[Topology on Metric Spaces#Topology of Submetric Spaces|Submetric Spaces]] are just the topological subspace of a metric space. 

Let $(X, \tau)$ is a topological space, $Y\subseteq X$ and $y \in Y$.
- If $\cal B$ is a basis (subbase) for $\tau$, then ${\cal B}_Y =\{B \cap Y \mid B \in {\cal B}\}$ is a basis (subbase) for $\tau|_Y$ 
- If ${\cal B}(y)$ is a local basis of $y$ for $\tau$, then $\{B \cap Y \mid B \in {\cal B}(y)\}$ is a local basis of $y$ in $(Y, \tau|_Y)$.  

**Def:** Let $X$ be a topological space, and $Y\subseteq X$. We say that $Y$ is a *discrete subset of $X$* if the topology inherited from $X$ is the discrete topology. 

**Prop:** Let $X$ be a topological space and $M$ be a subspace of $X$. The set $A \subseteq M$ is closed in $M$ iff $A = M \cap F$, where $F$ is closed in $X$. The closure $\text{cl}_M (A)$ if a set $A\subseteq M$ in the subspace and the closure $\text{cl}_X(A)$ are related by the equality $\text{cl}_M (A) = \text{cl}_X(A) \cap M$.

**Prop:** If $X$ is a subspace of a space $X$, and $L$ is a subset of $M$, then the two topologies defined on $L$, namely, the topology of a subspace of $M$ and the topology of a subspace of $X$, coincide. 

**Def:** We say that a subspace $M$ of $X$ is closed/open/dense if it is a closed/open/dense subset of $X$.

**Prop:** A subspace $M$ of $X$ is a open/closed subspace, then a set $A\subseteq M$ is open/closed in $M$ iff $A$ is open/closed in $X$. 

**Prop:** A subspace $M$ of $X$ is a cozero subspace, then a set $A\subseteq M$ iscozero in $M$ iff $A$ is cozero in $X$. 

**Obs:** The intersection of a cozero (zero) set in a topological space $X$ with a subspace $M$ of $X$ is a cozero (zero) set in $M$.

**Def:** For every topological space $X$ and any subspace $M$ of $X$, the function $i: M \to X$ defined as $i(x) = x$, is called the *embedding of the subspace $M$ in the space $X$*

**Obs:** The subspace topology coincides with the initial topology induced by the embedding from the subspace to the total space. Meaning that we also have this property: Let $X$ and $Y$ be topological spaces, and $M \subseteq X$. A function $f: Y \to M$ is continuous iff $f' = i \circ M$ is continuous, i.e., the diagram commutes: 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}
Y \arrow[dr,"f' "'] \arrow[r, "f"] & (X, \,_f \tau) \arrow[d,hook, "i"] \\ 
& X
\end{tikzcd}
\end{document}
```

The embedding $i: M \to X$ is open/closed iff $M$ is open/closed. 

For any continuous mapping $f: X \to Y$ and a subspace $M$ of $X$, the composition $f \circ i: M \to X$ us a continuous mapping; it is called the *restriction of $f$ to $M$* and is denoted as $f|_M$. 

**Prop:** Let $f: X \to Y$ and $g: Y \to X$ be maps between topological spaces. if $g \circ f$ is a closed/open, then the restriction $g|_{f[X]}: f[X] \to Z$ is closed/open.

**Def:** Let $f:X \to Y$ be a function between topological spaces, and $L$ a subspace of $Y$, the *restriction of $f$ to $L$* is defined as the mapping of the subspace $f^{-1}[L] \subseteq X$ to the subspace $L \subseteq Y$, that assigns $f(x) \in L$ to $x\in f^{-1}[L]$; this restriction is denoted by $f_L$.

**Prop:** If $f: X\to Y$ is a closed/open mapping for any subspace $L\subseteq Y$ the restriction $f_L: f^{-1}[L] \to L$ is closed/open.

**Def:** A mapping $f: X \to Y$ is called a *homeomorphic embedding* if it a composition of a homeomorphism and an embedding,i.e., if there exists a subspace $L \subseteq Y$ and a homeomorphism $f' : X \to L$ such that $f = i\circ f'$. If for a space $X$ there exists a homeomorphic embedding $f: X \to Y$ in a space $Y$, we say that $X$ is *embeddable* in $Y$. 

**Obs:** The restriction of a homeomorphic embedding is also a homeomorphic embedding.

**Def:** We say that a topological property $P$ is *hereditary (hereditary with respect to closed/open sets)* if for any space $X$ that has the property $P$, every subspace (closed/open subspace) of $X$ has the property $P$. If the property $P$ is not hereditary property but every subspace of a space $X$ has $P$, then we say that $X$ has $P$ *hereditarily*. ^1310cb

**Prop:**
- $T_i$ for $i \le 3\frac12$ are hereditary properties.
- $T_4$ is hereditary with respect to closed sets.
- Perfect normality and $T_6$ is a hereditary property.

**Prop:** If $\{U_\alpha : \alpha < \kappa\}$ is an open cover of a space $X$ and $\{f_\alpha: U_\alpha \to Y\mid \alpha < \kappa\}$ a family of compatible continuous functions, then the combination $\bigcup_{\alpha < \kappa} f_\alpha: X \to Y$ is a continuous function.

**Prop:** If $\{F_\alpha: \alpha < \kappa\}$ is a locally finite closed cover of a space $X$ and $\{f_\alpha: F_\alpha \to Y\mid \alpha < \kappa\}$ a family of compatible continuous functions, then the combination $\bigcup_{\alpha < \kappa} f_\alpha: X \to Y$ is a continuous function.

**Prop:** Suppose we are given a topological space $X$, a cover $\{A_\alpha : \alpha < \kappa\}$ of the space $X$ and a family $\{f_\alpha: A_\alpha \to Y\}$ of a compatible functions, such that the combination $f = \bigcup_{\alpha < \kappa} f_\alpha: X \to Y$ is continuous. If all mappings $f_\alpha$ are open (closed an the family $\{f_\alpha[A_\alpha] : \alpha < \kappa\}$ is locally finite), then the combination $f$ is open (closed).