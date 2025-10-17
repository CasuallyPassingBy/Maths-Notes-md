---
tags:
  - GraphTheory
---
Subjects: [[Group Theory]]
Links: [[Group Actions]]

**Obs:** If $X$ is a $G$-set, with $X$ and $G$ finite sets, and $r$ is the number of orbits on $X$, then we take representatives $x_1, \dots, x_r$ of each of the orbits. We know that $$|X| = \sum_{i = 1}^r |\text{orb}_G(x_i)|.$$We can define an auxiliary set $$X^G := \{x \in X \mid \forall g\in X(gx = x)\},$$Meaning that $X^G$ is the union of all the orbits that only contain a single element. If $s = |X^G|$, then $0\le s \le r$. We make the additional, assumption that $x_1, \dots, x_s$ are the elements that have single element orbits, and $x_{s+1}, \dots, x_r$ are the representative of the orbits with more than one element, then we get that $$|X| = |X^G| + \sum_{i = s+1}^r |\text{orb}_G(x_i)|.$$
An important example, is when $G$ acts on itself by conjugation. Note that the orbits are the conjugation classes of $G$. If $x$ has orbit with only itself it is because it is part of the [[Subgroups#^0fafab|centre of the group]]. If we denote $C_1, \dots, C_t$ to be the conjugation classes of $G$ with more than one element, we get that $$|G| = |Z(G)| + \sum_{i = 1}^t|C_i|.$$This is called *class equation of $G$*. We can make one final simplification $$|G| = |Z(G)| + \sum_{i = 1}^t[G: G_{x_i}].$$
**Th:** If $G$ is a group of order $p^n$, with $p$ prime, and $X$ is a finite $G$-set, then $$|X| \equiv |X^G| \pmod p.$$
**Cauchy's Theorem:** If $G$ is a finite group and $p$ is a prime that divides $|G|$, then $G$ has an element of order $p$, and thus $G$ has a subgroup of order $p$.

**Def:** Given a group $G$, we denote $Y$ to be the family of subgroups of $G$ and let $G$ act on $Y$ via conjugation: if $H \in Y$ and $\sigma \in G$, then $\sigma*H := \sigma H \sigma^{-1} \in Y$. If we consider its isotropy group $$G_H := \{\sigma \in G \mid \sigma H \sigma^{-1} = H\},$$we note that $H \trianglelefteq G_H$. Also note that $G_H$ is the largest subgroup of $G$ where $H$ is normal. This group is called the *normalizer of $H$ on $G$*, and will be denoted by $N_G(H)$ or simply $N(H)$ if $G$ is understood by context. 

**Def:** If $G$ is a finite group such that $|G| = p^n$ for some prime $p$, then we say that $G$ is a $p$-group. Note that this definition only applies to finite groups. 

**Lemma:** Let $G$ be a finite group. If $H$ is a subgroup and has order a power of a prime $p$, then $$[N(H) : H] \equiv [G:H] \pmod p.$$
**Cor:** Let $G$ be a finite group and $H$ be a $p$-subgroup of $G$. If $p$ divides $[G:H]$, then $H \neq N(H)$.

# Sylow's Theorem

**Sylow's First Theorem:** Let $G$ be a finite group of order $n$ and suppose that there's a prime $p$ such that $n = p^m t$ with $m \ge 1$ and $p \not\mid t$, then $G$ has a subgroup of order $p^j$ for each $1 \le j \le m$. 

**Def:** If $G$ is a finite group of order $n$ and $p$ is a prime such that $p^m \;\|\;n$ with $m \ge 1$, a subgroup $L \le G$ is with order $p^m$ is called a *Sylow $p$-subgroup of $G$*. The set of Sylow $p$-subgroups of $G$ is denoted as $\text{Syl}_p(G)$. 

**Obs:** If $L$ is a Sylow $p$-subgroup of $G$, then for every $g\in G$, then $gLg^{-1}$ is also a Sylow $p$-subgroup.

**Sylow's Second Theorem:** Let $G$ be a finite group of order $n$, and $H_1, H_2\le G$ are two Sylow $p$-subgroups of $G$, then $H_1$ and $H_2$ are conjugated.

**Cor:** If $G_1$ and $G_2$ be finite groups, and let $G = G_1 \times G_2$, then the Sylow $p$-subgroups of $G$ are of the form $H_1 \times H_2$, where $H_1$ and $H_2$ are Sylow $p$-subgroups of $G_1$ and $G_2$, respectively. 

**Cor:** Let $G$ be a finite group of order $n$, there is a unique Sylow $p$-subgroup of $G$ iff there's a normal Sylow p-subgroup. In particular, if $G$ is abelian, all Sylow $p$-subgroups of $G$ are unique. 

**Cor:** Let $G$ be a finite group. If for each prime $p$, there's a unique Sylow $p$-subgroup of $G$, then $G$ is the internal direct product of its Sylow subgroups. 

**Sylow's Third Theorem:** Let $G$ be a finite group of order $n$, $p$ a prime such that $p \mid n$, and $n_p$ is the Sylow $p$-subgroups of $G$, then $$n_p \equiv 1 \pmod p, \quad n_p = [G: N_G(P)],$$where $P$ is any Sylow $p$-subgroup of $G$, and $n_p \mid n$.

**Example:** If $G = S_p$, with $p$ prime, then we know that $|S_p| = p (p-1)!$, and $p \not\mid (p-1)!$, thus the Sylow $p$-groups of $S_p$ must have order exactly $p$. Thus, the Sylow $p$-groups must be cyclic, and $S_p$ has exactly $(p-1)!$ number of $p$-cycles.  If $n_p$ is the number of Sylow $p$-groups, then $n_p (p-1) = (p-1)!$, and $n_p = (p-2)!$. Lastly, by Sylow's third theorem, we know that $n_p \equiv 1 \pmod p$, and $(p-2)! \equiv 1 \pmod p$. Getting another proof of [[Wilson's Theorem]].

## Applications of Sylow's Theorem

**Def:** If $p$ is a prime, a group $G$ is said to be a $p$-group if every element of $G$ has order a power of $p$.

**Prop:** A finite group $G$ is a $p$-group iff it has order a power of $p$.

**Lemma:** If $G$ is a finite $p$-group, then $Z(G)$ is nontrivial.

**Cor:** If $G$ is a non abelian $p$-group, then $G$ is not simple.

**Cor:** If $p$ is prime, then every group $G$ of order $p^2$ is abelian.

**Cor:** Every group of order $p^2$ is isomorphic to $\Bbb Z/p^2\Bbb Z$ or $\Bbb Z/p\Bbb Z \times \Bbb Z/p\Bbb Z$. 

**Lemma:** Let $G$ be an arbitrary group and $H$ be a subgroup with index $n$ in $G$. Then, there's a normal subgroup $N$ of $G$ that is contained in $H$ such that $[G: N]$ is finite and divides $n!$.

**Prop:** Let $G$ be a finite group of order $n$, and let $p$ be smallest prime that divides $n$, then every subgroup with index $p$ in $G$ is normal. 

**Cor:** If $G$ is a group of order $pq$ with $p>q$ primes, then $G$ is not simple. 

**Prop:** Let $G$ be a group of order $pq$, with $p >q$ primes. If $p \not\equiv 1 \pmod q$, then $G$ is cyclic.

**Th:** Let $G$ be a group of order $pq$, with $p>q$ primes.
- If $G$ is abelian, then $G \cong \Bbb Z/pq\Bbb Z$ is cyclic of order $pq$.
- If $G$ is not abelian, then $p \equiv 1 \pmod q$ and $G \cong \langle a, b\mid a^q =1 = b^p, aba^{-1} = b^r\rangle$, where $r$ integer such that $1 < r <p$ and $r^q \equiv 1 \pmod p$. 

**Example:** If $p >2$ is a prime, there's a nonabelian group $G$ of order $2p$ such that $p \equiv 1\pmod 2$, we get by the theorem $$G \cong \langle a,b \mid a^2 = b^p, aba^{-1} = b^r\rangle,$$where $r$ is number such that $1<r<p$ and $r^2 \equiv 1 \pmod p$. Now we have that $p \mid r^2-1,$ thus $r \equiv 1, p-1 \pmod p$, thus $r \equiv -1 \pmod p$, and we get that $aba = b^{-1}$. This means that $G$ is isomorphic to the dihedral group of order $2p$, or $D_p$.