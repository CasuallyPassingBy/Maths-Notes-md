---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Riemann Integral in R]]

## Equivalence

_**If a function is Reimann Integrable if and only if it is Darboux Integrable**_

_**General type of Integrable functions: $\mathcal{C}^0(I) \subset\mathcal{R}_I$,**_ and all monotonic functions since they are continuous almost everywhere. $\mathcal{ R}_I$ is an associative commutative algebra over $\Bbb R$.

## Additivity Theorem

******Let $f$ be integrable in $[a,b]$ if and only if $f$ is integrable in $[a,c]$ and $[c,b]$ for some $c \in(a,b)$, and:

$$ \int_a^bf= \int_a^cf+\int_c^bf $$

_**Corollary:**_ $[c, d] \subseteq [a,b] \implies \mathcal{R}_{[c,d]} \subseteq\mathcal{R}_{[a,b]}$

_**Definition:**_ If $a < b$ then:

$$ \int_b^af =-\int_a^bf \text{, and }\int_a^a f =0 $$

## Algebraic Properties

Suppose that $f,g \in\mathcal{R}_I$, and $c \in\mathbb{R}$, then:

1. $cf \in\mathcal{R}_I$, and $\int_Icf= c\int_If.$
2. $f+g\in\mathcal{R}_I$, and $\int_I(f+g) = \int_If +\int_Ig$.
3. If $m \leq f\leq M \implies m\mu(I)\leq \int_I f\leq M\mu(I)$, where $\mu$ is the Lebesgue measure.
4. If $f \leq g$ on $I \implies \int_If \leq \int_Ig$.
5. The function $|f| \in\mathcal{R}_I$ , and $\big|\int_If \big|\leq \int_I|f|$.

## Lebesgue’s Criterion

Let $f:[a,b] \to \mathbb{R}$, $f\in\mathcal{R}_{[a,b]} \iff \mu(D_f) =0$, where $\mu$ is the Lebesgue Measure, and $D_f$ is the set of all discontinuities of $f$, or $f$ is continuous almost everywhere on $[a,b]$.

### Composition Theorem

Let $f\in\mathcal{R}_{[a,b]}$, and $f([a,b]) \subseteq [c,d]$ , where $\varphi \in \mathcal{C^0}[c,d]$, then $\varphi \circ f\in \mathcal{R}_{[a,b]}$

_**Corollary:**_

If $f, g \in\mathcal{R}_I \implies fg \in\mathcal{R}_I$

## Interchange of limit and integral

### Integrable limit theorem

Assume that $f_n \rightrightarrows f$ on $I$, and that each $f_n \in\mathcal{R}_I$, then $f \in\mathcal{R}_I$ and that:

$$ \lim_{n\to\infty}\int_If_n = \int_If $$

### Bounded Convergence Theorem

Assume that $f_n \Bbb Rightarrow f$, and $\exists K> 0\forall n \in \mathbb{N} (|f_n| \leq K)$, with both , $\forall n\in\mathbb{N}(f_n\in\mathcal{R}_I), f \in\mathcal{R}_I$, then:

$$ \lim_{n\to\infty}\int_If_n = \int_If $$

### Theorem

Let $g_n \to g$ on $[a, b]$ and uniformly on $[a, \gamma]$ where $\gamma\in(a,b)$, and $g_n$ is uniformly bounded and integrable, then:

$$ \lim_{n\to\infty}\int_a^bg_n =\int_a^bg $$

Let $f:[a,b]\to\Bbb R$ be bounded on $[a,b]$ and for any $c\in(a,b]$, $f\in\mathcal{R}_{[c,b]}$. Then, $f\in\mathcal{R}_{[a,b]}$ and,

$$ \lim_{c\to a^+}\int_c^bf=\int_a^bf $$