---
tags:
  - LinearAlgebra/AffineGeometry
---
Subjects: [[Affine Geometry]]
Links: [[Affine Spaces]], [[Space of Linear Transformations]]

**Def:** Given two affine space $A$ and $B$ whose associated vector space $\overrightarrow{A}$ and $\overrightarrow{B}$, an *affine map* or *affine homomorphism* from $A$ to $B$ is a map $f:A \to B$ such that $\overrightarrow{f}: \overrightarrow{A} \to \overrightarrow{B}$ defined as $\overrightarrow{f}(b-a) := f(b)- f(a)$ is a well defined linear map. By being well defined we mean that $b-a= d-c$ imples that $f(b)-f(a) = f(d)-f(c)$. 

This imples that for a point $a\in A$ and a vector $v\in \overrightarrow A$, we have that $f(a+v) = f(a) + \overrightarrow f(v)$. Therefore, $f$ is completely defined by its value on a single point and the associated linear map $\overrightarrow f$ . 

**Def:** An *affine transformation* or *endomorphism* of an affine space $A$ is an affine map from the space to itself.

**Def:** If $X$ of dimension at least $2$, a *semiaffine transformation* $f$ of $X$ is a bijection from $X$ onto itself that satisfies:
- for every $d$-dimensional affine subspace $S$ of $X$, then $f[S]$ is also a $d$-dimensional affine subspace of $X$.
- If $S$ and $T$ are parallel affine subspaces of $X$, then $f[S]$ and $f[T]$ are parallel.

**Prop:** The composition of affine transformations is an affine transformations. 

**Cor:** The set of all affine transformations of $X$ is a groups and it is called the [[Affine Group|affine group]] and it is denoted as $\text{Aff}(X)$. 

**Example:** Given a vector $v$, the translation map $T_v: A \to A$ defined as $a \mapsto a +v$ for every $a\in A$ is an affine map. 

By fixing a point $c\in X$ one can define a function $m_c :X \to V$ by $m_c(x) = x-c$. For any $c\in X$, this function is bijective, by the properties of being an affine space, and has an inverse $m_c^{-1}:V \to X$ given by $m_c^{-1}(v) = c+v$. Thus functions can be used to turn $X$ into a vector spaces with respect to the point $c$ by defining
- $x +y := m_c^{-1}(m_x(x) + m_c(y))$ for all $x, y\in X$, and
- $rx = m_c^{-1}(rm_c(x))$ for all $r\in F$ and $x\in X$.

For any linear transformation $\lambda$ of $V$, we can define the function $L(c, \lambda): X \to X$ by $$L(c, \lambda) := m_c^{-1}(\lambda(m_c(x))) = c + \lambda(x-c).$$Then $L(c, T)$ is an affine transformation of $X$ which leave the point $c$ fixed. It is a linear transformation of $X$, viewed as a vector space with origin $c$. 

Now, let $\sigma$ be any affine transformation of $X$. Pick a point $c\in X$ and consider the translation of $X$ by the vector $w= \sigma(c)-c$, denoted by $T_w$. There's a unique linear operator $\lambda$ of $V$ such that $$\sigma(x) = T_w(L(c, \lambda)(x)).$$This means that every affine transformation of $X$ is the composition of a linear transformation of $X$ (viewed as a vector space) and a translation of $X$.