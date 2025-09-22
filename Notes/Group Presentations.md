---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]], [[Normal Subgroups and Quotient Groups]], [[Free Groups]]

**Def:** We define a *group presentation* to be ordered pair, denoted by $\langle S \mid R\rangle$, where $S$ is an arbitrary set and $R$ is a set of elements of the free group $F(S)$. The elements of $S$ and $R$ are called the *generators* and *relators*, respectively, of the presentation. 

A group presentation defined a group, also denoted by $\langle S\mid R\rangle$, as the following quotient group: $$\langle S\mid R\rangle = F(S) / \overline R,$$where $\overline R$ is the *normal closure of $R$ in $F(S)$*. This $\langle S \mid R\rangle$ is a group. 

If a group is defined by a presentation $\langle S \mid R\rangle$, it is quite easy to describe homomorphism from it to another group $H$. We only need to know where the generators are sent and how they neutralised using the relators. Formally, we define a map from the generating set $S$ to $H$. As long as the natural extension of this map to a homomorphism $F(S)\to H$ takes each element of R$ to the identity, its kernel must contain $\overline R$, so it descents to the quotient by the factorization theorem from $\langle S \mid R\rangle$ to $H$. 

**Def:** Suppose $G$ is an arbitrary group. A *presentation of $G$* a group presentation $\langle S \mid R\rangle$ together with a specific isomorphism $\langle S \mid R \rangle \cong G$. 

Note that if that isomorphism exist it is uniquely determined by specifying which element of $G$ corresponds to each generator in $S$. 

**Th:** Every group has a presentation.

**Def:** If $G$ admits a presentation $\langle S \mid R\rangle$ in which both $S$ and $R$ are finite sets, we say that $G$ is *freely generated*. In this case, we usually write the presentation as $\langle s_1,\dots, s_n \mid r_1,\dots, r_m\rangle$. Since the $r_i$ actually all become equal to the identity in the group defined by the presentation, it is also often convenient to replace the relators by the equations obtauned by setting them equal to the identity, called *realtions* of the presentation, as in $$\langle s_1,\dots, s_n \mid r_1 = 1,\dots, r_m= 1\rangle$$ or even $$\langle s_1,\dots, s_n \mid r_1 = q_1,\dots, r_m = q_m\rangle.$$

**Presentations of Familiar Groups:**
- The free group on generators $\alpha_1,\dots, \alpha_n$ has a presentation $\langle \alpha_1,\dots, \alpha_n \mid \varnothing\rangle$. In particular, $\Bbb Z$ has the presentation $\langle \alpha \mid \varnothing\rangle$.
- The group $\Bbb Z \times \Bbb Z$ has presentation $\langle \beta, \gamma\mid \beta\gamma = \gamma\beta\rangle$.
- The [[Cyclic Groups|cyclic group]] $C_n$ has the presentation $C_n \cong \langle \alpha \mid \alpha^n = 1\rangle$.
- The [[Dihedral Groups|Dihedral group]] $D_{2n}$ has presentation $D_{2n} \cong \langle r,s \mid r^n = s^2 = (sr)^2 = 1\rangle$. 
- Let $\{G_\alpha\}_{\alpha <\kappa}$ be a collection of groups, if each $G_\alpha$ has a presentation $\langle S_\alpha \mid R_\alpha\rangle$, and the collection $\{S_\alpha\mid \alpha <\kappa\}$ is pairwise disjoint, then $\coprod_\alpha G_\alpha$ has a presentation $$\left\langle \left.\bigcup_{\alpha <\kappa} S_\alpha \; \right\rvert\; \bigcup_{\alpha <\kappa} R_\alpha\right\rangle.$$