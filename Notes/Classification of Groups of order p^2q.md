---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Cauchy and Sylow Theorems]], [[Primitive Roots]], [[Semidirect Product of Groups]], [[General Linear Group]]

**Prop:** Let $G$ be a finite group of order $p^2q$, where $p$ and $q$ are distinct primes. Then $G$ has at least one normal Sylow subgroup.
- If $p> q$, then Sylow $p$-subgroup is normal.
- If $q> p$, then either the Sylow $q$-subgroup is normal or the Sylow $p$-subgroup is normal.
In particular, a group of order $p^2q$ cannot be simple.

# Case $p>q$

We can analyse this case further. If $p>q$, and $q\not\mid p^2-1$, then both the Sylow $p$-subgroup and $q$-subgroup are normal, thus $G$ is isomorphic to either $C_{p^2}\times C_q$ or $C_p \times C_p \times C_q$. 

From now we will assume that $q\mid p^2-1$.

Let us consider when the Sylow $p$-subgroup is cyclic. We can use the fact that the integers modulo $p^2$ have a primitive root. Then we see that $\text{Aut}(\Bbb Z/p^2\Bbb Z) \cong (\Bbb Z/p^2\Bbb Z)^\times$, and thus it is cyclic. Note that there's an injective $\varphi:\Bbb Z/q\Bbb Z  \to \text{Aut}(\Bbb Z/p^2\Bbb Z)$ iff $q \mid p(p-1)$, i.e., $q| (p-1)$. Then, by the [[Cyclic Groups#^f4cacf|fundamental theorem of cyclic groups]], we get that there must be a unique cyclic subgroup $W$ of order $q.$ *There is just one nonabelian group of order $p^2q$ having a cyclic Sylow $p$-subgroup*, namely, with $W$ the unique order $q$-subgroup of $(\Bbb Z/p^2\Bbb Z)^\times$, the group of transformations $T_{z, w}: \Bbb Z/p^2 \Bbb Z \to \Bbb Z/p^2 \Bbb Z$, with $z\in \Bbb Z/p^2 \Bbb Z$ and $w\in W$, where $$T_{z, w}(x) := wx+z.$$
It is easy to check that this group is isomorphic to $\Bbb Z/p^2\Bbb Z\rtimes_\varphi \Bbb Z/q\Bbb Z$, with $\varphi: \Bbb Z/q\Bbb Z \to \text{Aut}(\Bbb Z/p^2\Bbb Z)$ an injective group homomorphism. 

Now, suppose that $\mathcal S_p \cong \Bbb Z/p \Bbb Z \times \Bbb Z/p \Bbb Z$. We can interpret $\mathcal S_p$ as a $\Bbb Z/p \Bbb Z$-vector field. So, this means that $\text{Aut}(\mathcal S_p) \cong \text{GL}(2, \Bbb Z/p \Bbb Z)$. 

Let us note that any automorphism $\phi$ of $G$ must take the unique Sylow $p$-subgroup $\mathcal S_p$ to itself, and that $\mathcal S_p$ is abelian, this imples that from the handout on isomorphisms of semidirect products that, for two homomorphisms $\theta_i: \Bbb Z/q\Bbb Z \to \text{Aut}(\mathcal S_p)$, $$\mathcal S_p \rtimes_{\theta_i} \Bbb Z/q\Bbb Z \cong \mathcal S_p \rtimes \Bbb Z/q\Bbb Z$$ iff $\theta_1[\Bbb Z/q\Bbb Z]$ and $\theta_2[\Bbb Z/q\Bbb Z]$ are conjugate subgroups of $\text{Aut}(\mathcal S_p)$. 

This classification problem becomes the linear algebra problem of determining the conjugacy classes of order $q$ of $\text{GL}(2, \Bbb Z/p\Bbb Z)$. 

**Lemma:** Let $A$ be a $2\times 2$ matrix over a field $k$. If $A$ is not a scalar multiple of the identity matrix, then $A$ is similar to the matrix $$\begin{pmatrix}0 & -\det(A) \\ 1 & \text{tr}(A)\end{pmatrix} $$
**Cor:** Two non scalar $2\times 2$ matrices over $k$ are similar iff they have the same eigenvalues. 

We start counting conjugacy classes. Let $A$ be a matrix of order $q$. The eigenvalues of such an $A$ are $q$th roots of unity.

If these eigenvalues are both $1$, then $A$ is similar to $B:= \begin{pmatrix} 0 & -1 \\ 1 & 2\end{pmatrix}$. We see that $B^p = I$, and hence $B^q \neq I$, hence $A^q \neq I$. So the eigenvalues cannot be both $1$. 

We supposed that $q\mid p^2 -1$, so $q$ divides $p-1$ or $p+1$, but not both if $q$ is odd. We have three cases to consider:
- $q= 2$
- $q\mid p+1$, but $q\not\mid p-1$.
- $q\mid p-1$, but $q\not\mid p+1$.

### $q = 2$

If $q=2$. We know that two order-$2$ subgroup of $\text{GL}(2, \Bbb Z/p\mathbb Z)$ are conjugate iff their unique generators are similar. The eigenvalues of $A$ are $(-1, -1)$ or $(1, -1)$. It follows that every order-$2$ subgroup of $\text{GL}(2, \Bbb Z/p\mathbb Z)$ is similar to one and only one of the three groups generate respectively by $$\begin{pmatrix}-1  & 0 \\ 0 & -1\end{pmatrix}\quad \begin{pmatrix}-1  & 1 \\ 0 & -1\end{pmatrix} \quad \begin{pmatrix}1  & 0 \\ 0 & -1\end{pmatrix}.$$We get three pairwise nonisomorphic semidirect products $G$
- $\langle x, y, z \mid x^p = y^p = z^2 = e, xy=yx, zx = x^{-1}z, zy = y^{-1}z\rangle$ 
- $\langle x, y, z \mid x^p = y^p = z^2 = e, xy=yx, zx = x^{-1}z, zy = xy^{-1}z\rangle$ 
- $\langle x, y, z \mid x^p = y^p = z^2 = e, xy=yx, zx = xz, zy = y^{-1}z\rangle$. This isomorphic to $\mathbb Z/p\mathbb Z \times D_{2p}$. 

### $q\mid p+1$, but $q\not\mid p-1$.

In the case where $q\mid p+1$, but $q\not\mid p-1$, we have that $(\Bbb Z/p\Bbb Z)^\times$ has no elements of order $q$, that is, $1$ is the only $q$th root of unity in $\Bbb Z/p\Bbb Z$. We also know that $\text{GL}(2, \Bbb Z/p\Bbb Z)$ has an order of $(p^2-1)(p^2-p)$, which is divisible by $q$. Thus there's at least one element with order $q$.

We know that the eigenvalues $\lambda$ and $\lambda'$ of $A$ satisfy $\lambda \lambda' = \det A = 1$, and that both $\lambda$, and $\lambda'$ cannot both be $1$. We know that $\lambda$ is a root of a quadratic equation, therefore $\mathbb Z/p\mathbb Z[\lambda]$ is a quadratic extension of $\mathbb Z/p\mathbb Z$, and this quadratic extension contains all the roots of the equation $x^q = 1$ (over $\mathbb Z/p\mathbb Z$), namely the powers of $\lambda$. 

If $B \neq I$ satisfies $B^q = I$, then the eigenvalues of $B$ must be of the form $(\lambda^a, 1/\lambda^a) (a,q) = 1$. Hence $B$ is similar to $A^a$, and there is a unique conjugacy class of order-$q$ subgroups of $\text{GL}(2, \mathbb Z/p\mathbb Z)$. 

In this case there exists a unique nonabelian semidirect product. 

### $q\mid p-1$, but $q\not\mid p+1$.

Since $q \mid p-1$, then there are now $q$th roots of unity, forming a cyclic subgroup of $(\Bbb Z/p \Bbb Z)^\times$, with generator $\zeta$. These eigenvalues of $A$ must be of the form $(\zeta^a, \zeta^b)$, where at least one of $a, b$, say $a$, is not divisible by $q$; and then if $c = a^{-1} \pmod q$, $A^c$ has eigenvalues $(\zeta, \zeta^d)$, for some $d$, and $A^c$ generates the same order $q$-subgroup, say $U$ as $A$ does.

Suppose $B$ generates an order $q$ subgroup $V$ and that the eigenvalues of $B$ are $(\zeta, \zeta^e)$. Then $U$ is conjugate to $V$ iff $A$ is similar to some power $B^f$, meaning, the unordered pairs $(\zeta, \zeta^d)$ and $(\zeta^f, \zeta^{ef})$ are the same. This is the same as either $f = 1$ and $e = d$, or $f = d\neq 0$ and $e = d^{-1}$. 

The set of conjugacy classes of order $q$ subgroups of $\text{GL}(2, \mathbb Z/p\mathbb Z)$ correspond $1- 1$ with the set consisting of the $(q-3)/2$ pairs $(d, d^{-1})$ with $d \neq d^{-1}\in \mathbb (\mathbb Z/q\mathbb Z)^\times$, together with the pairs $(1, 1)$, $(1, -1)$, and $(1, 0)$. Thus there are $(q+3)/2$ such conjugacy classes, and correspondingly, there are $(q+3)/2$ nonabelian semidirect products. 

# Case $q > p$
