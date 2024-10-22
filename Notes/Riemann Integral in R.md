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

_**Theorem:**_ If $f\in\mathcal{R}_I$, then $f$ is bounded on $I$

### Cauchy Criterion

Let $f: I \to\mathbb{R},$ be _**Reimann integrable on $I$**_ if and only if there:

$$ \forall\varepsilon>0\exists\delta>0\forall\dot{\mathcal{P}},\dot{\mathcal{Q}}\in\dot{\wp}_I [\|\dot{\mathcal{P}}\|,\|\dot{\mathcal{Q}}\|< \delta \Rightarrow |R(f,\dot{\mathcal{P}})-R(f,\dot{\mathcal{Q}}|< \varepsilon] $$

### Squeeze Theorem

Let $f: I \to\mathbb{R},$ be _**Reimann integrable on $I$**_ if and only if:

$$ \forall\varepsilon>0\exists\alpha_\varepsilon, \omega_\varepsilon\in\mathcal{R}_I\left(\alpha_\epsilon\leq f\leq\omega_\varepsilon, \int_I\omega_\varepsilon-\alpha_\varepsilon < \varepsilon\right) $$
## Integrability

### Definition

Let $f:I\to\mathbb{R}$, is _**Darboux integrable**_ if and only if $L(f) = U(f)$, and the _**Darboux Integral**_ of $f$ over $I$:

$$ \int_I f = L(f) = U(f) $$

### Integrability Criterion

Let $f:I\to\mathbb{R}$, is _**Darboux integrable**_ if and only if:

$$ \forall\varepsilon>0\exists\mathcal{P}\in\wp_I(U(f,P) - L(f,P)<\varepsilon) $$

### Sequential Criterion

Let $f:I\to\mathbb{R}$, is _**Darboux integrable**_ if and only if there exists a sequence of partitions $(\mathcal{P}_n) \subseteq \wp_I$ such that:

$$ \lim_{n\to\infty}U(f;\mathcal{P_n})-L(f;\mathcal{P_n}) = 0 $$

$$ \int_I f= \lim_{n \to\infty} U(f;\mathcal{P_n}) = \lim_{n \to\infty} L(f;\mathcal{P_n}) $$