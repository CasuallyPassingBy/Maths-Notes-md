---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Riemann Integral in R]] [[Riemann-Steiltjes Integral on R]], [[Vector-valued functions of R]]

**Def:** Let $f:[a,b]=I\to \Bbb R^n$, and $\alpha\in BV(I)$. We say that ${f \in \mathcal{R}_I(\alpha)}$, if for every $1 \le k \le n$, ${\pi_k \circ f=f_k \in\mathcal{R}_I(\alpha)}$. If this is the case we define:

$$ \begin{align*} \int_I f\, d\alpha &= \begin{pmatrix} \int_I f_1\, d\alpha \\ \\ \int_I f_2\, d\alpha \\ \vdots \\ \int_I f_n\, d\alpha \end{pmatrix} \end{align*} $$

********Th:******** Let $F, f:[a,b] \to \Bbb R^n$ where $f \in\mathcal{R}_I$ and $F' = f$:

$$ \int_a^b f \,dt = F(b) - F(a) $$

********Th:******** Let $f:[a,b]\to\Bbb R^n$ and $\mathbf{c} \in \Bbb R^n$, then

$$ \mathbf{c} \cdot \int_a^b f = \int_a^b \mathbf{c} \cdot f $$

**Th:** Let $f:[a,b]=I\to \Bbb R^n$, $\alpha\in BV(I)$ and ${f \in \mathcal{R}_I(\alpha)}$, then ${\|f\| \in \mathcal{R}_I(\alpha)}$, and:

$$ \left\|\int_I f\,d\alpha \right\| \le \int_I \left\| f\right\|\,d\alpha $$

**Cor:** Let $f:[a,b]\to \Bbb R^n$ be a continuous function, then it follows that
$$
\left\|\int_a^b f(t)\, dt\right\|\le |b-a|\|f\|_\infty
$$

where $\|\cdot\|_\infty$ is the [[Bounded Function Spaces|uniform norm]]

**Cor:** Let $f:[a,b]=I\to \Bbb R^n$ and $f' \in \mathcal{R}_I$, then:

$$ \|f(b)-f(a)\| \le \int_a^b \|f'\| $$