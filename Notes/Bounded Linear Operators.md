---
tags:
  - Analysis
  - FunctionalAnalysis
---
Subjects: [[Metric and Normed Spaces]], [[Functional Analysis]]
Links: [[Normed Vector Spaces]], [[Complete Metric Spaces]], [[Continuity on Metric Spaces]], [[Norm of Linear Operators for finite dimensions]], [[Space of Linear Transformations]], [[Compactness in Metric Spaces]], [[Dual Vector Spaces]], [[Hilbert Spaces]]

If $V=(V, \|\cdot\|_V)$ and $W= (W, \|\cdot\|_W)$ be normed spaces and $T:V\to W$a linear transformation. Then all the following are equivalents:
- $T$ is continuous
- $T$ is continuous at $0$
- There’s a $c >0$ such that $\|Tv\|_W \le c\|v\|_V$ for all $v \in V$, this is called a *bounded transformation*
- $T$ is Lipschitz continuous.
- If $A \subseteq V$ is bounded, then $T[A]$ is bounded.
- there's an $r>0$ such that $T[B(0, r)]$ is bounded.
- Exists $\sup\{\|T(v)\|_W \mid x \in \overline B(0,1) \}$ and it is finite.

We will denote ${\cal B}(V, W)$ to be
$$
	{\cal B}(V, W) :=\{T: V \to W\mid T \text{ is linear and bounded}\}
$$
and we define 
$$
\|T\|_{{\cal B}(V, W)} := \sup_{\substack{v \in V \\ v \ne 0}} \frac{\|Tw\|_W}{\|v\|_V}
$$
We can see that ${\cal B}(V, W)$ is a vector space, and $\| \cdot \|_{{\cal B}(V, W)}$ is a norm, thus, $({\cal B}(V, W), \|\cdot \|_{{\cal B}(V, W)})$ is a normed space. In the case where $W = V$, then it is denoted as $\mathcal B(V)$. If $W$ is the field, then it is denoted as $V^*$ and it is called the *dual space of $V$* or *topological dual of $V$,* and we call the elements of $V^*$ continuous linear functionals. 

We can see that, that since every $T$ is linear then we can divide by the norm of the vector and we get that $v/\|v\|_V \in S_V$
$$
\|T\|_{{\cal B}(V, W)} = \sup_{v\in S_V} \|Tv\|_W
$$
Similarly we get the, that for any $v \in V$, we get that 
$$
	\|Tv\|_W \le \|T\|_{{\cal B}(V, W)}\|v\|_V
$$
We get the following equivalence, for the norm. Let $V, W$ normed spaces and $T\in \mathcal B(V, W)$:
- $\|T \| =  \sup_{v\in S_V} \|Tv\|_W$ 
- $\|T \| =  \sup_{v\in B(0, 1)} \|Tv\|_W$ 
- $\|T \| =  \min\{ k \ge  0\mid k \text{ is a Lipschitz constant for } T\}$ 

If $W$ is a Banach space, then ${\cal B}(V, W)$ is a Banach space with the metric described above.

We get that no matter $V$, then $V^*$ is complete. 

**Prop:** Let $X$ and $Y$ be normed spaces. If $T\in \mathcal B(X, Y)$ and $(T_n)_{n <\omega}$ is a sequence in $\mathcal B(X, Y)$ such that $T_n \to T$, then $T_n x \to Tx$ for each $x\in X$. 

**Prop:** Let $X$, $Y$ and $Z$ be normed spaces. if $S \in \mathcal B(X, Y)$ and $T\in \mathcal B(Y, Z)$, then $TS \in \mathcal B(X, Z),$ and $\|TS \| \le \|T\| \|S\|$. 

**Cor**: Let $S_k \to S$ in $\mathcal B(V, W)$ and $T_k \to T$ on $\mathcal B(W, Z)$, then $T_k \circ S_k \to T\circ S$. 

**Th:** Let $X$ and $Y$ be normed spaces such that $X$ is infinite dimensional and $Y\neq \{0\}$. Then some linear operator from $X$ into $Y$ is unbounded. In particular, every infinite-dimensional normed space has a linear functional on it that's unbounded.

**Th:** Let $X$ and $Y$ be normed spaces such that $X$ is finite dimensional. Then every linear operator from $X$ into $Y$ is bounded, i.e., $\mathcal L(X, Y) = \mathcal B(X, Y)$.

**Def:** Suppose that $Y$ is a linear operator from a normed space into a normed space $Y$. Then $Y$ is an *isomorphism* or a *normed space isomorphism* into $Y$ if it is a homeomorphism. The operator $Y$ is an *isometric isomorphism* of *linear isometry* if $\|Tx \| = \|x\|$ whenever $x\in X$. The space $X$ is *embedded in $Y$* if there is an isometric isomorphism from $X$ into $Y$. The spaces  $X$ and $Y$ are *isomorphic* if there is an isomorphism from $X$ into $Y$, and are *isometrically isomorphic* if there is an isometric isomorphism from $X$ into $Y$. If $X$ and $Y$ are isomorphic, then it is denoted by writing $X \cong Y$.

**Prop:** Let $T$ be a linear operator from a normed space $X$ into a normed space $Y$.
- The operator $T$ is an isomorphism iff there are $s, t >0$ such that $s\|x\| \le \|Tx\| \le t\|x\|$ whenever $x\in X$. 
- If $T$ is an isometric isomorphism, then $T$ is an isomorphism.
- If $X$ is a Banach space and $T$ is an isomorphism, then $T[X]$ is a Banach space.

**Th:** Let $n \in \Bbb N^+$ be a nonnegative integer and let $X$ and $Y$ be $n$-dimensional normed spaces over $\Bbb F$. Then every surjective linear operator from $X$ into $Y$ is an isomorphism.

**Cor:** Let $n \in \Bbb N^+$. Then all $n$-dimensional normed spaces over $\Bbb F$ are isomorphic to each other.

**Cor:** Every finite-dimensional vector space has exactly one norm topology.

**Cor:** For every $n\in \Bbb N^+$, the only norm topology that $\Bbb F^n$ can have is its Euclidean topology.

**Cor:** Every finite-dimensional normed space is a Banach space.

**Cor:** Every finite-dimensional subspace of a normed space is a closed subspace of the space. 

**Cor:** Every finite-dimensional normed space has the Heine-Borel property, that is, the property that all closed and bounded subsets of the space are compact