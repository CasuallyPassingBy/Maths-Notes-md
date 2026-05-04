---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Riemann and Darboux Sums in R]]

## Integrability in Riemann

### Original Definition

Let $f: I \to\mathbb{R},$ be _**Reimann integrable on $I$**_ if and only if there:

$$ \exists L\in\mathbb{R} \forall\varepsilon>0 \exists\delta>0 \forall\dot{\mathcal{P}}\in\dot{\wp}_I [\|\dot{\mathcal{P}}\|< \delta \Rightarrow |R(f,\dot{\mathcal{P}})-L| < \varepsilon] $$

$L$ is also called the _**Reimann integral**_ of $f$ along $I$, also denoted as: $\int_If$ . The set of Reimann integrable functions is denoted as: $\mathcal{R}_I$

Other notation is: $\lim_{\|\dot{P}\|\to 0}R(f,\dot{P}) = L$ .

_**Theorem:**_ If $f \in \mathcal{R}_I$, then the integral is uniquely determined.

_**Theorem:**_ If $f \in\mathcal{R}_I$, and $f=g$ except at finitely many points, then $g \in\mathcal{R_{[a,b]}}$ and .

$$ \int_If = \int_Ig $$

_**Theorem:**_ If $f\in\mathcal{R}_I$, then $f$ is bounded on $I$.

We see that the set of partition of the closed interval $I$ is a directed set. We see that the refinement is the preorder relation. This means that $\lim_{\|P\| \to 0} R(f, \dot P) = L$ means that is the [[Convergence of Nets|limit of the net]] indexed by the set of tagged partitions. 

### Cauchy Criterion

Let $f: I \to\mathbb{R},$ be _**Reimann integrable on $I$**_ if and only if there: $$ \forall\varepsilon>0\exists\delta>0\forall\dot{\mathcal{P}},\dot{\mathcal{Q}}\in\dot{\wp}_I [\|\dot{\mathcal{P}}\|,\|\dot{\mathcal{Q}}\|< \delta \Rightarrow |R(f,\dot{\mathcal{P}})-R(f,\dot{\mathcal{Q}})|< \varepsilon] $$ ^9a7c62

### Squeeze Theorem

Let $f: I \to\mathbb{R},$ be _**Reimann integrable on $I$**_ if and only if:

$$ \forall\varepsilon>0\exists\alpha_\varepsilon, \omega_\varepsilon\in\mathcal{R}_I\left(\alpha_\epsilon\leq f\leq\omega_\varepsilon, \int_I\omega_\varepsilon-\alpha_\varepsilon < \varepsilon\right) $$
## Integrability

### Definition

Let $f:I\to\mathbb{R}$, is _**Darboux integrable**_ if and only if $L(f) = U(f)$, and the _**Darboux Integral**_ of $f$ over $I$:

$$ \int_I f = L(f) = U(f) $$

### Integrability Criterion

Let $f:I\to\mathbb{R}$, is _**Darboux integrable**_ if and only if: $$ \forall\varepsilon>0\exists\mathcal{P}\in\wp_I(U(f,P) - L(f,P)<\varepsilon) $$

### Sequential Criterion

Let $f:I\to\mathbb{R}$, is _**Darboux integrable**_ if and only if there exists a sequence of partitions $(\mathcal{P}_n) \subseteq \wp_I$ such that:

$$ \lim_{n\to\infty}U(f;\mathcal{P_n})-L(f;\mathcal{P_n}) = 0 $$

$$ \int_I f= \lim_{n \to\infty} U(f;\mathcal{P_n}) = \lim_{n \to\infty} L(f;\mathcal{P_n}) $$

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

We see that ${\cal R}_I$ is a vector space and the integral is a linear functional in this space.

## Lebesgue’s Criterion

Let $f:[a,b] \to \mathbb{R}$, $f\in\mathcal{R}_{[a,b]} \iff \lambda(D_f) =0$, where $\lambda$ is the [[Lebesgue Measure]], and $D_f$ is the set of all discontinuities of $f$, or $f$ is continuous almost everywhere on $[a,b]$.

**Th:** If $f$ is Riemann integrable, then $f$ is [[Lebesgue Integral on Measure Spaces|Lebesgue integrable]] and the Riemann integrable and Lebesgue integrals of $f$ coincide.

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