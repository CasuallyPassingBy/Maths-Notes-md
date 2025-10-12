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
**Th:** Suppose $G$ is a group, and $X$ is a $G$-set. For each $x\in X$, and $g\in G$, then $$G_{g\cdot x} = g G_x g^{-1}. $$
**Cor:** Let $X$ be a $G$-set. if for some $x\in X$ we have that $G_x \trianglelefteq G$, then for all $y \in \text{orb}_G(x)$ we have that $G_y = G_x$.

**Burnside's Lemma or Frobenius Theorem:** Let $G$ be a finite group, and $X$ be a finite $G$-set. If $n$ is the number of orbits of $X$ under the action of $G$, then $$n = \frac1{|G|} \sum_{g\in G}|X^g|. $$
**Obs:** Let be $X$ a $G$-set. The action of $G$ on $X$ induces a homomorphism $\phi:  G \to S_X$, given by $\phi(g)(x) = g*x$. Additionally, if $\psi: G \to S_X$ is a homomorphism, then $\psi$ induces an action of $G$ on $X$ given by $\sigma*x := \phi(\sigma) (x)$. This means that a $G$-action on $X$ is the same as a homomorphism $\phi:G \to S_X$.  We can write it as $$\text{Acc}(G, X) \leftrightarrow \text{Hom}(G, S_X). $$
The homomorphism from $\phi: G \to S_X$ above is called the *permutation representation* associated to a given action. 

**Def:** If $X$ is a $G$-set, then the action of $G$ on $X$ is called *faithful* if its permutation representation is injective. Let $\alpha: G \times X \to X$ be an action on, then we can define its kernel to be the kernel of its permutation representation. 

**Prop:** Let $\alpha:G \times X \to X$ be an action, and $\phi:G \to S_X$ be its permutation representation, then $$\ker\alpha := \ker\phi = \bigcap_{x\in X} G_x $$
**Cor:**  Let $\alpha:G \times X \to X$ be an action, $\phi:G \to S_X$ be its permutation representation, and $N = \ker \phi \trianglelefteq G$, then $G/N$ acts on $X$, there's $\tilde\phi: G/N \to S_X$ is injective, and there's a faithful action from $G/N$ on $X$. 

# Types of Actions

The action is *transitive* if for any two points $x, y \in X$, there is a group element $g\in G$ such that $\alpha(g, x) = y$, or equivalently if the orbit of any point is all of $X$

The action is said to be *free* if the only element of $G$ that fixes any element of $X$ is the identity: $\alpha(g, x) = x$ implies that $g = e$. This is equivalent to the requirement that $G_x = \{e\}$ for every $p\in X$. 

**Cor:** Suppose $G$ is a group and $X$ is a transitive $G$-set, then the set $\{G_s \mid s\in S\}$ of all isotropy groups is exactly only one conjugacy class of subgroups. This conjugacy class is called the *isotropy type of $X$*. 

# Equivariant Maps

Suppose $X$ and $Y$ are both $G$-sets. A map $F: X \to Y$ is said to be *equivariant* with respect to the given $G$-action if for each $g \in G$, $$F(g \cdot x) = g \cdot F(x).$$Equivalently, if $\theta$ and $\varphi$ are the given actions on $X$ and $Y$, respectively, $F$ is equivariant if the following diagram commutes for each $g \in G$: 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[r, "F"] \arrow[d, "\phi_g"'] & Y \arrow{d}{\phi_g} \\
X \arrow[r, "F"'] & Y
\end{tikzcd}
\end{document}
```

Equivariant maps are homomorphism in the [[Categories and Functors|category]] of $G$-sets (for a fixed $G$). Hence they are also known as $G$-morphisms, $G$-maps, or $G$-homomorphisms. Isomorphisms of $G$-sets are simply bijective equivariant maps. Note that the inverse of a $G$-isomorphism is another $G$-isomorphism

**Example:** Let $G$ and $H$ be groups, and $\phi: G \to H$ be a Lie group homomorphism. There is a natural action of $G$ on itself by left-translation. We define a left action $\theta$ of $G$ on $H$ by $$\theta(g, h) = F(g) h.$$ With respect to theses $G$-actions, $F$ is an equivariant. 

**Properties of $G$-Equivariant Maps:** Suppose $G$ is a group, and $X$, $Y$ are $G$-sets.
- If $G$ acts transitively on $X$, then any two $G$-equivariant maps from $X$ to $Y$ that agree on one element of $X$ are identical.
- If $X$ is nonempty, and $G$ acts transitively on $Y$, then every $G$-equivariant map from $X$ to $Y$ is surjective. 
- If $G$ acts transitively on $X$, then given $x\in X$ and $y\in Y$, there exists a (necessarily unique) $G$-equivariant map $\varphi:X\to Y$ satisfying $x\mapsto y$ iff $G_x \subseteq G_y$. 

**$G$-Set Isomorphism Criterion:** Suppose $X$ and $Y$ are $G$-sets with a transitive action. 
- Given $x\in X$ and $y\in Y$, there exists a necessarily unique $G$-isomorphism $\varphi:X \to Y$ taking $x \mapsto y$ iff $G_x = G_y$. 
- $X$ and $Y$ are $G$-isomorphic iff they have the same isotropy type. 

**Def:** If $X$ is a $G$-set, a $G$-isomorphism from $X$ to $X$ is called a *$G$-automorphism of $X$*. We know that the set of $G$-automorphisms from a group, see [[Automorphism Group|this]], and it is called the *$G$-automorphism group of $X$*, and it is denoted by $\text{Aut}_G(X)$. 

**Prop:** Suppose $X$ is transitive $G$-set. For any $x, y\in X$, there exists a necessarily unique $\varphi\in \text{Aut}_G(x)$ such that $x\mapsto y$ iff $G_x = G_y$.

**Characterisation of $G$-Automorphism Groups:** Let $X$ be a transitive $G$-set, and let $x\in X$. For each $g\in N_G(G_x)$, there is a unique $G$-automorphism $\varphi_g: X \to X$ such that $\varphi_g(x) = g\cdot x$. The map $g\mapsto \varphi_g$ is a surjective homomorphism from $N_G(G_x)$ to $\text{Aut}_G(X)$ whose kernel is $G_x$, and thus descends to an isomorphism $$N_G(G_x)/G_x \cong \text{Aut}_G(X),$$where $N_G(G_x)$ is the [[Group Actions on Themselves|normalizer]] of $G_x$ in $G$. 