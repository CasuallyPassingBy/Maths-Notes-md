---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Topological Groups]], [[Haar Measure]], [[Measures on Hausdorff Spaces]], [[Finite Product of Measures]], [[Space of Continuous Compactly Supported Functions]], [[Finite Products of Measures on Locally Compact Spaces]], [[Lp spaces]], [[Local Compactness]], [[Measurable Functions#Image Measures|Image Measures]], [[Signed and Complex Measures]]

# $L^1(G)$

**Def:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f$ and $g$ belong to ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$. The convolution of $f$ and $g$ is the function $f*g$ from $G$ to $\Bbb F$ defined by  $$(f*g)(t):= \begin{dcases}\int f(s) g(s^{-1}t)\, \mu(ds) & \text{if } s\mapsto f(s)g(s^{-1}t) \text{ is integrable,} \\ \\ 0& \text{otherwise}.\end{dcases}$$
**Lemma:** Let $G$ be a locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f\in {\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$. Then there is a countable family $\{K_n\mid n <\omega\}$ of compact subsets of $G$ such that $f$ vanishes outside of $\bigcup_{n<\omega} K_n$. 

**Lemma:** Let $G$ be a locally compact group, let $\mu$ be a left Haar measure on $G$, and let $F: G\times G \to G\times G$ be defined by $F(s, t) := (s, s^{-1}t)$. Then $F$ is a measure-preserving homeomorphism of $G\times G$ onto itself. That is, $F$ is a homeomorphism such that each Borel subset $A$ of $G\times G$ satisfies $(\mu\times\mu)(A) = (\mu\times\mu)(F^{-1}[A])$. 

**Prop:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f$ and $g$ belong to ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$.
- The function $s\mapsto f(s)g(s^{-1}t)$ belongs to ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$ for $\mu$-almost every $t\in G$.
- The convolution $f*g$ of $f$ and $g$ belongs to ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$ and satisfies $\|f*g\|_1 \le \|f\|_1\|g\|_1.$

We see that the convolution on ${\scr L}^1(G, \mathcal B(G), \mu)$ induces an operation on $L^1(G, \mathcal B(G), \mu, \Bbb F);$ this operation is also denoted by $*$ and called a *convolution*. 

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. Then $L^1(G, \mathcal B(G), \mu)$, with convolution as multiplication, is a Banach algebra. We can usually denote it as $L^1(G)$. 

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. If $f, g\in \mathcal C_c(G)$, then $f*g \in \mathcal C_c(G)$. 

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a left Haar measure on $G$. If $f, g\in \mathscr L^1(G, \mathcal B(G), \mu)$ and if $(f_n)_{n<\omega}$ and $(g_n)_{n<\omega}$ are sequences in ${\scr L}^1(G, \mathcal B(G), \mu)$ such that $f_n \stackrel{L^1}{\longrightarrow} f$, and $g_n \stackrel{L^1}{\longrightarrow} g$, then $f_n*g_n \stackrel{L^1}{\longrightarrow} f*g$. 

**Prop:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f$ and $g$ belong to ${\scr L}^1(G, \mathcal B(G), \mu)$. Note that we can change in the definition of $f*g$ the expression $f(s) g(s^{-1}t)$ can be replaces with the following:
- $f(ts)g(s^{-1})$,
- $f(s^{-1})g(st)\Delta(s^{-1})$, and
- $f(ts^{-1})g(s)\Delta(s^{-1})$.

**Prop:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f_1, f_2, g_1$ and $g_2$ belong to ${\scr L}^1(G, \mathcal B(G), \mu)$. If $f_1 = f_2$ $\mu$-almost everywhere, and if $g_1 = g_2$ $\mu$-almost everywhere, then $f_1*g_1 = f_2*g_2$ everywhere. 

**Prop:** Let $G$ be a locally compact group. Then $G$ is commutative iff $L^1(G)$ is commutative. 

**Prop:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$. If $G$ is first countable, then there is a sequence $(\varphi)_{n<\omega}$ of nonnegative functions in ${\scr L}^1(G, \mathcal B(G), \mu)$, or even in $\mathcal C_c(G)$, such that $$\int \varphi_n \, d\mu = 1 \quad \text{holds for all }n <\omega$$and such that $$ f *\varphi_n \stackrel{L^1}{\longrightarrow} f \quad \text{and}\quad \varphi_n*f \stackrel{L^1}{\longrightarrow} f  \qquad \text{holds for } f\in \mathscr L^1(G, \mathcal B(G), \mu).$$Such sequence is called an *approximate identity.*

**Prop:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$. There is a net $(\varphi)_{\alpha\in A}$ of nonnegative functions in ${\scr L}^1(G, \mathcal B(G), \mu)$, or even in $\mathcal C_c(G),$where $A$ is the set of open neighbourhoods of $e$ and $U \le V$ iff $V\subseteq U$ such that $$\int \varphi_\alpha \, d\mu = 1 \quad \text{holds for all }\alpha\in A$$and such that $$ f *\varphi_\alpha \stackrel{L^1}{\longrightarrow} f \quad \text{and}\quad \varphi_\alpha*f \stackrel{L^1}{\longrightarrow} f  \qquad \text{holds for } f\in \mathscr L^1(G, \mathcal B(G), \mu).$$Such net is called an *approximate identity.*


# $M(G)$

**Lemma:** Let $G$ be a locally compact group. If $\mu$ and $\nu$ are finite positive regular Borel measures on $G$ and if $\mu\times \nu$ is a regular Borel product of $\mu$ and $\nu$, then the formula $$(\mu*\nu)(A) := (\mu\times \nu)(\{(x, y) \in G\times G\mid xy\in A\}) $$defines a regular Borel measure  on $G$. Furthermore, $$(\mu*\nu)(A) = \int \nu(x^{-1} A) \, \mu(dx) = \int \mu(Ay^{-1}) \, \nu(dy) $$holds for each $A$ in $\mathcal B(G)$. 

Let's recall that $M_r(G, \Bbb R)$ is the Banach space of all finite signed regular Borel measures on $G$. Likewise, $M_r(G, \Bbb C)$ is the Banach space of all complex regular Borel measures on $G$. Here we will denote each of those spaces by $M(G)$.

Let $\mu$ and $\nu$ belong to $M(G)$. We define their convolution $\mu*\nu$ by $$(\mu*\nu)(A) = \int\nu(x^{-1}A)\, \mu(dx) = \int \mu(Ay^{-1})\, \nu(dy). $$We see that $\mu*\nu$ is regular, and $\mu*\nu\in M(G)$. 

It is easy to check that if $\mu$ and $\nu$ belong to $M(G)$ and if $f$ is a bounded Borel function on $G$, then $$\int f\, d(\mu*\nu) = \int\left( \int f(xy)\, \mu(dx)\right)\, \nu(dy) = \int \left(\int f(xy)\, \nu(dy)\right)\, \mu(dx). $$
**Prop:** Let $G$ be a locally compact group. Then $M(G)$, with convolution as multiplication, is a Banach algebra.

**Prop:** Let $G$ be a locally compact group. If $\delta_e$ is the points mass concentrated at $e$, then $\delta_e$ is the identity of the algebra $M(G)$. 

**Prop:** Let $G$ be a locally compact group. $G$ is commutative iff convolution is a commutative operation on $M(G)$. 

**Def:** We can define $M_a(G)$ to be the collection of elements of $M(G)$ that are absolutely continuous with respect to some Haar measure on $G$.

**Prop:** Let $G$ be a locally compact group. Then the following statements are true.
- $M_a(G)$ is an ideal in the algebra $M(G)$.
- If $\mu$ is a left Haar measure on $G$, then the map $f\mapsto \nu_f$, where $\nu_f$ is defined by $\nu_f(A) = \int_A f\, d\mu$, induces a norm-preserving algebra homomorphism of $L^1(G)$ into $M(G)$.
- The image of $L^1(G)$ under this homomorphism is $M_a(G)$.

We see that we have a coordinate-free description of $L^1(G)$: it is isomorphic to the algebra $M_a(G)$, whose definition only depends on the existence of Haar measures and not the choice of a particular left or right Haar measure.

**Cor:** We see that $L^1(G)$ has an identity iff the topology of $G$ is discrete. 

**Th:** Let $G$ be a locally compact group, and let $\mu$ be a regular Borel measure on $G$. Then the map $T: L^\infty_b(G, \mathcal B(G), \mu)\to L^1(G, \mathcal B(G), \mu)^*$ defined by $$T({\langle g\rangle})(\langle f\rangle) = \int fg\, d\mu $$is an isometric isomorphism of $L^\infty_b(G, \mathcal B(G), \mu)$ onto the dual of $L^1(G, \mathcal B(G), \mu)$. 

**Prop:** Let $G$ be a locally compact group, and let $\mu$ be a regular Borel measure on $G$. Suppose $\nu\in M(G)$, and $f\in \mathscr L^1(G, \mathcal B(G), \mu)$, and that $\mu_f$ is the finite signed or complex regular Borel measure defined by $$\mu_f(A) := \int_A f\, d\mu. $$We define functions $g$ and $h$ on $G$ by  $$g(t) = \begin{dcases}
\int f(s^{-1}t)\,\nu(ds) & \text{if }s \mapsto f(s^{-1}t) \text{ is }|\nu|\text{-integrable}, \\ \\
0& \text{otherwise,}
\end{dcases} $$and $$h(s) = \begin{dcases}
\int f(st^{-1})\Delta(t^{-1})\,\nu(ds) & \text{if }t \mapsto f(st^{-1})\Delta(t^{-1}) \text{ is }|\nu|\text{-integrable}, \\ \\
0& \text{otherwise.}
\end{dcases} $$Then $g$ and $h$ belong to $\mathscr L^1(G, \mathcal B(G), \mu)$ and that $$(\nu*\mu_f) =\int_A g\, d\mu\quad \text{and}\quad (\mu_f*\nu)(A) = \int_A h\, d\mu  $$for every $A\in \mathcal B(G)$. If in addition, we see that $\nu*\mu_f = 0$ holds for every $f\in \mathscr L^1(G, \mathcal B(G), \mu)$ iff $\nu = 0$. 

**Prop:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$. If $(\varphi_\alpha)_{\alpha\in A}$ is the approximate identity of $L^1(G)$, then the net of measures $(\mu_\alpha)_{\alpha\in A}$ defined by  $$\mu_\alpha(A) = \int_A \varphi_\alpha\, d\mu $$for every $A\in \mathcal B(G)$, converge in the weak$^*$-topology of $M(G)$, when viewed as the dual to $\mathcal C_0(G)$,  to $\delta_e$. 