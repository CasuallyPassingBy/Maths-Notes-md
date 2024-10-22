---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Functions of Bounded Variation on R]], [[Riemann Integral in R]]

Let $\alpha:I =[a,b]\to\mathbb{R}$ be monotonically increasing. Given a partition $P$ of $I$, then:

$$ \Delta\alpha_i = \alpha(x_i)-\alpha(x_{i-1}) $$

The set of all function _Reimann-Stieltjes Integrable_ with respect to $\alpha$ along $I$ is denoted as $\mathcal{R}_I(\alpha)$

There’s also the option of $\alpha$ to be of _bounded variation,_ which is a generalization of monotonicity.

## Reimann Sums

Let $f:I\to\mathbb{R}$, a _**Reimann-Stieltjes**_ sum is defined as follows, given $\dot{\mathcal{P}}\in\dot{\wp}_I$:

$$ R(f; \dot{\mathcal{P}}, \alpha) = \sum_{i= 1}^n f(t_i)\Delta\alpha_i $$

### Integrability

Let $f:I\to\mathbb{R}$, be _**Reimann-Stieltjes Integrable**_ iff:

$$ \exists L\in\mathbb{R} \forall\varepsilon>0 \exists\delta>0 \forall\dot{\mathcal{P}}\in\dot{\wp}_I [\|\dot{\mathcal{P}}\|< \delta \Rightarrow |R(f,\dot{\mathcal{P}}, \alpha)-L|] $$

$L$ is called the _Riemann-Stieltjes integral_ of $f$ with respect to $\alpha$ along $I$, denoted as:

$$ \int_If(x) \,d\alpha(x) = \int_I f \,d\alpha

$$

## Darboux Sums

Given $f:I\to\mathbb{R},$ bounded the lower and upper sum of a parition $P$ with respect to $\alpha$ are defined as follows:

$$ L(f,\mathcal{P},\alpha) = \sum_{i =1}^nm_i\Delta\alpha_i \text{, where } m_i := \inf_{x\in[x_i, x_{i-1}]}f(x) $$

$$ U(f,\mathcal{P},\alpha) = \sum_{i =1}^nM_i\Delta\alpha_i \text{, where } M_i := \sup_{x\in[x_i, x_{i-1}]}f(x) $$

Similarly, there’s a lower integral and upper integral with respect to $\alpha$:

$$ L(f,\alpha) = \underline{\int_I}f\,d\alpha= \sup_{\mathcal{P}\in\wp_I}L(f,\mathcal{P},\alpha) $$

$$ U(f,\alpha) = \overline{\int_I}f\,d\alpha= \inf_{\mathcal{P}\in\wp_I}U(f,\mathcal{P},\alpha) $$

_**Lemma:**_ If $\mathcal{P}'$ is a refinement of a partition $\mathcal{P}$, and has the corresponding relation with the lower and upper sums:

$$ L(f,\mathcal{P}, \alpha) \leq L(f,\mathcal{P}' , \alpha)\leq U(f,\mathcal{P}', \alpha) \leq U(f, \mathcal{P}, \alpha) $$

_**Theorem: $L(f,\alpha) \le U(f,\alpha)$**_

### Integrability
$f:I\to\mathbb{R}$ is _Reimann-Stieltjes integrable_ iff:

$$ \underline{\int_I}f\,d\alpha = \overline{\int_I}f\,d\alpha $$

_**Darboux-Cauchy Criterion**_ $f:I\to\mathbb{R}$ is _Reimann-Stieltjes integrable_ $(f\in\mathcal{R}_{I}(\alpha))$ iff:

$$ \forall\varepsilon>0\exists\mathcal{P}\in\wp_I(U(f,P,\alpha) - L(f,P,\alpha)<\varepsilon) $$

_**Theorem:**_
1. Given an $\varepsilon > 0$, and there’s a $\mathcal{P}$ such that satisfies the _Darboux-Cauchy Criterion,_ any refinement of $\mathcal{P}$ also satisfies it.
    
2. Given an $\varepsilon > 0$, and there’s a $\mathcal{P}$ such that satisfies the _Darboux-Cauchy Criterion,_ any $t_i, s_i \in[x_i, x_{i-1}]$ then:
	$$ \sum_{i=i}^n|f(s_i) - f(t_i)|\Delta\alpha_i <\varepsilon $$
    
3. If $f\in\mathcal{R}_I(\alpha)$, and $(2)$ is satisfied, then:
$$ \left|\sum_{i=1}^nf(t_i)\Delta\alpha -\int_I f\,d\alpha\right| $$

## Integral Properties

### Additivity Theorem

1. If $f\in\mathcal{R}_{[a,b]}(\alpha)$, and $c \in (a,b)$, then $f\in\mathcal{R}_{[a,c]}(\alpha)$ and $f\in\mathcal{R}_{[c,b]}(\alpha)$, and:
    
    $$ \int_a^bf\,d\alpha = \int_a^cf\,d\alpha+\int_c^bf\,d\alpha $$
    

### General Integrability Theorems
1. If$f$ $\in {\cal C}^0[a,b]$, then $f\in\mathcal{R}_I(\alpha)$.
2. If $f$ is monotonic on $[a,b]$ and $\alpha$ is continuous on $[a,b],$ then $f\in\mathcal{R}_I(\alpha)$.
3. Let $f$ be bounded on $[a,b]$, and only has a finite number of discontinuities on $[a,b]$, and $\alpha$ is continuous at all discontinuities of $f$, then $f\in\mathcal{R}_I(\alpha)$.
4. Let $f\in\mathcal{R}_I(\alpha)$, there’s $m,M\in \mathbb{R}[m\le f\le M]$ on $I$, ${\phi\in\mathcal{C}^0([m, M])}$ then $\phi \circ f\in\mathcal{R}_I(\alpha)$ .

### Algebraic Properties
1. If $f_1, f_2\in\mathcal{R}_I(\alpha)$, then $f_1 +f_2\in\mathcal{R}_I(\alpha)$, and:
    
    $$ \int_I f_1 +f_2 \,d\alpha = \int_If_1\,d\alpha + \int_If_2\,d\alpha $$
    
2. If $f \in\mathcal{R}_I(\alpha)$, and $c\in\mathbb{R}$, then $cf\in\mathcal{R}_I(\alpha)$, and:
    
    $$ \int_Icf\,d\alpha = c\int_If\,d\alpha $$
    
3. If $f_1 \le f_2$ on $I$, then:
    
    $$ \int_If_1\,d\alpha \le\int_If_2\,d\alpha $$
    
4. If $f\in\mathcal{R}_I(\alpha)$ y $|f| \le M$ on $[a,b]$, then:
    
    $$ \left|\int_If\,d\alpha\right| \le M(\alpha(b)-\alpha(a)) $$
    
5. If $f\in\mathcal{R}_{I}(\alpha_1)$ and $f\in\mathcal{R}_{I}(\alpha_2)$, then $f\in\mathcal{R}_{I}(\alpha_1 +\alpha_2)$ and:
    
    $$ \int_If\,d(\alpha_1 +\alpha_2) = \int_If\,d\alpha_1 +\int_If\,d\alpha_2 $$
    
6. If $f\in\mathcal{R}_{[a,b]}(\alpha)$, and $c\in\mathbb{R}^+$, then $f\in\mathcal{R}_{[a,b]}(c\alpha)$ and:
    
    $$ \int_If\,d(c\alpha) = c\int_If\,d\alpha $$
    
7. If $f,g \in\mathcal{R}_I(\alpha)$, then $fg\in\mathcal{R}_I(\alpha)$.
    
8. If $f\in\mathcal{R}_I(\alpha)$, then $|f|\in\mathcal{R}_I(\alpha)$ and:
    
    $$ \left|\int_I f\,d\alpha\right|\le \int_I |f| \,d\alpha $$
    

### Unit Step Function

The _unit step function_: $u:\mathbb{R}\to\{0,1\}$, where:

$$ u(x) := \begin{cases} 0 & x\le 0\\ 1 & x > 0 \end{cases} $$

_**Theorem:**_ Let $s\in(a,b)$, if $f$ is bounded on $[a,b]$, and $f$ is continuous on $s$ and $\alpha(x) = u(x-s)$, then:

$$ \int_a^bf\,d\alpha = f(s) $$

_**Theorem:**_ Let $\forall n\in\mathbb{N}(c_n \geq 0)$, and that $\sum c_n$ converge, $(s_n)_{n\in\mathbb{N}}$ be a sequence of different points of $[a,b]$ and:

$$ \alpha(x) = \sum_{n\in\mathbb{N}} c_nu(x-s_n) $$

Let $f$ be continuous on $[a,b]$. Then,

$$ \int_a^bf\,d\alpha = \sum_{n\in\mathbb{N}}c_nf(s_n) $$

### Miscellaneous

_**Theorem:**_ Let $\alpha$ be monotonically increasing and $\alpha'\in\mathcal{R}_I$. Let $f$ be bounded function on $[a,b]$. If $f\in\mathcal{R}_I(\alpha)$ iff $f\alpha'\in\mathcal{R}_I$, and:

$$ \int_a^bf\,d\alpha = \int_a^b f\alpha' $$

_**Change of variables:**_ Let $\varphi$ be strictly increasing continuous function that maps $[A,B]$ onto $[a,b]$. Let $\alpha$ be monotonically increasing on $[a,b]$ and $f\in\mathcal{R}_I(\alpha)$. Let’s define $\beta$ and $g$ on $[A,B]$ as:

$$ \beta(y) = \alpha(\varphi(y)), \text{ and } g(y) =f(\varphi(y)) $$

Then $g\in\mathcal{R}_{[A,B]}(\beta)$, and

$$ \int_A^Bg\,d\beta = \int_a^bf\,d\alpha

$$