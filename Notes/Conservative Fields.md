---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Line Integral over a Vector Field]], [[Connected Sets in Rn]]
**********Def:********** Let $F:U \subseteq\Bbb R^n \to \Bbb R^n$ a continuous function on $U$, an open and connected set. $F$ is called a _************conservative field or gradient on U************_ if there’s a function $\varphi :U\to \Bbb R$ such that ************************** ^ddeab3

$$ F(x) = \nabla \varphi(x) \qquad \text{for all $x \in U$} $$

In this case we say that $\varphi$ is a _gradient or a potential_ for $F$.

********Th:******** Let $F =(F_k)_{k = 1}^n :U \to \Bbb R^n$ is continuous over a region (open and connected set) $U$. Then the following are equivalent: ^13cae7
- $F$ is a conservative field on $U$
- the line integral of $F$over any closed curve $\Gamma \subseteq U$ parametrized by a piecewise smooth and closed function $\gamma$, then
    
    $$ \oint_\Gamma F \cdot\, d\gamma = 0 $$
    
- the line integral of $F$ over any curve $\Gamma \subseteq U$ parametrized by a piecewise smooth function $\gamma$ only depends of the extreme points of $\gamma$. In other words, if $\gamma:[a,b] \to\Bbb R^n$ and ${\delta:[c, d]\to \Bbb R^n}$ be piecewise smooth functions, parametrizing $\Gamma \subseteq U$ and $\Delta \subseteq U$ respectively, such that $\gamma(a) = \delta (c)$ and $\gamma(b) = \delta(d)$, then
    $$ \int_\Gamma F\cdot\, d\gamma = \int_\Delta F\cdot \, d\delta $$

**Prop:** Let $F =(F_k)_{k = 1}^n :U \to \Bbb R^n$ be a $\cal C^1$ function on $U$. If $F$ is conservative field on $U$ then
$$ J_F(x) =(J_F (x))^\top $$
for all $x \in U$.

**Def:** Let $U \subseteq \Bbb R^n$ a region. We say that $U$ is a star-domain if there’s a $x_0 \in U$, such that for any $y \in U$, then $[x_0, y] \subseteq U$.

**Th:** Let $F =(F_k)_{k = 1}^n :U \to \Bbb R^n$ be a $\cal C^1$ function on $U$. If $F$ is a field on $U$, with $U$ a star region. If
$$ J_F(x) =(J_F (x))^\top $$

for all $x \in U$ then $F$ is a conservative field on $U$.

**Cor:** Let $F =(F_k)_{k = 1}^n :U \to \Bbb R^n$ be a $\cal C^1$ function on $U$. If $F$ is conservative field on $U$, with $U$ a star region.

$$ J_F(x) =(J_F (x))^\top $$

for all $x \in U$ iff $F$ is a conservative field on $U$.

### Smooth Homotopy
**Def:** A homotopy $H:[0,1]\times [0,1] \to G$ is called smooth if the intermediate curves $\gamma_s(t)$ are piecewise smooth functions of $t$ for each $s$ and the cross curves $\lambda_t(s)$ are piecewise smooth functions of $s$ for each $t$

********************************************Smooth Deformation Theorem:******************************************** Suppose $F$ is a $\cal C^1$ function with symmetric Jacobian matrix on an open set $G$ and that $\Gamma_0$ and $\Gamma_1$ are piecewise smooth in $G$, with parametrizations $\gamma_0$ and $\gamma_1$ respectively. .
- If $\gamma_0$ and $\gamma_1$ are paths from $x_0$ to $x_1$ and are homotopic in $G$ with fixed endpoints with a smooth homotopy, then
    $$ \int_{\Gamma_0} F \cdot\, d\gamma_0 = \int_{\Gamma_1} F \cdot\, d\gamma_1 $$
- If $\gamma_0$ and $\gamma_1$ are closed curves which are homotopic as closed curves in $G$ with a smooth homotopy, then
    $$ \oint_{\Gamma_0} F \cdot\, d\gamma_0= \oint_{\Gamma_1} F \cdot\, d\gamma_1 $$

Still lacks the theory of integration on continuous curves, to get this result. The proof is equivalent to the one to prove [[Homotopy in C#Smooth Deformation Theorem|Smooth Deformation Theorem]] of complex analysis.

$(*)$Th: Let $F =(F_k)_{k = 1}^n :U \to \Bbb R^n$ be a $\cal C^1$ function on $U$. If $F$ is conservative field on $U$, with $U$ simply connected region.

$$ J_F(x) =(J_F (x))^\top $$

for all $x \in U$, iff $F$ is a conservative field on $U$.

From this result we can get a couple of corollaries
- in $\Bbb R^2$ we get [[Green's Theorem and Curl in R2#^b541fe|conservative iff irrotational]] in a simply connected domain
- in $\Bbb R^3$ we get [[Stokes Theorem and Curl in R3#^c0e398|conservative iff irrotational]] in a simply connected domain

