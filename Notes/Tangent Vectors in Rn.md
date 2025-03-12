---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Differentiablity of Real valued functions of Rn#Directional Derivatives|Directional Derirvatives on Rn]], [[Derivations]], [[Lie Algebra]]

We visualise the tangent space $T_p(\Bbb R^n)$ at $p$ in $\Bbb R^n$ as the vector space of all arrows emanating from $p$. To distinguish the between points and vectors, I am going to use the notation $p = (p^1, \dots, p^n)$ for points and $v = \langle v^1, \dots, v^n\rangle$ or as $$v = \begin{bmatrix}v^1 \\ \vdots \\ v^n\end{bmatrix} $$
We usually denote the standard basis for $\Bbb R^n$ or $T_p(\Bbb R^n)$ by $e_1, \dots, e_n$. Then $v = \sum v^i e_i$ for some $v^i \in \Bbb R$. The elements of $T_p(\Bbb R^n)$ are called *tangent vectors* (or simply *vectors*) at $p$ in $\Bbb R^n$.

Let $p \in \Bbb R^n$. As long as two functions agree on some neighbourhood of a point $p$, they will have the same directional derivatives at $p$. This suggests we can introduce an equivalence relation on the $\mathcal C^\infty$ functions defined on some neighbourhood of $p$. 

Consider the set of all pairs $(f, U)$, where $U$ is a neighbourhood of $p$ and $f\in \mathcal C^\infty(U)$. We say that $(f, U)$ is *equivalent* to $(g, V)$ if there is an open set $p\in W \subseteq U \cap V$  such that $f= g$ restricted to $W$. 

This is an equivalence relation. The equivalence class of $(f, U)$ is called the *germ* of $f$ at $p$. We write $\mathcal C^\infty_p$ or $\mathcal C^\infty_p(\Bbb R^n)$ for the set of all germs of $\mathcal C^\infty$ functions on $\Bbb R^n$ at $p$. 

We have that $\mathcal C_p^\infty$ is an algebra over $\Bbb R$. 

## Derivations

**Def:** Any linear map $D: \mathcal C_p^\infty \to \Bbb R$ that satisfies: $$D(fg) = (Df) g + f (Dg)$$ called the *Leibniz rule*, is called a *derivation at $p$* or a *point-derivation* of $\mathcal C^\infty_p$. We denote the set of all derivations at $p$ by $\mathcal D_p(\Bbb R^n)$. We see that $\mathcal D_p(\Bbb R^n)$ is a Lie algebra. 

**Lemma:** If $D$ is a point-derivation of $\mathcal C^\infty_p$, then $D(c) = 0$ for any constant function.

**Th:** The linear map $\varphi: T_p (\Bbb R^n) \to \mathcal D_p(\Bbb R^n)$ defined as $$v \mapsto  D_v = \sum v^i  \left.\frac{\partial}{\partial x^i}\right\rvert_p$$is an isomorphism of vector spaces. 

We see that under the vector space isomorphism $T_p(\Bbb R^n) \cong \mathcal D_p(\Bbb R^n)$, the standard basis $e_1, \dots, e_n$ for $T_p(\Bbb R^n)$ correspond to the set $\left.\dfrac{\partial}{\partial x^1}\right\rvert_p, \cdots, \left.\dfrac{\partial}{\partial x^n}\right\rvert_p$ of the partial derivatives. From now on, we will make this identification and write a tangent vector $v = \sum v^i e_i$ as $$v = \sum v^i \left.\frac{\partial}{\partial x^i}\right\rvert_p$$
The vector space $\mathcal D_p(\Bbb R^n)$ of derivations at $p$ is more suitable for generalisation to manifolds. 