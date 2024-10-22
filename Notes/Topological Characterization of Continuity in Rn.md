---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Continuity on R]], [[Compact Sets in Rn]], [[Connected Sets in Rn]]

A function $f: D\subseteq\Bbb R^n\to \Bbb R^m$ is continuous iff for each open subset $V$ of $\Bbb R^m$ the inverse image:

$$ f^{-1}[V] =\{x \in D \mid f(x) \in V\} $$

is open in $D$.

********Def:******** A function $f:S\subseteq\Bbb R^n\to \Bbb R^m$ is ********_uniformly continuous on $S$_ iff

$$ \forall \varepsilon >0\exists \delta >0\forall x,y \in S[\|{x-y}\|<\delta\implies \|f(x) -f(y)\| < \varepsilon] $$
This is an extension of the notion of uniform [[Uniform Continuity on R|contuinuity on R]]

********Th:******** Let $f:K \subseteq\Bbb R^n\to\Bbb R^m$ be a continuous function on a compact domain $K$, then

- $f$ is uniformly continuous on $K$
- The image $f[K]$ is compact on $\Bbb R^n$

**********Cor:********** Let $f:K\subseteq\Bbb R^n\to \Bbb R$, where $K$ is compact, then $f$ attains finite maximum and minimun values.

********Th:******** Let $f:K\subseteq\Bbb R^n\to \Bbb R^m$ be a injective function defined on a compact domain $K$. The inverse function $f^{-1}: f[K]\to \Bbb R^n$ is continuous.

********Th:******** Let $f: A \subseteq \Bbb R^m\to \Bbb R^n$ be uniformly continuous on $A$, then there’s a unique extension of $f$ into $\operatorname{cl}(A)$, that is also uniformly continuous.

**********Th:********** Let $f:A\subseteq \Bbb R^n \to \Bbb R^m$ is continuous and $B\subseteq A$. If $B$ is connected then $f[B]$ is connected.

### **Uniform Extension Theorem**
Let $f:A\subseteq \Bbb R^n \to \Bbb R^m$, be uniformly continuous, then we can extend $f$ to $\text{cl}(A)$, with a function $f^*:\text{cl}(A) \to \Bbb R$ such that $f^*|_A = f$ and $f^*$ is uniformly continuous, additionally, this function is unique, making this the unique extension of $f$