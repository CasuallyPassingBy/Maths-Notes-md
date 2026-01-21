---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Metric Spaces]], [[Riemannian Metrics on Smooth Manifolds]]

If $\gamma:[a,b] \to M$ is a piecewise smooth curve segment, the *length of $\gamma$* is $$L_g(\gamma) = \int_a^b |\gamma'(t)|_g\, dt.$$Because $\|\gamma(t)\|_g$ is continuous at all but finitely any value of $t$, and has a well-defined left and right-handed limits, at those points the integral is well-defined. 

**Def:** Suppose $(M ,g)$ is a Riemannian manifold. A smooth curve $\gamma:J\to M$ is said to be a *unit-speed curve* if $|\gamma'(t)|_g = 1$.

**Prop:** Every smooth curve with nowhere-vanishing velocity has unit-speed reperametrisation on a Riemannian manifold. 

**Cor:** Every Riemannian $1$-manifold is flat. 

**Cor:** Let $\Bbb T^n := \Bbb S^1\times \dots \Bbb S^1\subseteq \Bbb C^n$, and let $g$ be the metric on $\Bbb T^n$ induced from the Euclidean metric on $\Bbb C^n$, then $g$ is flat. 

**Prop:** If $\gamma:[a,b] \to M$ is a piecewise smooth curve segment and $a<c<b$, then $$L_g(\gamma) = L_g(\gamma|_{[a,c]}) + L_g(\gamma|_{[c,b]}).$$
**Parameter Independence of Length:** Let $(M,g)$ be a Riemannian manifold, and let $\gamma:[a,b]\to M$ be a piecewise smooth curve segment. If $\widetilde\gamma$ is a reparametrisation of $\gamma$, then $L_g(\widetilde \gamma) = L_g(\gamma)$. 

**Prop:** Let $(M, g)$ and $(\widetilde M, \widetilde g)$ be Riemannian manifolds. If $F: M \to \widetilde M$ is an isometry and $\gamma:[a,b] \to M$ is a piecewise smooth curve segment, then $L_{\widetilde g}(F \circ\gamma) = L_g(\gamma)$. 

**Def:** Suppose $(M, g)$ is a connected Riemannian manifold. For any $p, q\in M$, the *Riemannian distance function from $p$ to $q$*, denoted by $d_g(p, q)$, is defined to be the infimum of $L_g(\gamma)$ over all piecewise smooth curve segments from $p$ to $q$. 

**Prop:** If $(M, g)$ and $(\widetilde M, \widetilde g)$ are connected Riemannian manifolds and $F:M \to \widetilde M$ is an isometry, then $d_{\widetilde g}(F(p), F(q)) = d_g(p,q)$ for all $p, q\in M$. 

**Prop:** Let $(M, g)$ is a compact Riemannian manifold and $p,q\in M$, If there is a piecewise smooth curve segment connecting $p$ and $q$, then there exists a piecewise smooth curve segment $\gamma$ joining $p$ and $q$ that satisfy$$L_g(\gamma) = d_g(p, q).$$In other words, the infimum in the definition of the Riemannian distance is attained. 

**Lemma:** Let $g$ be any Riemannian metric on an open set $U\subseteq \Bbb R^n$. For any compact $K\subseteq U,$ then there exists positive constants $c, C$ such that for all $x\in K$ and all $v\in T_x\Bbb R^n$, $$c\|v\|_{\overline g}\le  \|v\|_g \le C\|v\|_{\overline g}, $$where $\overline g$ is the Euclidean metric. 

**Riemannian Manifolds as Metric Spaces:** Let $(M, g)$ be a connected Riemannian manifold. With the Riemannian distance function, $M$ is a metric space whose metric topology is the same as the original manifold topology. 

As a consequence of this theorem, all of the terminology of metric spaces can be carried over to connected Riemannian manifolds. Thus, a connected Riemannain manifold $(M, g)$ is said to be *complete*, and $g$ is said to be a *complete Riemannian metric*, if $(M, d_g)$ is a [[Complete Metric Spaces|complete metric space]]; and a subset $B\subseteq M$ is said to be *bounded* if there exists a constant $K$ such that $d_g(x, y)\le K$ for all $x, y\in B$. 

**Cor:** Every smooth manifold with or without boundary is metrizable, 

**Prop:** Suppose $g = f(t) dt^2$ is a Riemannian metric on $\Bbb R$. Then $g$ is complete iff both of the following improper integrals diverge: $$\int_0^\infty \sqrt{f(t)}\, dt, \qquad \int_{-\infty}^0\sqrt{f(t)}\, dt.$$
**Prop:** Let $M$ be a connected noncompact smooth manifold and let $g$ be a Riemannian metric on $M$. There exists a positive function $h\in\mathcal C^\infty(M)$ such that the Riemannian metric $\widetilde g = hg$ is complete. 

**Prop:** Suppose $(M, g)$ is connected Riemannian manifold $S\subseteq M$ is a connected embedded submanifold, and $\widetilde g$ is the induce Riemannian metric on $S$.
- $d_{\widetilde g}(p,q) \ge d_g(p, q)$ for $p, q\in S$.
- If $(M, g)$ is complete and $S$ is properly [[Embedded Smooth Submanifolds|embedded]], then $(S, \widetilde g)$ is complete.

**Cor:** Every connected smooth manifold admits a complete Riemannian metric.