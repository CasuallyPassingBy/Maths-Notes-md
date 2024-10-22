---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Continuous Functions in C]], [[Complex Numbers]], [[The Derivative on R]], [[Important Functions in Complex Numbers]]

****Def:**** Let $f:A\subseteq \Bbb C \to \Bbb C$ where $A\subseteq \Bbb C$ is an open set. The function $f$ is said to be _**************differentiable (in the comples sense)**************_ at $z_0 \in A$ if

$$ \lim_{z\to z_0}\frac{f(z) - f(z_0)}{z-z_0} $$

exists. The limit denoted as $f'(z_0)$, or sometimes by $\dfrac{df}{dz}(z_0)$. Thus $f'(z_0)$ is a complex number. The function $f$ is said to be ***********_holoorphic on $A$_ if $f$ is complex differentiable at each ${z_0 \in A}$. The word _**************holomorphic**************_ is synominous to analytic. The phrase ****_holomorphic at $z_0$_ means $f$ is analyitic on a neighborhood of $z_0$.

**Prop:** If $f'(z_0)$ exists, then $f$ is continuous at $z_0$.

**Prop:** Let $f,g : A \subseteq \Bbb C \to \Bbb C$ and $z_0 \in A$. If $f'(z_0)$ and $g'(z_0)$ exists then:

- $f+g$ is differentiable at $z_0$ and $(f+g)'(z_0) = f'(z_0)+g'(z_0)$
- If $c \in \Bbb C$, then $cf$ is differentiable at $z_0$ and $(cf)'(z_0) = cf'(z_0)$
- $fg$ is differentiable at $z_0$ and $(fg)'(z_0) = f'(z_0)g(z_0)+f(z_0)g'(z_0)$
- If $g(z_0) \ne 0$, then $f/g$ is differentiable at $z_0$ and

$$ \left(\frac{f}{g}\right)'(z_0)= \frac{f'(z_0)g(z_0)-f(z_0)g'(z_0)}{g(z_0)^2} $$

### Chain Rule

Let $g:\Omega \subseteq \Bbb C \to \Bbb C$ and $f:\overline \Omega \subseteq \Bbb C \to \Bbb C$ , such that $f[\overline \Omega] \subseteq \Omega$ and $z_0 \in\overline \Omega$. If $f$ is differentiable at $z_0$ and $g$ is differentiable at $f(z_0)$, then $g \circ f$ is differentiable at $z_0$ and

$$ (g \circ f)'(z_0) = g'(f(z_0))f'(z_0) $$

************Prop:************ Any polinomial $p \in \Bbb C[x]$ is holomorphic in all $\Bbb C$, and any rational function with $p, q \in \Bbb C[x]$ of the form $p/q$ is analyitic on all $\Bbb C$ except on the roots of $q$.

************Prop:************ Let $f$ be holomorphic on an open and connected set $A$, any of the following conditions is enough to conclude that $f$ is constant.
- $|f|$ is a constant on $A$
- $f (z) \in \Bbb R$ for all $z \in A$
- $f'=0$ on $A$

******Prop:****** The function $\exp: \Bbb C \to \Bbb C$ is holomorphic on $\Bbb C$ and

$$ \frac{d}{dz} \exp(z) =\exp(z) $$

**********Cor:********** The trigonometric functions $\sin, \cos: \Bbb C \to \Bbb C$ are holomorphic on $\Bbb C$ and

$$ \frac{d}{dz} \sin z = \cos z \quad \text{ and } \quad \frac{d}{dz} \cos z= -\sin z $$

**********Prop:********** For any $y_0 \in \Bbb R$, then the $\ln_{y_0} :\Bbb C^* \to \Bbb C$ is holomorphic on ${\Bbb C\setminus\{r(\cos y_0 + i \sin y_0) \mid r \ge 0\}}$ and

$$ \frac{d}{dz} \ln_{y_0} z = \frac{1}{z} $$

for $z \in {\Bbb C\setminus\{r(\cos y_0 + i \sin y_0) \mid r \ge 0\}}$.

************Cor:************ Let $g: \Bbb C \to A_{\alpha, n}$, defined as

$$ g(z) = \exp\left(\frac{1}{n} \ln_{\alpha n}(z)\right) $$

is the $n$th root with image on $A_{\alpha, n}$. Then $g$ is continuous and holomorphic at${\Bbb C\setminus\{r(\cos(n\alpha) + i \sin(n\alpha)) \mid r \ge 0\}}$

$$ \frac{d}{dz} g(z) = \frac{1}{n(g(z))^{n-1}} $$

********Prop:******** Let $g(z) = z^n$ with $g:\Bbb C \to \Bbb C$ is holomorphic on $\Bbb C$, and

$$ \frac{d}{dz} z^n =n z^{n-1} $$
# Differentiation of Elementary Functions

******Prop:****** The function $\exp: \Bbb C \to \Bbb C$ is holomorphic on $\Bbb C$ and

$$ \frac{d}{dz} \exp(z) =\exp(z) $$

**********Cor:********** The trigonometric functions $\sin, \cos: \Bbb C \to \Bbb C$ are holomorphic on $\Bbb C$ and

$$ \frac{d}{dz} \sin z = \cos z \quad \text{ and } \quad \frac{d}{dz} \cos z= -\sin z $$

**********Prop:********** For any $y_0 \in \Bbb R$, then the $\ln_{y_0} :\Bbb C^* \to \Bbb C$ is holomorphic on ${\Bbb C\setminus\{r(\cos y_0 + i \sin y_0) \mid r \ge 0\}}$ and

$$ \frac{d}{dz} \ln_{y_0} z = \frac{1}{z} $$

for $z \in {\Bbb C\setminus\{r(\cos y_0 + i \sin y_0) \mid r \ge 0\}}$.

************Cor:************ Let $g: \Bbb C \to A_{\alpha, n}$, defined as

$$ g(z) = \exp\left(\frac{1}{n} \ln_{\alpha n}(z)\right) $$

is the $n$th root with image on $A_{\alpha, n}$. Then $g$ is continuous and holomorphic at${\Bbb C\setminus\{r(\cos(n\alpha) + i \sin(n\alpha)) \mid r \ge 0\}}$

$$ \frac{d}{dz} g(z) = \frac{1}{n(g(z))^{n-1}} $$

********Prop:******** Let $g(z) = z^n$ with $g:\Bbb C \to \Bbb C$ is holomorphic on $\Bbb C$, and

$$ \frac{d}{dz} z^n =n z^{n-1} $$