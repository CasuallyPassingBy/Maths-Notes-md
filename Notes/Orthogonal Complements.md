---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Dual Spaces]], [[Inner Products and Norms]], [[Orthogonal Bases#Riesz Representation Theorem|Riesz Representation Theorem]]
If $U$ is a subset of $V$, then the _****orthogonal complement****_ of $U$, denoted $U^\bot$, is the set of all vectors of all vectors $V$ that are orthogonal to every vector in $U$

$$ U^\bot := \{v \in V \mid \forall u \in U[\langle v, u \rangle = 0]\} $$

- ****Properties****
    
    If $U$ is a subset of $V$, then $U^\bot$ is a subspace of $V$
    
    $\{0\}^\bot = V$
    
    $V^\bot = \{0\}$
    
    If $U$ is a subset of $V$, then $U \cap U^\bot \subseteq \{0\}$
    
    If $U$ and $W$ are subsets of $V$ and $U \subseteq W$, then $W ^\bot\subseteq U^\bot$
    

If $U$ is a finite dimensional subspace of $V$, then

$$ V = U \oplus U^\bot $$

If $V$is finite dimensional and $U$ is a subspace of $V$. Then

$$ \dim U^\bot = \dim V - \dim U $$

Suppose $U$ is finite dimensional subspace of $V$. Then

$$ U = (U^\bot)^\bot $$