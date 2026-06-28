---
tags:
  - ProbabilityTheory
  - MeasureTheory
  - Topology
---
Subjects: [[Probability Theory]], [[Measure Theory]], [[Topology]]
Links: [[Stone-Čech compactification]], [[Space of Continuous Functions that Vanish at Infinity]], [[Topological Dual Vector Space]], [[Measures on Hausdorff Spaces]], [[Vague Topology on the Space of Radon Measures]]

Let $X$ be a Tychonoff space. We denote the Stone-Čech compactification of $X$ by $\beta X$. We see that there's an isometric isomorphism between $C_b(X, \Bbb F)$ and $C(\beta X,\Bbb F)$. We note that $C(\beta X, \Bbb F) = C_0(\beta X, \Bbb F) = C_b(\beta X, \Bbb F)$. Thus  $$C_b(X, \Bbb F)^* \cong C(\beta X, \Bbb F) \cong M(\beta X, \Bbb F),$$by the Riesz representation theorem, where $M(\beta X, \Bbb F)$ represents the set of  Radon measures on $\beta X$ with finite variation (they can be signed or complex depending on $\Bbb F$). 

Let us consider the set $M(X)$ to the set of Radon measures on $X$ with bounded variation. Let $\iota:X \hookrightarrow \beta X$  be the natural embedding of $X$ into $\beta X$. We see that if $\mu$ is a Radon measure on $X$, then $\iota_*\mu$ is a a Radon measure on $\beta X$. Additionally, we see that the mapping $\iota_*: M(X, \Bbb F) \to M(\beta X, \Bbb F)$ defined by $\iota_*(\mu) := \iota_* \mu$ is an isometric embedding. 

We can endow the space $M(\beta X, \Bbb F)$ with the weak*-topology, and, in turn, give $M(X, \Bbb F)$ the subspace topology of this topological space. We call this topology on $M(X, \Bbb F)$ the *weak topology*. 

Let $(\mu_{\alpha})_{\alpha\in A}$ be a net of Radon measures with bounded variation on $X$ and let $\mu$ be a Radon measure with bounded variation on $X$. We say that $(\mu_{\alpha})_{\alpha\in A}$ *converges weakly* to $\mu$, denoted by $\mu_\alpha \stackrel{w}{\longrightarrow} \mu$ if for $f\in \mathcal C_b(X)$, we have$$\lim_{\alpha} \int f\, d\mu_\alpha= \int f\, d\mu. $$By the universal property of $\beta X$, this is topologically equivalent to saying that the push-forward net $(\iota_* \mu_\alpha)_{\alpha\in A}$ converges in the weak* topology of $M(\beta X, \Bbb F)$ to $\iota_*\mu$. Furthermore, let $P(X)$ denote the space of all Radon probability measures on $X$. If $\mu_\alpha\in P(X)$ for all $\alpha\in A$ and the weak limit $\mu$ also belongs to $P(X)$, we say that $(\mu_\alpha)_{\alpha\in A}$ *converges in distribution*, or *converges narrowly*, to $\mu$. 

Note that if $\mu\in P(X)$, then its total variation $\|\mu\| = \mu(X) = 1$. since $\iota_*$ is an isometric embedding, then image $\iota_*[P(X)]$ is a subset of the unit sphere of $M(\beta X, \Bbb F)$. In fact, because probability measures are positive $\iota_*[P(X)]$ is embedded into the intersection of the unit sphere and the positive cone of $M(\beta X, \Bbb F)$. 

We see that the space $M(X, \Bbb F)$ with the weak topology is a Hausdorff space. 

**Lemma:** Let $\mu$ and $\nu$ be Radon measures on $X$ with bounded variation. If $$\int f\, d\mu = \int f\, d\nu $$for all $f\in \mathcal C_b(X, \Bbb F)$, then $\mu = \nu$. 