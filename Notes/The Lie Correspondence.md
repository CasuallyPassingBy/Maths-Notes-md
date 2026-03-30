---
tags:
  - DifferentialGeometry
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Lie Groups]], [[Lie Algebra of a Lie Group]], [[Infinitesimal Generators of Lie Group Actions]], [[The Exponential Map on Lie Groups]]

**Prop:** Suppose $G$ is a connected Lie group, $H$ is any Lie group, and $\Phi, \Psi: G \to H$ are Lue group homomorphisms such that $\Phi_* = \Psi_*: \text{Lie}(G) \to \text{Lie}(H)$. Then $\Phi = \Psi$. 

**Th:** Suppose $G$ and $H$ are Lie groups with $G$ simply connected, then let $\frak g$ and $\frak h$ be their Lie algebras. For any Lie algebra homomorphism $\varphi: \frak g \to h$, there is a unique Lie group homomorphism $\Phi: G\to H$ such that $\Phi_* = \varphi$. 

**Cor:** If $G$ and $H$ are simply connected Lie groups with isomorphic Lie algebras, then $G$ and $H$ are isomorphic. 

**The Lie Correspondence:** There is a a one-to-one correspondence between isomorphism classes of finite-dimensional Lie algebras and isomorphisms classes of simply connected Lie groups, given by associating each simply connected Lie group with its Lie algebra. 

# Lie's Fundamental Theorems

**Def:** A *local Lie group* is defined to be an open subset $U$ in some finite-dimensional real vector space $V$, together with an element $e\in U$ and smooth maps $m: U \times U \to V$ and $i: U \to V$, satisfying the following identities for all $g, h, k$ sufficiently close to $e$ that both sides are defined:
- $m(g, m(h, k)) = m(m(g, h), k)$;
- $m(e, g) = g = m(g, e)$;
- $m(i(g), g) = e = m(g, i(g))$.

The left translation map $L_g: U \to V$ is defined just as for ordinary Lie groups, and a vector field $X\in {\frak X}(U)$ is said to be *left-invariant* if $d(L_g)_{g'}(X_{g'}) = X_{m(g, g')}$ for all $g, g'\in U$ such that $m(g, g')\in U$. Two local Lie groups $(U, e, m, i)$ and $(U', e', m', i')$ are said to be *locally isomorphic* if there is a diffeomorphism from a neighbourhood of $e$ in $U$ to a neighbourhood of $e'$ in $U'$ that takes $e$ to $e'$, $m$ to $m'$, and $i$ to $i'$. whenever the respective operations are defined. A *local (left or right) action of a local Lie group* on a n open subset $W\subseteq \Bbb R^n$ is defined like an ordinary action except that $g\cdot x$, or $x\cdot g$, is requiered to be defined only for $(g, x)$ in a neighbourhood of $\{e\}\times W$in $U\times W$. A coordinate neighbourhood of the identity in any Lie group is a local Lie group, and any smooth action of a Lie group on smooth manifold restricts to a local action on any sufficiently small coordinate neighbourhood. 

**The Fundamental Theorems of Sophus Lie:**
- *First Fundamental Theorem:* The set of let-invariant vector fields on a local Lie group is a finite-dimensional Lie algebra under Lie bracket, and two local Lie groups with isomorphic Lie algebras are locally isomorphic.
- *Second Fundamental Theorem:* Given an open subset $W\subseteq \Bbb R^n$, there is a one-to-one correspondence between smooth right actions of a local Lie groups on $W$ and finite-dimensional Lie algebras of ${\frak X}(W)$.
- *Third Fundamental Theorem:* Given any finite-dimensional abstract Lie algebra $\frak g$, there exists a local Lie group whose algebra of left-invariant vector fields is isomorphic to $\frak g$.

