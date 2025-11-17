---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]]

**Def:** If $G$ is a group and $X$ is a set, a *left action* of $G$ on $X$ is a map $\alpha: G\times X \to X$, often written $(g, x) \mapsto g\cdot x$, that satisfies for all $x\in X$ and $g_1, g_2\in G$:
- $g_1 \cdot (g_2 \cdot x) = (g_1g_2) \cdot x$
- $e\cdot x =x$ 
We call $X$ a *$G$-set.* If $X$ has a left action of $G$ on $X$, $(X, \alpha)$.

Additionally, we can define a $\beta: X \times G\to X$, often written $(x, g)\mapsto x\cdot g$ that satisfies for all $x\in X$ and $g_1, g_2\in G$:
- $(x \cdot g_1) \cdot g_2 = x\cdot(g_1g_2)$
- $x\cdot e =x$ 
Then we say that $\beta$ is a *right action of $G$ on $X$*. 

**Def:** If $X \neq \varnothing$, let $G \times X \to X$ given by $g*x= x$ for all $x\in X$, then we say that $G$ acts on $X$ *trivially*. 

**Def:** If $G$ is a group acting on $X$. We define the set of *fixed points of $g$* for $g\in G$, as $$X^g := \{x\in X\mid g*x = x\}.$$
**Def:** For any $x\in X$, the *orbit* of $x$ under the action is the set $$\text{orb}_\alpha(x) = G \cdot x := \{g\cdot x \mid g\in G\},$$the set of all images of $x$ under the action by elements of $G$.

**Def:** Given $x\in X$, the *isotropy group* of $x$ or the *stabiliser of $x$*, denoted by $G_x$, is the set of elements $g\in G$ that fix $x$: $$G_x := \{g\in G \mid g\cdot x =x\} $$
**Examples:** 
- If $H \le G$, and $H$ acts on $G$ by left translations, $H \times G \to G$ given by $h*g = hg$, then $\text{orb}_H(g) =Hg.$  
- If $G$ is a group, and $G$ acts on itself via conjugation, $G \times G \to G$ such that $\sigma* g = \sigma g \sigma^{-1}$, then $G_g = Z_G(g)$, the [[Subgroups#^0fafab|centraliser]] of $g$ in $G$, and $\text{orb}_G(g)$ is the conjugation class of $g$ in $G$.

**Orbit-Stabilser Theorem:** If $X$ is a $G$-set, then for each $x\in X$ we have that $$|\text{orb}_G(x)| = [G: G_x].$$
**Cor:** If $G$ is a finite group, and $H, K \le G$, then for all $x\in G$ we have that $$|HxK| = \frac{|H||K|}{|H \cap xKx^{-1}|} $$ ^81eaff

**Th:** Suppose $G$ is a group, and $X$ is a $G$-set. For each $x\in X$, and $g\in G$, then $$G_{g\cdot x} = g G_x g^{-1}. $$
**Cor:** Let $X$ be a $G$-set. if for some $x\in X$ we have that $G_x \trianglelefteq G$, then for all $y \in \text{orb}_G(x)$ we have that $G_y = G_x$.

**Burnside's Lemma or Frobenius Theorem:** Let $G$ be a finite group, and $X$ be a finite $G$-set. If $n$ is the number of orbits of $X$ under the action of $G$, then $$n = \frac1{|G|} \sum_{g\in G}|X^g|. $$
**Obs:** Let be $X$ a $G$-set. The action of $G$ on $X$ induces a homomorphism $\phi:  G \to S_X$, given by $\phi(g)(x) = g*x$. Additionally, if $\psi: G \to S_X$ is a homomorphism, then $\psi$ induces an action of $G$ on $X$ given by $\sigma*x := \phi(\sigma) (x)$. This means that a $G$-action on $X$ is the same as a homomorphism $\phi:G \to S_X$.  We can write it as $$\text{Act}(G, X) \leftrightarrow \text{Hom}(G, S_X). $$
The homomorphism from $\phi: G \to S_X$ above is called the *permutation representation* associated to a given action. 

**Def:** If $X$ is a $G$-set, then the action of $G$ on $X$ is called *faithful* if its permutation representation is injective. Let $\alpha: G \times X \to X$ be an action on, then we can define its kernel to be the kernel of its permutation representation. 

**Prop:** Let $\alpha:G \times X \to X$ be an action, and $\phi:G \to S_X$ be its permutation representation, then $$\ker\alpha := \ker\phi = \bigcap_{x\in X} G_x $$
**Cor:**  Let $\alpha:G \times X \to X$ be an action, $\phi:G \to S_X$ be its permutation representation, and $N = \ker \phi \trianglelefteq G$, then $G/N$ acts faithfully on $X$, there's $\tilde\phi: G/N \to S_X$ is injective, such that $\tilde\phi$ is the permutation representation of the action of $G/N$ on $X$. 

**Def:** Let $X$ be a $G$-set, then we the subset of $X^G$ of $X$ is called the *fixed-point set* or the *set of $G$-fixed points*, of the $G$-action on $X$. We can also call them the *invariant elements,* and we can denote it as $X^ G$ or $\text{Fix}_G(X)$.  ^7f0380
# Types of Actions

The action is *transitive* if for any two points $x, y \in X$, there is a group element $g\in G$ such that $\alpha(g, x) = y$, or equivalently if the orbit of any point is all of $X$

The action is said to be *free* if the only element of $G$ that fixes any element of $X$ is the identity: $\alpha(g, x) = x$ implies that $g = e$. This is equivalent to the requirement that $G_x = \{e\}$ for every $p\in X$. 

**Jordan's Theorem:** Let $X$ be a finite set such that $|X| = n \ge 2$, and a finite group $G$ acts transitively on $X$, then there's some $g\in G$ such that $|X^g| = 0$. We can define $G_0 := \{g\in G \mid |X^g| = 0\}$, then $|G_0| \ge n-1$. 

**Cor:** Let $X$ be a finite transitive $G$-set, and $G$ be a finite group, then $$\sum_{g\in G}|X^g| = |G|. $$
**Cor:** Suppose $G$ is a group and $X$ is a transitive $G$-set, then the set $\{G_s \mid s\in S\}$ of all isotropy groups is exactly only one conjugacy class of subgroups. This conjugacy class is called the *isotropy type of $X$*. 