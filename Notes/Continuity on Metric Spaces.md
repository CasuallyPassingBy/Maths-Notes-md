---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Metric Spaces]], [[Continuity on R]], [[Uniform Continuity on R]], [[Limits and Continuity of Vector valued functions of Rn]], [[Normed Spaces]], [[Space of Linear Transformations]]
### Continuity

A function $f:(X,d) \to (Y,\rho)$ between metric spaces is continuous at $z \in X$ iff:

$$ \forall \varepsilon \exists \delta>0 \forall x\in X[d(x,z) < \delta \implies \rho(f(x), f(z)) < \varepsilon] $$

we say that $f$ is continous if it’s continuous at every $z \in X$

A function $\phi: X \to Y$ is a **homeomorphism** if $\phi$ is continuous and bijective, and $\phi^{-1}: Y\to X$ is continuous. We say that $X$ and $Y$ are **homeomorphic** if there exists a homeomorphism between them. If $\phi$ is uniformly continuous, with a uniformly continuous inverse, we call it a uniform homeomorphism, and $X$ and $Y$ are called uniformly homeomorphic. This means that the [[Topology on Metric Spaces|topologies generated]] by the metrics on $X$ and $Y$ .

Let $\phi: X \to Y$ and $\psi: Y\to Z$ be functions between metric spaces.
- If $\phi$ and $\psi$ are continuous, then $\psi \circ \phi : X \to Z$ is continuous
- If $\phi$ is a homeomorphism, then $\psi$ is continuous iff $\psi \circ \phi : X \to Z$ is continuous
- If $\psi$ is a homeomorphism, then $\phi$ is continuous iff $\psi \circ \phi : X \to Z$ is continuous

### Uniform Continuity
A function $f:(X, d) \to (Y, \rho)$ between metric spaces, is uniformly continuous if for every $\varepsilon>0$, there’s a $\delta >0$ such that for all $x, y \in X$, such that $d(x,y) < \delta$ implies then ${\rho(f(x), f(y)) < \varepsilon}$, or symbollically

$$ \forall \varepsilon >0\exists\delta>0 \forall x,y \in X[d(x,y)<\delta \implies \rho(f(x), f(y)) < \varepsilon ] $$

Since this property is global, then we say that $f$ is uniformly continuous on $X$.

if $f$ is uniformly continuous then $f$ is continuous.


### Lipschitz Continuity

A function $\phi: X \to Y$ is _**Lipschitz continuous**_, if there’s $c >0$ such that )

$$ d_Y(\phi(x), \phi(y)) \le c d_X(x, y) $$

The constant $c$ is called the _**************Lipschitz constant**************_ for **************_$\phi$._

The function $\phi$ is an **equivalence if $\phi$ is Lipschitz continuous and bijective, and $\phi^{-1}:Y\to X$ is Lipschitz continuous

If $\phi$ is Lipschitz continuous, then $\phi$ is unifomrly continuous

We get the following properties:

- if $f:X\to Y$ and $g:Y \to Z$ are uniformly continuous, then $f \circ g$ is uniformly continuous.
- if $f:X\to Y$ and $g:Y \to Z$ are Lipschitz continuous, then $f \circ g$ is Lipschitz continuous.

The _********canonical projections********_ are the functions $\pi_X : X \times Y \to X$, and $\pi_y :X\times Y \to Y$, given by

$$ \pi_X (x, y) = x \qquad \pi_Y(x,y) = y $$

The canonical projections are Lipschitz continuous.

$\phi:Z \to X\times Y$ is continuous iff $\pi_X \circ \phi$ and $\pi_Y \circ \phi$ are continuous.

If $V=(V, \|\cdot\|_V)$ and $W= (W, \|\cdot\|_W)$ be normed spaces and $L:V\to W$a linear transformation. Then all the following are equivalents:
- $L$ is continuous
- $L$ is continuous at $0$
- There’s a $c >0$ such that $\|Lv\|_W \le c\|v\|_V$ for all $v \in V$, this is called a *bounded transformation*
- $L$ is Lipschitz continuous.

This tells us, that the "nice" linear maps, are the bounded ones. This comes really useful, because we can study their properties, of [[Bounded Linear Operators]]

If $d$ is a metric on $V$ we say that

- $d$ is **translation invariant** if for any $v, w , z\in V$ it is satisfied that
    
    $$ d(v+z, w+z ) = d(v, w) $$
    
- $d$ is **absolutely homogeneous** if it for any $v, w\in V$ anf $\lambda \in \Bbb R$
    
    $$ d(\lambda v, \lambda w) = |\lambda|d(v, w) $$
    

With the translation invariance, we get that the sum of vectors is continuous and with both properties we get that the scalar product is also continuous. This two properties are enough to tell us that there is a norm $\|\cdot \|$ on $V$ such that it induces $d$.

We can define an important function. Let $A$ be a nonempty subset of $X$ and $x \in X$. The distance of $x$ to $A$ is the real number

$$ \text{dist}(x, A) = \inf_{y \in A}d(x, y) $$

If we let $f: X \to \Bbb R^{\ge 0}$, defined as $f(x) = \text{dist}(x, A)$ is Lipschitz continuous. For any $x\in X$ it is satisfied that $\text{dist}(x, A) = 0$ iff $x\in \overline A$. 