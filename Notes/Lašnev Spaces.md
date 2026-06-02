---
tags:
  - Topology
aliases:
  - Lasnev Spaces
---
Subjects: [[Topology]]
Links: [[Metrizable Spaces]], [[Metrization Theorems]], [[Continuous Functions and Homeomorphims]], [[Perfect Spaces]], [[Topological Networks]]

**Def:** A topological space $X$ is a *Lašnev space* if there's a metrizable space $M$ and a closed, continuous and surjective function $f:M \to X$. 

**Th:** By the [[Metrization Theorems#^fdd00b|Hanai-Morita-Stone Theorem]] a Lašnev space is metrizable iff it is first countable.

We know that Lašnev space is $T_6$, [[Fréchet-Urysohn Spaces|Fréchet-Urysohn space]], and [[Paracompacteness|paracompact]].

**Prop:** Every Lašnev is a $\sigma$-space. 

**Lašnev Theorem:** If $X$ is a Lašnev space, then $X$ can be decomposed $X = M \cup \bigcup_{n < \omega} X_n$, where $f^{-1}\{x\}$ is compact for each $x\in M$, and $X_n$ is a discrete closed subspace of $X$ for $n <\omega.$

**Obs:** The product of two Lašnev space may not even be Fréchet-Urysohn. 

**Obs:** Let $C$ be a convergence sequence along with the limit point. We consider $C$ as a subspace of the real line. The sequential fan $S(\omega)$ is the quotient space obtained by the topological sum of countably many and infinitely many copies of $C$ with the limits points identified as one point called $\infty$. The convergent sequence $C$, is a compact metric space, in particular, it is a Fréchet-Urysohn space. The sequential fan $S(\omega)$, being a closed image of a metric space, is a Lašnev space. It is well known that $C\times S(\omega)$ is not a Fréchet-Urysohn space. We do this by finding a subspace that is homeomorphic to the Arens' space. Thus the product of a Lašnev space with a compact metric space is not even ensured to be Lašnev. 

**Prop:** An arbitrary subset of a Lašnev space is also Lašnev. 

**Example:** There exists a countable Lašnev space $X$ such that $\mathcal K\langle X\rangle$ is not Lašnev.

**Lemma:** Let $f:X\to Y$ be a closed map with $X$ a metric space. Then every compact set of $Y$ is the image of some compact set of $X$. 