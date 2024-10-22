---
tags:
  - LinearAlgebra
  - Analysis
---
Subjects: [[Metric and Normed Spaces]], [[Linear Algebra]]
Links: [[Vector Spaces]], [[Normed Spaces]]

**Def:** An inner product on $V$* is a function $\langle \cdot, \cdot\rangle :V \times V\to \mathbb F$, such that

- $\langle v, v \rangle \ge 0$, for all $v \in V$
- $\langle v, v\rangle = 0$ iff $v = 0$
- $\langle u+v, w\rangle = \langle u, w\rangle+ \langle v, w\rangle$, for all $u, v,w \in V$
- $\langle \lambda u, v\rangle$ for all $\lambda \in \mathbb F$ and all $u, v \in V$
- $\langle u, v\rangle = \overline{ \langle v, u\rangle}$

in the context of physics, inner product is defined as $\langle u| v\rangle = \langle v, u\rangle$. Thus is homogeneous on the second entry.

********Def:******** An ********************inner product space******************** is a vector space $V$ along with an inner product on $V$, usually denoted as $(V, \langle \cdot, \cdot\rangle)$

- **Properties of the inner product**
    For each fixed $u \in V$, the function that takes $v$ to $\langle v, u\rangle$ is a linear map from $V$ to $\mathbb F$.
    $\langle 0, u\rangle =0$ for all $u \in V$
    $\langle u, 0\rangle = 0$ for all $u \in V$
    $\langle u, v+w\rangle = \langle u, v\rangle+ \langle u, w\rangle$ for all $u, v,w \in V$
    $\langle u,\lambda v \rangle = \overline \lambda \langle u, v\rangle$ for all $\lambda \in \mathbb F$ and $u, v \in V$
    
**Def**: For $v \in V$, the *******_norm of $v$,_ is denoted as $\|v\|$, and defined as:

$$ \|v\| = \sqrt{\langle v, v\rangle} $$
- Basic Properties of the Norm
    $\|v\| =0$ iff $v = 0$
    $\|\lambda v \| = |\lambda|\|v\|$ for all $\lambda \in \mathbb F$ and $v\in V$
    
### Important Examples of inner products

**********************************************Complex coordinate space**********************************************

For $x,y \in \mathbb C^n$ then it is of the form

$$ \langle x, y\rangle = y^*x $$

**********************************************Real coordinate space**********************************************

For $x,y \in \mathbb R^n$ then it is of the form

$$ \langle x, y\rangle = y^\top x $$

********Def:******** Two vectors $u, v\in V$ are called *************_orthogonal if $\langle u, v\rangle = 0$_

******Th:****** Suppose $u$ and $v$ are orthogonal vectors in $V$. Then

$$ \|u+v\|^2=\|u\|^2+\|v\|^2 $$

******Th:****** Suppose $u, v\in V$, with $v \ne 0$. Set $c = \frac{\langle u, v\rangle}{\|v\|^2}$ and $w = u-cv$. Then

$$ \langle w,v \rangle =0 \text{ and } u=cv+w $$

**************Cauchy-Schwarz Inequality**************

Suppose $u,v \in V$. Then

$$ |\langle u,v \rangle|\le \|u\| \|v\| $$

This inequality iff one of $u$, $v$ us a scalar multiple of the other.

**************************************Trianglele Inequality**************************************

Suppose $u, v\in V$. Then

$$ \| u+v\| \le \|u\|+\|v\| $$

This inequality is an equality iff $u$, $v$ is a nonnegative multiple of each other.

********************************************Parallelogram Equality:******************************************** Suppose $u, v\in V$. Then

$$ \|u+v\|^2+\|u-v\|^2 =2(\|u\|^2+\|v\|^2) $$

**********************************************Polarization Identity**********************************************

Suppose $u, v \in V$. Then

$$ \|u+v\|^2 = \|u\|^2+\|v\|^2+2\operatorname{Re}\langle u, v \rangle $$

Suppose $V$ is real inner product space. Then

$$ \langle u,v \rangle =\frac{\|u+v\|^2-\|u-v\|^2}{4} $$

Suppose $V$ is complex inner product space. Then

$$ \langle u,v \rangle = \frac{\|u+v\|^2 - \|u-v\|^2 + \|u+iv\|^2i - \|u-iv\|^2i}{4} $$

These identities above can be used to define an inner product given a norm, iff they satisfying the parallelogram equality.

Let $S\in \mathcal L(V)$ be injective and $(V, \langle \cdot, \cdot\rangle)$, then we can define a new inner product as $\langle u, v\rangle_* := \langle Su, Sv\rangle$

Suppose $V$is finite dimensional and $\langle \cdot, \cdot\rangle_1$ and $\langle \cdot, \cdot\rangle_2$ are inner products on $V$ with corresponding norms $\|\cdot \|_1$ and $\|\cdot \|_2$. Then there’s a positive number $c$ such that, for all ${v \in V}$

$$ \|v \|_1 \le c \|v \|_2 $$

and the $\langle \cdot, \cdot \rangle = \langle \cdot, \cdot \rangle_1 +\langle \cdot, \cdot \rangle_2$ is also another inner product.

********Def:******** Given a vector space $V$ over a subfield $F$ of $\mathbb C$, a **norm** on $V$ is a function $\|\cdot\|:V \to \Bbb R$ such that:

- $\|u+v\| \le \|u\|+\|v\|$, for all $u, v\in V$
- $\|\lambda v\|=|\lambda|\|v\|$, for all $\lambda \in F$, $v \in V$
- $\| v\| = 0$ iff $v=0$

Given $(V, \|\cdot\|)$ a normed space, then we can define a metric on $V$ such that ${d:V\times V\to \Bbb R}$, where $d(u,v) =\|u-v\|$