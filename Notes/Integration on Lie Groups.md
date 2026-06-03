---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Haar Measure]], [[Integration of Differential Forms on Smooth Manifolds]], [[Lie Groups]], [[Lie Algebra of a Lie Group]], [[Measures on Hausdorff Spaces]], [[Densities on Smooth Manifolds]], [[Orientations of Smooth Manifolds]], [[The Exponential Map on Lie Groups]], [[Normal Lie Subgroups]]

**Def:** Let $G$ be a Lie group. A covariant tensor field $A$ on $G$ is said to be *left-invariant* if $L_g^* A= A$ for all $g\in G$. 

**Prop:** Let $G$ be a compact Lie group endowed with a left-invariant orientation. Then $G$ has a unique positively oriented left-invariant $n$-form $\omega_G$ with the property that $$\int_G \omega_G = 1.$$
The orientation form whose existence is asserted in this proposition is called the *Haar volume form on $G$*. Similarly, the map $f \mapsto \int_G f \omega_G$ is called the *Haar integral.*

We see that every Lie group has a left-invariant top-form form that is uniquely determined up to constant multiple. It is only in the compact case that we can use the volume normalisation to single out a unique one.

Let $n = \dim G$, and choose a non-zero alternating top-form at the identity, $\omega_e\in {\bigwedge}^{\!n}(T_e^*G)$. We define a global left-invariant top-form $\omega$ by setting: $$\omega_g := (\ell_{g^{-1}})^*\omega_e.$$
Let $G$ be given an oriention induced by $\omega$. For any open set $U\subseteq G$, we define a Borel measure $\mu$ via the integration of this form: $$\mu_0(U) := \int_U \omega. $$This is well-defined because every open set $U$ is an open submanifold of $G$.

Let $g\in G$. Since $\ell_g: U \to gU$ is an orientation-preserving diffeomorphism between open submanifolds, the smooth change of variables applies $$\mu_0(gU) = \int_{gU} \omega  = \int_U \ell^*_g \omega = \int_U\omega = \mu_0(U). $$Thus, $\mu_0$ is left-invariant on all open sets. 

Carathéodory's Extension Theorem guarantees a unique extension to an outer measure, which restricts to a true regular measure $\mu$ on the Borel $\sigma$-algebra $\mathcal B(G)$. Because this extension is unique and $\mu_0$ is left-invariant on the generating open sets, the extended Borel measure $\mu$ is left-invariant for all Borel sets $E\in \mathcal B(G)$, satisfying $\mu(gE) = \mu(E)$. 

To show that $\mu$ is locally finite, let $K$ be a compact neighbourhood of $e$. In a local chart $(V, \varphi)$ containing $K$, the form can be expressed smoothly as $\omega = f(x) \, dx^1\wedge\dots\wedge dx^n$. Because $f$ is continuous it is bounded by some constant $M$ on the compact set $\varphi[K]$. Thus $$\mu(K) = \int_{\varphi[K]} f(x)\, dx^1\wedge \dots\wedge dx^n \le M \lambda(\varphi[K]) <\infty. $$
We see that $\mu$ is a Haar measure on $G$. Since any left-invariant top-form is unique up to a real multiplier $c\in \Bbb R^\times$, and any left Haar measure is unique up to a positive multiplier $c\in \Bbb R^+$, we establish a one-to-one correspondence between positively oriented left-Haar volume forms and left-Haar measures. 

**Prop:** Let $G$ be a Lie group. If $\omega$ is a left-invariant top-form, then its pullback under the right-multiplication map $r_g(x) = xg$ satisfies$$r_g^*\omega = \det(\text{Ad}(g^{-1})) \omega$$
**Cor:** If $G$ is a Lie group, its measure-theoretic modular function $\Delta:G \to \Bbb R^+$ is given smoothly by $$\Delta(g) = |\det(\text{Ad}(g^{-1}))|.  $$If in addition, $G$ is connected, then  $$\Delta(g) =\det(\text{Ad}(g^{-1})).   $$
**Cor:** Let $G$ be a connected Lie group. Then $G$ is unimodular iff $$\text{tr}(\text{ad}_X)  =0 \qquad \forall X\in \frak g. $$
**Def:** A Lie algebra $\frak g$ is called perfect if $\mathfrak g = [\mathfrak{g}, \mathfrak{g}]$. 

We see a couple of classes that must be unimodular:
- Compact Lie groups.
- Abelian Lie groups.
- Discrete Lie groups.
- Connected Lie groups that have perfect Lie algebras. 