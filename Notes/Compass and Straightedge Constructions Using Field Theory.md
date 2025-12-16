---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Galois Field Extensions]]

**Elemental Operations:** Suppose given a set of points $\cal P$ of $\Bbb R^2$. The only operations that are permitted are:
- Straightedge: For any two points of $\cal P$ connect them with the unique line between them.
- Compass: Draw a circle with centre as a point in $\cal P$ and radius the distance between any pair of points in $\cal P$. 

**Def:** Let $\mathcal P \subseteq \Bbb R^2$ be a set of points.
- A point $Q\in \Bbb R^2$ is *constructible in a single step* from $\cal P$ if it is the intersection of two different lines, or two circles, or a line and a circle contructed fron $\cal P$ from the elemental operations.
- A point $Q\in \Bbb R^2$ is *constructible* if $\cal P$ if there exists a finite sequence $Q_1,\dots, Q_n = P$ of points of $\Bbb R^2$ such that:
	1. $Q_1$ is constructible in a single step from $\cal P$.
	2. $Q_{i+1}$ is constructible in a single step from $\mathcal P\cup\{Q_j \mid 1 \le j \le i\}$ for $1 \le i <n$,

From elemental geometry we know there are a couple of common constructions.
- Construction of the midpoint of line segment.
- Construction of the perpendicular bisector of a line that pases though a given point. 
- Construction of the parallel line of a line that passes through a given point.

# Algebraic Formulation

**Def:** Let $\cal P\subseteq \Bbb R^2$ be a set of points. A real number $\alpha\in \Bbb R$ is called *constructible*, with compass and straightedge, if there are constructible points $Q_1$ and $Q_2$ of $\Bbb R^2$ from $\cal P$ such that the oriented length of the segment $\overline{Q_1 Q_2}$ is $\alpha$. 

**Prop:** Let ${\cal P} \subseteq \Bbb R^2$ is set of at least two points. If $\alpha, \beta$ are constructible real numbers from $\cal P$, then also $\alpha\pm\beta$, $\alpha\beta$ and $\alpha/\beta$ (when $\beta \ne 0$) are also constructible from $\cal P$. We see that if $K$ is the set of real constructible numbers from $\cal P$, then $K$ is a subfield of $\Bbb R$, and $\Bbb Q \subseteq K \subseteq \Bbb R$. 

**Lemma:** Let $\mathcal P \subseteq \Bbb R^2$ be a set has the $(0,0)$ and $(1,0)$. If $u\ge 0$ is a real constructible from $\cal P$, the $\sqrt u$ is also constructible from $\cal P$.

**Cor:** If $K(\alpha)/K$ is a field extension of degree $2$ such that $K(\alpha) \subseteq \Bbb R$, then every $u\in K(\alpha)$ is constructible from the finite set of points of $K$. 

**Lemma:** Let $\mathcal P \subseteq \Bbb R^2$ is a set of points that have $(0,0), (1,0)\in  \cal P$. Then the point $\alpha= (a,b)\in \Bbb R^2$ is constructible from $\cal P$ iff the points $(a,0)$ and $(b, 0)$ are constructible from $\cal P$. 

Given a set of points ${\cal P} \subseteq \Bbb R^2$ with at least two points, choosing the unit to be the distance between two points of $\cal P$ and using straightedge and compass we can construct $\Bbb Q$ and, and thus $\Bbb Q^2$. 

This explains why we can choose without loss of generality that our set of points to contains ${\cal P} \subseteq \Bbb R^2$  the points $(0,0)$ and $(1, 0)$. 

If $Q = (x, y) \in \Bbb R^2$ is constructible from $\cal P$, then we know that $x$ and $y$ are also constructible real numbers from $\cal P$. In general, if $Q_n = (x_n, y_n)\in \Bbb R^2$ is a constructible point that can be constructed from $\cal P$, then there are a sequence of points $Q_1 =(x_1, y_1),\dots, Q_n$, such that $Q_1$ is constructible from $\cal P$ in a single step, and $Q_{i+1}$ is constructible from ${\cal P} \cup\{Q_j \mid 1 \le j \le i\}$. In on of these cases we can define $$K_{i+1} := K_i(x_{i+1}, y_{i+1}), $$and $K_0 := \Bbb Q$. From this definition, we see that $$\Bbb Q = K_0 \subseteq K_1 \subseteq K_1 \subseteq \cdots \subseteq K_n\subseteq \Bbb R.$$The natural question is what is the value of $[K_{i+1}: K_i]$. 

**Lemma:** With the notation of the last paragraphs, $x_{i+1}$ and $y_{i+1}$ are roots in $K_{i+1}$ of quadratic polynomials of $K_i$.

**Th:** Let ${\cal P}\subseteq \Bbb R^2$ be a set of points that contain the points $(0,0)$ and $(1, 0)$. Let $\alpha\in\Bbb R$. The following statements are equivalent.
- $\alpha$ is constructible.
- There is a finite sequence of real numbers $\alpha_1,\dots, \alpha_n\in \Bbb R$ such that:
	1. $\alpha_1^2\in \Bbb Q$.
	2. $\alpha_{i+1}^2\in \Bbb Q(\alpha_1,\dots, \alpha_i)$ for every $1 \le i <n$. 
	3. $\alpha\in \Bbb Q(\alpha_1,\dots, \alpha_n)$. 

**Cor:** If $\alpha$ is a constructible real number then $[\Bbb Q(\alpha) : \Bbb Q]$ is a power of $2$. 

## Classic Greek Problems

**Th:** It is impossible, with compass and straightedge, to trisect the angle of $\pi/3$. 

This is because if $\alpha = \cos(\pi/9)$, then $[\Bbb Q(\alpha),\Bbb Q] = 3$. This automatically proves that $\cos(2\pi/9)$ and the regular nonagon are impossible using only compass and straightedge. This also implies, although a bit more subtly, that the angles $\pi/180$ and $\pi/90$ are not constructible. 

**Th:** It is impossible, with compass and straightedge, to duplicate the volume of a cube.

This is because $[\Bbb Q(\sqrt[3]2),\Bbb Q] = 3$.

**Th** It is impossible, with compass and straightedge, to square the circle.

This is because $\pi$ is transcendental over $\Bbb Q$.

## Constructible Regular Polygons

We are gonna identify the plane $\Bbb R^2$ with $\Bbb C$, with the natural isomorphism $(a,b) \mapsto a+bi$. 

**Cor:** We see that the regular pentagon and hexagon are constructible with compass and straightedge. 

**Th:** Let $\cal P\subseteq \Bbb C$ be a set of points that contain $0$ and $1$. Let $\alpha\in \Bbb C$. The following statements are equivalent.
- $\alpha\in\Bbb C$ is constructible from $\cal P$.
- There exists a sequence $\alpha_0,\dots,\alpha_n\in\Bbb C$ such that $\alpha_i^2\in \Bbb Q(\alpha_0,\dots, \alpha_{i-1})$ and $\alpha\in \Bbb Q(\alpha_0,\dots, \alpha_n)$.
- $\alpha$ is algebraic over $\Bbb Q$, and the [[Normal Closure of a Field|normal closure]] $N$ of $\Bbb Q(\alpha)/\Bbb Q$ has degree $[N: \Bbb Q] = 2^r$ for some integer $r \ge 0$. 

**Gauss-Wantzel Theorem:** Let $n \ge 1$ be an integer. The regular $n$-gon is constructible with compass and straightedge iff $$ n = 2^m p_1\cdots p_r,$$where $m\ge 0$ and $p_i$ are [[Fermat primes]]. 

The proof relies that a primitive $n$th root of unity is constructible iff the regular $n$-gon is constructible. We use that we  the $n$th [[Cyclotomic Polynomials and Extensions|cyclotomic extension]] is a normal extension, and that we know has degree $\varphi(n)$. Finally, we just check that $\varphi(n)$ is a power of $2$, which only happens if the odd primes are Fermat primes, and with $1$ as their exponent. 

**Prop:** An angle $\theta$ can be trisected with compass and straightedge iff the polynomial $$f(x) = 4x^3-3x+\cos(\theta)$$is reducible over $\Bbb Q(\cos(\theta))$. 

**Cor:** The angle of $\pi/60$, or $3°$, is constructible using only compass and straightedge. Explicitely, $$\begin{align*}
\cos \frac\pi{60} &= \frac1{8}(\sqrt3-1)\sqrt{5+\sqrt 5}+\frac1{16}(\sqrt6-\sqrt2)(\sqrt 5-1) \\
\sin \frac\pi{60} &= \frac 1{16}(\sqrt6+\sqrt 2)(\sqrt5-1)-\frac18 (\sqrt3-1)\sqrt{5-\sqrt5},
\end{align*}
$$
Because I found it mildly interesting we can calculate $\cos(2\pi/5)$ and $\sin(2\pi/5)$, $$\cos\frac{2\pi}5 = \frac{\sqrt5 -1}{4}, \qquad \sin\frac{2\pi}5 = \sqrt\frac{5+\sqrt 5}{8}.$$
