---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Continuity on R]]
## Types

1. if $\lim_{x\to c}f(x)$ exists but has a different value of $f(c)$, it is a _removable discontinuity._
2. if $\lim_{x\to c^-}f(x)\neq\lim_{x\to c^+}f(x)$, it is a _jump discontinuity._
3. if $\lim_{x\to c}f(x)$ doesn’t exist for any other reason, it is an _essential discontinuity._

## Sets of Discontinuities

Let $f:\Bbb{R}\to\Bbb{R}$, $D_f$ is the set of discontinuities of $f$:

$$ D_f=\{x\in\Bbb{R}:f \text{ is discontinuous at }x\} $$

Let $f:\Bbb{R}\to\Bbb{R}$, and $\alpha >0$, $f$ is $\alpha$_-continuous at $x$_ iff:

$$ \exists\delta>0\forall y,z\in\Bbb{R}[|z-y|< \delta\implies|f(z)-f(y)|< \alpha] $$

The set of $\alpha$ discontinuities of $f$ is defined as:

$$ D_f^\alpha = \{x\in\Bbb{R}: f\text{ is not $\alpha$ continous} \} $$

$D_f^\alpha$ is a closed.

_**Lemma:**_ Let $\alpha < \alpha'$ , then $D_f^{\alpha'} \subseteq D_f^\alpha$

_**Lemma:**_ Let $\alpha > 0$, then $D_f^\alpha \subseteq D_f$

_**Theorem:**_ Let $(\alpha_n)$ be a sequence $\forall n\in\Bbb{N}[\alpha_n> 0]$, such that $\alpha_n\to 0$, then:

$$ D_f = \bigcup_{n\in\Bbb{N}}D_f^{\alpha_n} $$

Thus, $D_f$ is an $F_\sigma$ set.

_**Corollary:**_ There’s no function such that $D_f = \Bbb{R}\setminus\mathbb{Q}$ since by [[Baire's Category Theorem|Baire’s Category Theorem]], $\Bbb{R}\setminus\mathbb{Q}$ cannot be $F_\sigma$.

## Monotone Functions

$f:D\to\Bbb{R}$, $f$ is called _monotone_ iff either:

- $\forall x,y\in D [x\le y\implies f(x)\le f(y)]$, increasing monotone function.
- $\forall x, y\in D[x\le y\implies f(x) \ge f(y)]$, decreasing monotone function.

_**Theorem:**_ if $f$ is monotonic, then $|D_f| \le \aleph_0$, thus $\mu(D_f) = 0$, and $f$ is continuous almost everywhere.

_**Theorem:**_ if $f$ is monotonically increasing and $c$ is a limit point of $D$, then:

1. $\lim_{x\to c^-} f(x)= \sup_{x < c} f(x)$
2. $\lim_{x\to c^+} f(x)= \inf_{x > c} f(x)$