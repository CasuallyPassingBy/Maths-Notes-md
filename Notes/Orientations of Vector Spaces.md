---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Bases and Dimension]],  [[Differential Geometry]], [[Exterior Algebra]]

**Def:** Let $V$ be a a real vector space of dimension $n \ge 1$. We say that two ordered bases $(E_1,\dots, E_n)$ and $(\widetilde E_1,\dots, \widetilde E_n)$ for $V$ are *consistently oriented* if the transition matrix $(B_ i^j)$, defined by $$E_i = B_i^j \widetilde E_j, $$has positive determinant.

**Obs:** Being consistently oriented is an equivalence relation on the sets of all ordered bases for $V$, and there are exactly two equivalence classes.

**Def:** If $\dim V \ge 1$, we define an *orientation for $V$* as an equivalence class of ordered bases. If $(E_1,\dots, E_n)$ is any ordered basis for $V$, we denote the orientation that it determines by $[E_1,\dots, E_n]$, and the opposite orientation by $- [E_1,\dots, E_n]$. A space together with a choice of orientation is called an *oriented vector space*. If $V$ is oriented, then any ordered basis $(E_1,\dots, E_n)$ that is in the given orientation is said to be *oriented* or *positively oriented*. Any basis that is not in the given orientation is said to be *negatively oriented.*

For the special case of a zero-dimensional vector space $V$, we define an orientation of $V$ to be simply a choice of one of the numbers $\pm 1$.

**Example:** The orientation $[e_1,\dots, e_n]$ of $\Bbb R^n$ determined by the standard basis is called the *standard orientation*. The standard orientation of $\Bbb R^0$ is defined to be $+1$. 

**Prop:** Let $V$ be a vector space of dimension $n$. Each nonzero element $\omega\in {\textstyle \bigwedge}^{\!k}(V^*)$ determines an orientation $\mathcal O_\omega$ of $V$ as follows: if $n \ge 1$, then $\cal O_\omega$ is the set of ordered bases $(E_1,\dots, E_n)$ such that $\omega(E_1,\dots, E_n)> 0$; while if $n =  0$, then $\cal O_\omega$ is $+1$ if $\omega > 0$, and $-1$ if $\omega < 0$. Two nonzero $n$-covectors determine the same orientation iff each is a positive multiple of each other. 

**Def:** If $V$ is an oriented $n$-dimensional vector space and $\omega$ is an $n$-covector that determines the orientation of $V$ as described in the proposition above, we say that $\omega$ is a *positively oriented $n$-covector*. 