---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Line Integral over a Vector Field]], [[Covector Fields on Smooth Manifolds]], [[Conservative Fields]], [[The Cotangent Bundle]], [[Local and Global Sections of Vector Bundles]], [[Riemann Integral in R]]

Another important application of covector fields is to make coordinate independent sense of the notion of a [[Line Integral over a Vector Field|line integral]].

Suppose $[a,b]\subseteq \Bbb R$ is a compact interval and $\omega$ is a smooth covector field on $[a,b]$. If we let $t$ denote the standard coordinate on $\Bbb R$, $\omega$ can be written as $\omega_t = f(t)\, dt$ for some smooth function $f:[a,b] \to\Bbb R$. We define the *integral of $\omega$ over $[a,b]$* to be $$\int_{[a,b]} \omega := \int_a^b f(t)\,dt.$$

**Diffeomorphism Invariance of the Integral:** Let $\omega$ be a smooth covector field on the compact interval $[a,b]\subseteq \Bbb R$. If $\varphi: [c,d] \to [a,b]$ is an increasing diffeomorphism, then $$\int_{[c,d]} \varphi^*\omega = \int_{[a,b]} \omega,$$and if $\varphi$ is a decreasing diffeomorphism then $$\int_{[c,d]} \varphi^*\omega =- \int_{[a,b]} \omega.$$

Now let $M$ be a smooth manifold. By a *curve segment* in $M$ we mean a continuous curve $\gamma: [a,b] \to M$ whose domain is a compact interval. It is a *smooth curve segment* if it has a smooth extension to an open interval containing $[a,b]$. A *piecewise smooth curve segment* is a curve segment $\gamma: [a,b] \to M$ with the property that there exists a finite partition $a = a_0<a_1<\dots <a_k = b$ of $[a,b]$ such that $\gamma|_{[a_{i-1}, a_i]}$ is smooth for each $i$. 

**Lemma:** If $M$ is a connected smooth manifold, any two points of $M$ can be joined by a piecewise smooth curve segment.

If $\gamma:[a,b] \to M$ is a smooth curve segment and $\omega$ is a smooth covector field on $M$, we define the *line integral* of $\omega$ over $\gamma$ to be the real number$$\int_\gamma \omega:= \int_{[a,b]}\gamma^*\omega. $$More generally, if $\gamma$ is piecewise smooth, we define $$\int_\gamma \omega := \sum_{i = 1}^k \int_{[a_{i-1},a_i]}\gamma^*\omega,$$where $[a_{i-1}, a_i]$, $i \in\{1,\dots, k\}$, are the intervals on which $\gamma$ is smooth. 

**Properties of Line Integrals:** Let $M$ be a smooth manifold. Suppose $\gamma:[a,b] \to M$ is a piecewise smooth curve segment and $\omega,\omega_1,\omega_2\in \Omega^1(M)$. 
- For any $c_1, c_2\in \Bbb R$, $$\int_\gamma (c_1\omega_1+c_2\omega_2) = c_1\int_\gamma \omega_1 + c_2\int_\gamma \omega_2. $$
- It $\gamma$ is a constant map, then $\int_\gamma\omega = 0.$ 
- If $a<c<b$, then$$\int_\gamma\omega = \int_{\gamma_1}\omega+ \int_{\gamma_2}\omega, $$where $\gamma_1 := \gamma|_{[a,c]}$ and $\gamma_2 := \gamma|_{[c,b]}$. 

**Prop:** Suppose $F: M \to N$ is any smooth map, $\omega\in \Omega^1(N)$, and $\gamma$ is a piecewise smooth curve segment in $M$, then $$\int_\gamma F^*\omega = \int_{F \circ \gamma}\omega. $$

**Prop:** If $\gamma: [a,b] \to M$ is a piecewise smooth curve segment, the line integral of $\omega$ over $\gamma$ can also be expressed as the ordinary integral $$\int_\gamma \omega = \int_a^b \omega_{\gamma(t)}(\gamma'(t))\, dt. $$
**Parameter Independence of Line Integrals:** Suppose $M$ is a smooth manifold, $\omega$ is a smooth covector field on $M$, and $\gamma$ is a piecewise smooth curve in $M$. For any reparametrization $\widetilde \gamma$ of $\gamma$ we have $$\int_{\widetilde\gamma} \omega = \begin{dcases}
\int_\gamma\omega & \text{if $\widetilde\gamma$ is a forward reparametrization,} \\
-\int_\gamma\omega & \text{if $\widetilde\gamma$ is a backward reparametrization.}
\end{dcases}
$$
**Fundamental Theorem for Line Integrals:** Let $M$ be a smooth manifold. Suppose $f$ is a smooth real-valued function on $M$ and $\gamma: [a,b] \to M$ is a piecewise smooth curve segment in $M$. Then  $$\int_\gamma df = f(\gamma(b)) - f(\gamma(a)). $$
# Conservative Covector Field

We say that a smooth covector field $\omega$ on a manifold $M$ is *exact*, or an *exact differential* on $M$ if there is a function $f\in \mathcal C^\infty(M)$ such that $\omega = df$. In this case, the function $f$ is called a *potential* for $\omega$. The potential is not uniquely determined, but the difference between two potentials for $\omega$ must be a constant on each component of $M$.

We say that $\gamma$ is a *closed* curve segment if $\gamma(a) = \gamma(b)$. 

We say that a smooth covector field $\omega$ is *conservative* if the line integral of $\omega$ over any closed piecewise smooth curve segment is zero. 

**Lemma:** A smooth covector field $\omega$ is conservative iff the line integral of $\omega$ depends only on the endpoints of the curve, i.e., $\omega_\gamma\omega = \int_{\widetilde\gamma}\omega$ whenever $\gamma$ and $\widetilde \gamma$ are piecewise smooth curve segments with the same starting and ending points. 

**Prop:** If $M$ is a compact manifold,, then every exact covector field on $M$ vanishes at least at two points. 

**Th:** A smooth covector field is conservative iff it is exact. 

Let $f$ be any potential function for $\omega$, and let $(U, (x^i))$ be any smooth chart of $M$. Because $f$ is smooth, it satisfies the following identity on $U$:$$\frac{\partial^2 f}{\partial x^i\partial x^j} = \frac{\partial^2 f}{\partial x^j\partial x^i}.$$Writing $\omega = \omega_i \,dx^i$ in coordinates, the fact that $\omega = df$, is equivalent to $\omega_i = \frac{\partial f}{\partial x_i}$. Substituting this, we get that$$\frac{\partial \omega_i}{\partial x^j} = \frac{\partial \omega_j}{\partial x^i}.$$We say that a smooth covector field $\omega$ is *closed* if its components in every smooth chart satisfy the equality above. 

**Lemma:** Every exact covector field is closed. 

**Prop:** Let $\omega$ be a smooth covector field. If $\omega$ satisfy $\frac{\partial \omega_i}{\partial x^j} = \frac{\partial \omega_j}{\partial x^i}.$ in some smooth chart around every point, then it is closed. 

**Cor:** If $G: M \to N$ is a local diffeomorphism, then the pullback $G^* : \Omega^1(N) \to \Omega^1(M)$ takes closed covector fields to closed covector fields, and exact one to exact ones. 

The question of whether a particular closed covector field is exact is a global one, depending on the shape of the domain in question. This observation is the starting point for *[[de Rham Cohomology]]*, which expresses a deep relationship between smooth structures and topology. 

**Prop:** If $U$ is a star-shaped open subset of $\Bbb R^n$, then every closed covector field on $U$ is exact. 

**Local Exactness of Closed Covector Fieds:** Let $\omega$ be a closed covector field on a smooth manifold $M$. Then every $p\in M$ has a neighbourhood on which $\omega$ is exact. 