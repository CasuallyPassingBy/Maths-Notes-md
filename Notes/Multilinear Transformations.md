---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Bilinear Forms]], [[Space of Linear Transformations]], [[Tensor Product of Modules]], [[Group Actions]], [[Symmetric Group]]

A multilinear map is a function of several variables that is linear separately in each variable. More precisely a multilinear map is a function $$ f:V_1\times \dots \times V_n \to W$$where $V_1, \dots V_n$, and $W$ be vector spaces with the following property: for each $i$, if all the variables but $v_i$ are held constant, then $f(v_1, \dots, v_i, \dots, v_n)$ is a linear function of $v_i$. 

A multilinear map of one variable is a linear map, and of two variables is a bilinear map. More generally, for any nonnegative integer $k$, a multilinear map of $k$ variables is called a $k$-linear map. If the codomain of a multilinear map is the field of scalars, it is called a multilinear form. 

We denote the space of all multilinear transformations: $$\mathcal L(V_1, \dots, V_n;W):= \{f:V_1\times \dots \times V_n \to W\mid F \text{ is } k\text{ multilinear}\}$$
If all $V_1 = \dots = V_n = V$, then we write $$\mathcal L_n(V, W) := \mathcal L(V, \dots, V;W)$$

If we associate each $F \in \mathcal L(V_1, \dots, V_n; W)$ and the function $\tilde F \in \mathcal L(V_1, \mathcal L(V_2, \dots, V_n; W))$ given by $$\tilde (Fv_1)(v_2, \dots, v_n) := F(v_1, v_2, \dots, v_n)$$
We a vector space isomorphism and $$\mathcal L(V_1, \dots, V_n; W) \cong \mathcal L(V_1, \mathcal L(V_2, \dots, V_n;W))$$
If all variables belong to the same space, we can consider special types: symmetric, anti-symmetric and alternating $k$-linear maps. 

# Symmetric and Alternating multilinear maps

We can define how $S_n$ acts on $\mathcal L_n(V, W)$, for $f\in \mathcal L_n(V)$ and $\sigma \in S_n$, then $$\sigma f(v_1, \dots, v_n) := f(v_{\sigma(1)}, \dots, v_{\sigma(n)})$$
We have that is $F \in \mathcal L_n(V, W)$ symmetric iff, any $\sigma \in S_n$ then 
$$\sigma F = F$$

Let $V$ and $W$ be vector fields over a field $F$. A multilinear map of the $f: V^n \to W$ is alternating if it satisfies the following condition:
- if $x_1, \dots, x_n$ are linearly dependent then $f(x_1, \dots, x_n)  = 0$
**Properties:**
- If any component $x_i$ of the alternating multilinear map is replaced by $x_i + cx_j$ for any $j \ne i$ and $c\in F$, then the value of the map is not changed.

- Every alternating multilinear map is anti symmetric, meaning that $$f(\dots, x_i, x_{i+1}, \dots)= - f(\dots, x_{i+1}, x_i, \dots)$$or equivalently $$\sigma f = (\text{sgn }\sigma) f$$
The set of of all symmetric $n$-linear functions from $V$ to $W$ is denoted as $S_n(V;W)$, and for alternating $n$-linear functions from $V$ to $W$ is denoted as $A_n(V;W)$. 
### The Symmetrizing and Alternating Operators

Given any $f\in \mathcal L_n(V; W)$, then there's a way to make a symmetric $k$-linear function $Sf$ from it: $$(Sf) := \sum_{\sigma \in S_n} \sigma f$$
Similarly, we can make an alternating $k$-linear function from $f$, as $$(Af) := \sum_{\sigma \in S_n} (\text{sgn}\sigma) \sigma f$$
If $f \in \mathcal L_n(V; W)$, then:
- $Sf$ is a symmetric $n$-linear map
- $Af$ is an alternating $n$-linear map

If $f$ is an alternating $n$-linear function on a vector space $V$, then $Af = (n!) f$ 
# Relation to tensor products

There is a natural one to one correspondence between multilinear maps: $$ f:V_1\times \dots \times V_n \to W$$ and linear maps $$ F:V_1\otimes \dots \otimes V_n \to W$$where $V_1\otimes \dots \otimes V_n$ denotes the tensor product of $V_1, \dots V_n$. The relation between the functions $f$ and $F$ is given by the formula $$f(v_1, \dots, v_n) = F(v_1\otimes \dots \otimes v_n)$$