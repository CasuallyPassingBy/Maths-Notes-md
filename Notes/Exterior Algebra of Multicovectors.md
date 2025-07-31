---
tags:
  - DifferentialGeometry
  - LinearAlgebra
---
Subjects: [[Differential Geometry]], [[Linear Algebra]]
Links: [[Dual Vector Spaces]], [[Exterior Algebra]], [[Multilinear Transformations]], [[Tensor Product of Modules]],  [[Graded Ring]], [[Tensor Product of Linear Functions]]
# Tensor Product 

**Def:** Let $f \in \mathcal L_k(V; \Bbb R)$ and $g\in \mathcal L_\ell(V; \Bbb R)$. Their *tensor product* is the $(k+\ell)$-linear function $f\otimes g$ defined by: $$(f\otimes g ) (v_1, \dots, v_{k + \ell}) = f(v_1, \dots, v_k) g(v_{k+1}, \dots,v_{k+\ell}) $$
The tensor product is associative: $$f \otimes (g \otimes h) = (f\otimes g) \otimes h$$
**Prop:** Let $V$ be a vector space of dimension $n$ with basis $e_1, \dots, e_n$. Let $\alpha^1, \dots, \alpha^n$ be the dual basis of $V'$. The basis for the space $\mathcal L_k(V; \Bbb R)$ of $k$-linear functions on $V$ is $\{\alpha^{i_1}\otimes \dots \otimes \alpha^{i_k}\}$ for all multi-indices $(i_1, \dots, i_k)$. 

**Cor:** The $\dim \mathcal L_k(V; \Bbb R) = n^k$. 

# Wedge Product

We are going to drop, the fact that the codomain is $\Bbb R$ for the rest of the note, since this notation is a bit cumbersome. 

If two multilinear forms $f$ and $g$ on a vector space $V$ are alternating, then we would like to have a product that is also alternating as well. This motives the definition of the *wedge product*, also called the *exterior product*, for $f\in A_k(V)$ and $g\in A_\ell(V)$: $$f \wedge g := \frac1{k! \ell !} A(f\otimes g)$$To avoid redundancies of $f\wedge g$ is to stipulate that in the sum, $\sigma(1), \dots, \sigma(k)$ be in ascending order and $\sigma(k+1), \dots, \sigma(k+\ell)$ also be in ascending order. We call a permutation $\sigma \in S_{k + \ell}$ a $(k, \ell)$*-shuffle* if: $$\sigma(1) < \cdots < \sigma(k) \quad \text{and} \quad \sigma(k+1) < \cdots < \sigma(k+\ell)$$We get that: $$f\wedge g = \sum_{\substack{(k, \ell)-\text{shuffles}\\ \sigma \in S_{k+\ell}}} \sigma (f\otimes g)$$
**Prop:** The wedge product is anti-commutative: if $f\in A_k(V)$ and $g\in A_\ell(V)$, then $$f \wedge g = (-1)^{k\ell} g\wedge f$$
**Cor:** If $f$ is a multicovector of odd degree on $V$, then $f\wedge f = 0$.

**Lemma:** Suppose $f$ is a $k$-linear function and $g$ an $\ell$-linear function on a vector space $V$. Then:
- $A(A(f) \otimes g) = k! A(f\otimes g)$
- $A(f\otimes A(g)) = \ell ! A(f\otimes g)$

**Associativity of wedge product:** Let $V$ be a real vector a space and $f, g, h$ alternating multilinear maps on $V$ of degree $k, \ell, m$, respectively. Then $$(f\wedge g) \wedge h= f \wedge (g \wedge h) $$
**Cor:** Under the hypothesis of the proposition: $$f\wedge g \wedge h = \frac1{k!\ell ! m!} A(f\otimes g \otimes h) $$
This corollary easily generalises to an arbitrary number of factors: if $f_i \in A_{d_i}(V)$, then $$f_1 \wedge \dots \wedge f_r = \frac1{(d_1)!\cdots (d_r)!} A(f_1 \otimes \cdots \otimes f_r)$$
**Cor:** For $a, b\in \Bbb R$, $f \in A_k(V)$ and $g\in A_\ell (V; \Bbb R)$, then $af \wedge bg = (ab) f\wedge g$.

**Wedge product of $1$-covectors:** If $\alpha^1, \dots, \alpha^k$ are linear fuctionals on a vector space $V$ and $v_1, \dots, v_k \in V$, then $$(\alpha^1\wedge \cdots \wedge \alpha^k) (v_1, \dots, v_k) = \det[\alpha^i(v_j)]$$
**Cor:** Suppose two sets of covectors of the vector space $\beta^1, \dots, \beta^k$ and $\gamma^1, \dots, \gamma^k$ are related by $$\beta^i = \sum_{j = 1}^k a_j^i \gamma^j$$for a $k\times k$ matrix $A = [a^i_j]$. Then $$\beta^1 \wedge \cdots \wedge \beta^k = (\det A) \gamma^1 \wedge \dots \wedge \gamma^k$$
**Cor:** Let $f$ be a $k$-covector on a vector space $V$. Suppose two sets of vectors $u_1, \dots, u_k$ and $v_1, \dots, v_k$ in $V$ are related by $$u_j = \sum_{i = 1}^k a^ i_j v_i$$for a $k\times k$ matrix $A = [a^i_j]$. Then $$f(u_1, \dots, u_k) = (\det A)f(v_1,\dots, v_k)$$
**Cor:** Let $\alpha^1, \dots, \alpha^k$ be $1$-covectors on space $V$. Then, $\alpha^1 \wedge \dots \wedge \alpha^k$ iff $\alpha^1, \dots, \alpha^k$ are linearly independent in the dual space $V'$. 

**Prop:** Let $\alpha$ be a non-zero $1$-covector and $\gamma$ a $k$-covector on a finite-dimensional vector space $V$. Then $\alpha \wedge \gamma = 0$ iff $\gamma = \alpha \wedge \beta$ for some $(k-1)$-covector $\beta$ on $V$. 

For a finite-dimensional vector space $V$, say dimension $n$, define $$A_* (V) =\bigoplus_{k = 0}^\infty A_k(V) = \bigoplus_{k = 0}^n A_k(V)$$with the wedge product of multicovectors as multiplication, $A_*(V)$ becomes [[Graded Ring|anticommutative graded algebra,]] called the *exterior algebra* or the *Grassman algebra* of multicovectors on the vector space $V$. 
# Basis for $k$-Covectors

Let $e_1, \dots, e_n$ be a basis for a real vector space $V$, let $\alpha^1, \dots, \alpha^n$ be the dual basis for $V'$. We use the [[Multi-index notation|multi-index notation]], let $I = (i_1, \dots, i_k)$ and write $e_I := (e_{i_1}, \dots,e_{i_k})$ and $\alpha^I := \alpha^{i_1}\wedge \cdots \wedge \alpha^{i_k}$. 

A $k$-linear functional $f$ on $V$ is completely determined by its values on all $k$-tuples $(e_{i_1}, \dots, e_{i_k}).$ If $f$ is alternating, then it is completely determined by its values on $(e_{i_1}, \dots, e_{i_k})$ with $1 \le i_1 < \cdots < i_k \le n$; it suffices to consider $e_I$ with $I$ in strictly ascending order.

**Lemma:** Let $e_1, \dots, e_n$ be a basis for a vector space $V$ and let $\alpha^1, \dots, \alpha^n$ be the dual basis in $V'$. If $I =(1 \le i_1 < \cdots < i_k \le n)$ and $J = (1 \le j_1 < \cdots < j_k \le n)$ are strictly ascending multi-indices of length $k$, then $$\alpha^I(e_J) = \delta^I_J = \begin{cases} 1 & I = J \\0 & I \neq J \end{cases}$$
**Prop:** The alternating $k$-linear functions $\alpha^I$, $I = (1 \le i_1 < \cdots < i_k \le n)$, form a basis for the space $A_k(V)$ of alternating $k$-linear functions on $V$.

**Cor:** If the vector space $V$ has dimension $n$, then the vector space $A_k(V)$ of $k$-covectors on $V$ has dimension $n \choose k$.

**Cor:** If $k > \dim V$, then $\dim A_k(V) = 0$. 