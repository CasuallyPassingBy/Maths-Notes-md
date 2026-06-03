---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Line Integral over a Vector Field]], [[Vector Surface Integral]], [[Riemann Integral in Rn]], [[Orientations of Smooth Manifolds]], [[Change of Variable Theorem in Rn]], [[Smooth Partitions of Unity for Manifolds]], [[Differential Forms on Smooth Manifolds]]

Recall that a *domain of integration in $\Bbb R^n$* is a bounded subset whose boundary has measure zero.

**Def:** Let $D\subseteq \Bbb R$ be a domain of integration, and let $\omega$ be a continuous $n$-form on $\overline D$. Any such form can be written as $\omega = f\; dx^1\wedge \dots \wedge dx^n$ for some continuous function $f: \overline D \to \Bbb R$. We define the *integral of $\omega$ over $D$* to be $$\int_D \omega := \int_D f.$$This can be written more suggestively as $$\int_D f \; dx^1 \wedge \dots \wedge dx^n := \int_D f\; dx^1\cdots dx^n.$$
Somewhat more generally, let $U$ be an open subset of $\Bbb R^n$ or $\Bbb H^n$, and suppose $\omega$ is compactly supported $n$-form on $U$. We define $$\int_U \omega = \int_D \omega,$$where $D\subseteq\Bbb R^n$ or $\Bbb H^n$ is any domain of integration containing $\text{supp }\omega$, and $\omega$ is extended to be zero on the complement of its support. 

**Prop:** Suppose $D$ and $E$ are open domain of integration in $\Bbb R^n$ or $\Bbb H^n$, and $G: \overline D \to \overline E$ is a smooth map that restricts to an orientation-preserving or orientation-reversing diffeomorphism from $D$ to $E$. If $\omega$ is an $n$-form on $\overline E$, then $$\int_D G^* \omega = \begin{dcases}\int_E \omega & \text{if }G \text{ is orientation-preserving,} \\ -\int_E \omega & \text{if }G\text{ is orientation-reversing.}\end{dcases} $$

**Lemma:** Suppose $U$ is an open subset of $\Bbb R^n$ or $\Bbb H^n$, and $K$ is a compact subset of $U$. Then there is a domain of integration $K\subseteq D \subseteq \overline D\subseteq U$. 

**Prop:** Suppose $U$, $V$ are open subsets of $\Bbb R^n$ or $\Bbb H^n$, and $G: U \to V$ is an orientation-preserving or orientation-reversing diffeomorphism. If $\omega$ is a compactly supported $n$-form on $V$, then  $$\int_V \omega = \pm \int_U G^*\omega,$$with the positive sign if $G$ is orientation-preserving, and the negative sign otherwise.

# Integration on Manifolds

**Def:** Let $M$ be an oriented smooth $n$-manifold with or without boundary, and let $\omega$ be an $n$-form on $M$. Suppose first that $\omega$ is compactly supported in a domain of a single smooth chart $(U,\varphi)$ that is either positively or negatively oriented. We define the *integral of $\omega$ over $M$* to be $$\int_M \omega =: \pm \int_{\varphi[U]} \left(\varphi^{-1}\right)^* \omega,  $$with the positive sign for positively oriented chart, and the negative sign otherwise. 

**Prop:** With $\omega$ as above, $\int_M\omega$ does not depend on the choice of smooth chart whose domain contains $\text{supp }\omega$. 

To integrate over an entire manifold, we combine this definition with a partition of unity. 

**Def:** Suppose $M$ is an oriented smooth $n$-manifold with or without boundary, and $\omega$ is a compactly supported $n$-form on $M$. Let $\{U_i\}$ be a finite open cover of $\text{supp }\omega$ by domains of positively or negatively oriented smooth charts and let $\{\psi_i\}$ be the subordinates smooth partition of unity. Define the *integral of $\omega$ over $M$* to be $$\int_M \omega := \sum_{i} \int_M \psi_i \omega. $$
**Prop:** The definition of $\int_M \omega$ given above doesn't depend on the choice of open cover or partition of unity.

Just we have for orientations, we have a special definition in the zero-dimensional case.

**Def:** The integral of a compactly supported $0$-form $f$ over an oriented $0$-manifold $M$ is to be defined to be the sum $$\int_M f := \sum_{p\in M}\pm f(p), $$where we take the positive sign where the orientation is positive sign and the negative sign at points where it is negative.

**Def:** If $S\subseteq M$ is an oriented immersed $k$-dimensional submanifold with or without boundary, and $\omega$ is a $k$-form on $M$ whose restriction to $S$ is compactly supported we interpret $\int_S \omega$ to mean $\int_S \iota_S^*\omega$, where $\iota_S: S\hookrightarrow M$ is inclusion. In particular, if $M$ is a compact, oriented, smooth $n$-manifold with boundary and $\omega$ is an $(n-1)$-form on $M$, we can interpret $\int_{\partial M}\omega$ unambiguously as the integral of $\iota_{\partial M}^*\omega$ over $\partial M$, where $\partial M$ is always understood to have the Stoke's orientation. 

**Properties of Integral of Forms:** Suppose $M$ and $N$ are nonempty oriented smooth $n$-manifolds with or without boundary, and $\omega$, $\eta$ are compactly supported $n$-forms on $M$.
- *Linearity:* If $a, b\in \Bbb R$, then $$\int_M a\omega + b\eta  = a \int_M \omega + b\int_M \eta. $$
- *Orientation Reversal:*: If $-M$ denotes $M$ with the opposite orientation, then $$\int_{-M}\omega = -\int_M \omega. $$
- *Positivity:* If $\omega$ is a positively oriented orientation form, the $\int_M \omega > 0$.
- *Diffeomorphism Invariance:* If $F: N \to M$ is an orientation-preserving or orientation-reversing diffeomorphism, then $$\int_M \omega = \begin{dcases}\int_N F^*\omega & \text{if }F \text{ is orientation-preserving,} \\ -\int_N F^* \omega & \text{if }F\text{ is orientation-reversing.}\end{dcases} $$
**Cor:** Suppose $E$ and $M$ are smooth $n$-manifolds with or without boundary, and $\pi: E \to M$ is a smooth $k$-sheeted covering map or generalised covering map. If $E$ and $M$ are oriented and $\pi$ is orientation-preserving $$\int_E \pi^*\omega = k \int_M \omega $$for any compactly supported $n$-form $\omega$ on $M$.

**Integrations Over Parametrizations:** Let $M$ be an oriented smooth $n$-manifold with or without boundary, and let $\omega$ be a compactly supported $n$-form on $M$. Suppose $D_1, \dots, D_k$ are open domains of integration in $\Bbb R^n$, and for $i = 1,\dots, k$, we are given smooth maps $F_i: \overline D_i \to M$ satisfying:
- $F_i$ restricts to an orientation-preserving diffeomorphism from $D_i$ onto an open subset $W_i \subseteq M$;
- $W_i \cap W_j = \varnothing$ when $i \neq  j$;
- $\text{supp }\omega \subseteq \bigcup_{i = 1}^k \overline W_i$. 
Then  $$\int_M \omega = \sum_{i = 1}^k \int_{D_i} F^*_i \omega. $$

**Prop:** If $M$ is an oriented compact smooth $n$-manifold, $n \ge 1$, and $\omega_0, \omega_1$ are smooth orientations forms on $M$ such that $\int_M \omega_0 = \int_M \omega_1$, then there is a diffeomorphism $F: M \to M$ such that $F^*\omega_1 = \omega_0$. 

The techniques used to prove this are reliant on [[Time-Dependent Vector Fields and Flows]]. 